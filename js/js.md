## JS

- JavaScript=ECMAScript+DOM API+BOM API
- Node.js=ECMAScript+操作系统 API+文件系统 API+网络 API+数据库 API

### 定义

- 函数声明，也就是使用 function 关键字声明的函数。在变量对象中以函数名建立一个属性，属性值为指向该函数所在内存地址的引用。如果函数名的属性已经存在，那么该属性将会被新的引用所覆盖。

- 变量声明，每找到一个变量声明，就在变量对象中以变量名建立一个属性，属性值为 undefined。如果该变量名的属性已经存在，为了防止同名的函数被修改为 undefined，则会直接跳过，原属性值不会被修改。

## Node.js

### 异步

- 不同类型的观察者（消息队列？），处理的优先级不同，idle 观察者最先，I/O 观察者其次，check 观察者最后。
- idle 观察者：顾名思义，就是早已等在那里的观察者，以后会说到的 process.nextTick 就属于这类
- I/O 观察者：顾名思义，就是 I/O 相关观察者，也就是 I/O 的回调事件，如网络，文件，数据库 I/O 等
- check 观察者：顾名思义，就是需要检查的观察者，后面会说到的 setTimeout/setInterval 就属于这类
- macro-task 包括：script(整体代码), setTimeout, setInterval, setImmediate, I/O, UI rendering。
- micro-task 包括：process.nextTick, Promises, Object.observe, MutationObserver
- 执行顺序：函数调用栈清空只剩全局执行上下文，然后开始执行所有的 micro-task。当所有可执行的 micro-task 执行完毕之后。循环再次执行 macro-task 中的一个任务队列，执行完之后再执行所有的 micro-task，就这样一直循环。
- Promise 封装异步代码，Promise 本身不是异步

### fs 扩展:fs-extra

Promises 接口

- copy(srcpath, dstpath):复制文件或目录,默认覆盖目标路径
- move(srcpath, dstpath):移动文件或目录,默认不覆盖目标路径
- remove('/tmp/myfile'):删除文件或目录
- emptyDir:初始化指定目录(创建或清空目录)
- pathExists(file):测试给定路径是否存在
- outputFile(file, 'hello!'):写入文件,自动创建目录
- outputJson(file, {name:'a'}):对象写入 JSON 文件,自动创建目录
- readJson('./package.json'):读取 JSON 文件将其解析为对象
- ensureLink(srcpath, dstpath):确保链接存在
- ensureSymlink(srcpath, dstpath):确保符号链接存在

## Electron

### 路径

- \_\_dirname：当前文件所在目录，模块导入使用的相对路径。electron 打包后文件在 asar 包内，如 app.asar\main.js，app.asar\index.html
- process.execPath：执行文件安装路径
- process.cwd()：执行文件启动路径，child_process.fork，fs 等使用的相对路径。
- process.resourcesPath：electron 应用，资源文件路径
- require('path').resolve(process.argv[2]) //基于执行时路径获取绝对路径,一般只适用于解析命令行参数路径
- require('path').parse('/test/hello.json') //解析路径,获取路径文件信息
- \_\_filename===module.filename //是当前文件名
- \_\_dirname //当前文件路径
- process.cwd() //只有 require 的路径是相对当前文件即:\_\_dirname，其他大部分函数接收的路径都是相对于程序运行时路径即:process.cwd()
- process.chdir('/tmp') //可以修改当前工作空间即:process.cwd()的值
- require.main.filename //入口文件名
- process.execPath //node 可执行文件路径
- require('path').parse(require.main.filename).dir //项目根目录

### Web Worker 子线程

- 渲染进程中,有跨域问题

### child_process.fork 子进程

- 主进程和渲染进程中

### 渲染进程中 child_process 和 process 功能似乎不完整，加 remote 调用？

"use strict"//es6 严格模式
"use asm";//asmjs 模式
让 cmd 支持 utf-8：chcp 65001

node --harmony es6
babel-node es6
iojs es6

type：类型
typeof 返回变量基本数据类型:number,boolean,string,object,undefined,function
instance：实例
（对象的）实例:new 一个对象创建出来的是 instance（对象的实例）
基本数据类型不是任何对象的实例
constructor：对象的构造函数
对象《===》函数，函数的构造函数是 Function
typeof new String() 返回 object
typeof 'a' 返回 string
'a' instanceof 　 String 返回 false
'a'.constructor==String 返回 true
new String() instanceof 　 String 返回 true
new String().constructor==String 返回 true
function a(){}
typeof a //return function
a.constructor==Function //return true

创建对象的实例有三步：
function A(x){
　　 this.x=x;
}
var obj=new A(1);

1. 创建 Object 对象的实例 obj：obj=new Object();
   　　 2. 将 obj 的内部**proto**指向构造他的对象 A 的 prototype 3. 将 obj 作为 this 去调用构造函数 A，从而设置成员并初始化。此时，obj 具有了 x 属性，同时具有了对象 A 的原型的所有成员,所有实例共享对象成员而不是每个实例都有对象成员的一个副本
   Js 所有"函数"都有 prototype
   对象的 prototype 的 constructor 指向对象本身
   instance 的**proto**指向其对象的 prototype
   function A(x){
   　　 this.x = x;
   }
   A.prototype.a = "a";
   function B(x,y){
   A.call(this,x);//B 的实例成员继承 A 的实例成员：x
   this.y = y;
   }
   //B.prototype = new A();//B 的原型继承 A 的所有：原型成员 a 和实例成员 x，实例化对象时，同名的原型成员会被实例成员取代（obj 的成员 x 是 B 的实例成员 x 而非 B 的原型成员 x）
   B.prototype =A.prototype//B 的原型只继承 A 的原型成员 a 不继承实例成员 x
   B.prototype.b = function(){
   　　 alert("b");
   }//此时 B 有实例成员 x,y，原型成员（对象成员）a,b,x,继承的成员可以重写
   B.prototype.constructor = B;//原型继承后修正 constructor
   var obj = new B(1,3);//调用 B 的构造函数，初始化实例成员：x,y

let Calculator = function (decimalDigits, tax) {
this.decimalDigits = decimalDigits;
this.tax = tax;
};
Calculator.prototype = {
add: function(x, y) {
return x + y;
},
subtract: function(x, y) {
return x - y;
}
};

const 合格的常量声明关键字
const 命令只是指向变量所在的地址,不可变的只是这个地址，即不能把 const 指向另一个地址，但对象本身是可变的，所以依然可以为其添加新属性。
对象冻结，应该使用 Object.freeze 方法，不能再添加新属性
const foo={a:{b:1}}
let constantize = obj => {
Object.freeze(obj);
Object.keys(obj).forEach( (key, value) => {
if ( typeof obj[key] === 'object' ) {
constantize( obj[key] );
}
});
};
constantize(foo)

let 合格的变量声明关键字

解构赋值
let [head, ...tail] = [1, 2, 3, 4];
//head 1
//tail [2, 3, 4]

let { log, sin, cos } = Math//将 Math 对象的对数、正弦、余弦三个方法，赋值到对应的变量上

字符串也可以解构赋值。这是因为此时，字符串被转换成了一个类似数组的对象。
const [a, b, c, d, e] = 'hello';
a // "h"
b // "e"
c // "l"
d // "l"
e // "o"
类似数组的对象都有一个 length 属性，因此还可以对这个属性解构赋值。
let {length : len} = 'hello';
len // 5

变量的解构赋值用途很多。
（1）交换变量的值
[x, y] = [y, x];

函数只能返回一个值，如果要返回多个值，只能将它们放在数组或对象里返回。有了解构赋值，取出这些值就非常方便。
// 返回一个数组
function example() {
return [1, 2, 3];
}
var [a, b, c] = example();
// 返回一个对象
function example() {
return {
foo: 1,
bar: 2
};
}
var { foo, bar } = example();

函数参数的解构也可以使用默认值。
function move({x = 0, y = 0} = {}) {
return [x, y];
}
move({y: 8,x: 3}); // [3, 8],参数可以无次序
move({x: 3}); // [3, 0]
move({}); // [0, 0]
move(); // [0, 0]

解构赋值对提取 JSON 对象中的数据，尤其有用。
var jsonData = {
id: 42,
status: "OK",
data: [867, 5309]
}
let { id, status, data: number } = jsonData;
console.log(id, status, number)
// 42, OK, [867, 5309]

var map = new Map();
map.set('first', 'hello');
map.set('second', 'world');
for (let [key, value] of map) {
console.log(key + " is " + value);
}
// 获取键名
for (let [key] of map)
// 获取键值
for (let [,value] of map)

加载模块时，往往需要指定输入那些方法。解构赋值使得输入语句非常清晰。
const { SourceMapConsumer, SourceNode } = require("source-map");

4 个字节问题
JavaScript 内部，字符以 UTF-16 的格式储存，每个字符固定为 2 个字节。对于那些需要 4 个字节储存的字符（Unicode 码点大于 0xFFFF 的字符），JavaScript 会认为它们是两个字符。汉字“??”的码点是 0x20BB7，UTF-16 编码为 0xD842 0xDFB7（十进制为 55362 57271），需要 4 个字节储存。ES6 提供了 codePointAt 方法，能够正确处理 4 个字节储存的字符，返回一个字符的码点。codePointAt 方法的参数，是字符在字符串中的位置（从 0 开始）。JavaScript 将“??”视为 2 个字符，codePointAt 方法在第一个字符上，正确地识别了“??”，返回了它的十进制码点 134071（即十六进制的 20BB7）。在第二个字符（即“??”的后两个字节）上，codePointAt 方法的结果与 charCodeAt 方法相同。
"??".length // 2
"??".codePointAt(0)//134071
"??".codePointAt(1)//57271
String.fromCodePoint(134071)//??
String.fromCodePoint 可以识别辅助平面的字符（编号大于 0xFFFF）
codePointAt 方法是测试一个字符由两个字节还是由四个字节组成的最简单方法。
function is32Bit(c) {
return c.codePointAt(0) > 0xFFFF;
}
is32Bit("??") // true
is32Bit("吉") // false
'??吉利'.at(0)// '??'
Unicode 表示
"\uD842\uDFB7"//"??" es5
"\u{20BB7}"//"??" es6
ES6 对正则表达式添加了 u 修饰符，用来识别处理大于\uFFFF 的 Unicode 字符。
/^\S$/.test('??') // false
/^\S$/u.test('??') // true
/\u{20BB7}/u.test('??') // true
正确返回字符串长度
function codePointLength(text) {
var result = text.match(/./gu);
return result ? result.length : 0;
}
"??".length // 2
codePointLength("??") // 1

有些 Unicode 字符的编码不同，但是字型很相近，比如，\u004B 与\u212A 都是大写的 K。
/k/i.test('\u212A'), // false
/k/iu.test('\u212A') // true
上面代码中，不加 u 修饰符，就无法识别非规范的 K 字符。
为了表示语调和重音符号，Unicode 提供了两种方法。一种是直接提供带重音符号的字符，比如 ǒ（\u01D1）。另一种是提供合成符号（combining character），即原字符与重音符号的合成，两个字符合成一个字符，比如 O（\u004F）和 ˇ（\u030C）合成 ǒ（\u004F\u030C）。
ES6 提供 String.prototype.normalize()方法，用来将字符的不同表示方法统一为同样的形式，这称为 Unicode 正规化。
'\u004F\u030C'.normalize('NFC').length, // 1
'\u01D1'.normalize('NFD').length,//2
'\u01D1'=== '\u004F\u030C'.normalize()//true
NFC，默认参数，表示“标准等价合成”（Normalization Form Canonical Composition），返回多个简单字符的合成字符。所谓“标准等价”指的是视觉和语义上的等价。
NFD，表示“标准等价分解”（Normalization Form Canonical Decomposition），即在标准等价的前提下，返回合成字符分解的多个简单字符。
NFKC，表示“兼容等价合成”（Normalization Form Compatibility Composition），返回合成字符。所谓“兼容等价”指的是语义上存在等价，但视觉上不等价，比如“囍”和“喜喜”。
NFKD，表示“兼容等价分解”（Normalization Form Compatibility Decomposition），即在兼容等价的前提下，返回合成字符分解的多个简单字符。
语调
'a\u0304a\u0301a\u030Ca\u0300'
var s = "Hello world!";
s.startsWith("world", 6) // true
s.endsWith("Hello", 5) // true
s.includes("Hello", 6) // false
使用第二个参数时，endsWith 的行为与其他两个方法有所不同。它针对前 n 个字符，而其他两个方法针对从第 n 个位置直到字符串结束。
repeat()返回一个新字符串，表示将原字符串重复 n 次。
"x".repeat(3) // "xxx"
"hello".repeat(2) // "hellohello"
正则表达式的 y 修饰符
“粘连”（sticky）修饰符。它的作用与 g 修饰符类似，也是全局匹配，后一次匹配都从上一次匹配成功的下一个位置开始，不同之处在于，g 修饰符只要剩余位置中存在匹配就可，而 y 修饰符确保匹配必须从剩余的第一个位置开始，这也就是“粘连”的涵义。
y 修饰符的设计本意，就是让头部匹配的标志?在全局匹配中都有效。
/a+/y 等价于/^a+/g
字符串转正则模式
var str = 'hello. how are you?';
RegExp.escape = require('regexp.escape');
var regex = new RegExp(RegExp.escape(str), 'g');
模板字符串（template string）是增强版的字符串，用反引号（`）标识。它可以当作普通字符串使用，也可以用来定义多行字符串，或者在字符串中嵌入变量。所有的空格和缩进都会被保留 var name = "Bob", time = "today"`Hello ${name}, how are you${time}?`var obj = {x: 1, y: 2}`\${obj.x + obj.y}`function fn() { return "Hello World"; }`foo \${fn()} bar`模板字符串可以紧跟在一个函数名后面，该函数将被调用来处理这个模板字符串。这被称为“标签模板”功能（tagged template）。函数的第一个参数是一个数组，该数组的成员是模板字符串中那些没有变量替换的部分，函数的其他参数，都是模板字符串各个变量被替换后的值。 var total = 30; var msg = passthru`The total is ${total} (${total\*1.05} with tax)\n\n\n`; function passthru(literals,...values) { console.log(literals) console.log(literals.raw) console.log(values) var output = ""; for (var i = 0; i < values.length; i++) output += literals[i] + values[i] return output += literals[i] } 模板处理函数的第一个参数（模板字符串数组），还有一个raw属性。这是为了方便取得转义之前的原始模板而设计的。 String.raw方法，往往用来充当模板字符串的处理函数，返回一个斜杠都被转义（即斜杠前面再加一个斜杠）的字符串，对应于替换变量后的模板字符串。String.raw方法也可以作为正常的函数使用。这时，它的第一个参数，应该是一个具有raw属性的对象，且raw属性的值应该是一个数组。 String.raw`Hi\n\${2+3}!` // "Hi\\n5!"
String.raw({ raw: 'test' }, 0, 1, 2)// 't0e1s2t'
// 等同于
String.raw({ raw: ['t','e','s','t'] }, 0, 1, 2)

ES6 提供了二进制和八进制数值的新的写法，分别用前缀 0b 和 0o 表示。
0b111110111 === 503 // true
0o767 === 503 // true

取代 angularJS：模板字符串、Object.observe
取代 jquery：querySelector、querySelectorAll

class C {
constructor(x) {
this.x = x;
}
a() {
console.log("a");
}
}
class D extends C {
constructor(x, y) {
super(x); // 调用父类的 constructor(x, y)
this.y = y;
}
b() {
console.log("b");
}
}
var obj2 = new D(1,3);

类与继承、模块、异步、闭包

可选(国际区号可选(0 或 00 或+开头,接 1-3 位数字,-),国内区号(0 开头,接 2-3 位数字,-)),7－8 位数字座机号,1-4 位数字分机号

<SCRIPT LANGUAGE="JavaScript">
function testit(){
var filter1=
/^(((0|00|\+)?\d{1,3}-)?0\d{2,3}-)?(\d{7,8})(-(\d{1,4}))?$/;
var filter=new RegExp(
"^(((0|00|\\+)?\\d{1,3}-)?0\\d{2,3}-)?(\\d{7,8})(-(\\d{1,4}))?$"
);
console.log(filter1,filter1+''===filter+'',filter)
alert(filter1.test(txt.value));
alert(filter.test(txt.value));
}

##TODO

- 变量对象/活动对象/作用域链/原型链/闭包/this/上下文, window.performance.
