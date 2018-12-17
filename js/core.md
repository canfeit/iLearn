第一个 ECMAScript 标准是基于 Netscape Navigator 4 发布的 JavaScript 版本，它依然缺失重要的特性，比如正则表达式、JSON、异常，以及内置对象的重要方法。不过，在浏览器中它工作得不错。JavaScript 正开始变得越来越好。1997 年 6 月，版本 1 发布了。
标准的第二版 ECMAScript 2 的发布是用来纠正 ECMA 和 JavaScript ISO 标准（ISO/IEC 16262）之间的不一致性的，所以语言没有做任何改动。这个版本发布于 1998 年 6 月。
ECMAScript 3：第一次大变动
ECMAScript 2 后工作在继续，对该语言的第一次大变更出现了。这个版本带来了：

正则表达式

do-while 块

异常和 try/catch 块

更多有关字符串和数组的内置函数

格式化数字输出

in 和 instanceof 运算符

更好的错误处理

ECMAScript 3 发布于 1999 年 12 月。

2000 年 11 月，Netscape Navigator 6 发布。这个版本是对过去版本的重大修订，支持 ECMAScript 3。大约在一年半后，Firefox 发布。它是一个基于 Netscape Navigator 代码库的精简版浏览器，也支持 ECMAScript 3。这些浏览器与 IE 一起，继续推动 JavaScript 的成长

在 ECMAScript 4 开发的最高峰，有如下这些特性：

类

接口

命名空间

包

可选的类型注解

可选的静态类型检查

结构类型

类型定义

多方法（Multimethods）

参数化类型

尾调用

迭代器（Iterator）

生成器（Generator）

内省

类型识别的异常处理器

常量绑定

块作用域

解构

函数表达式

数组推导式（Array comprehensions）
总之，ECMAScript 4 花了近 8 年的时间开发，最后却被废弃了。这对涉及的所有人来说都是一个沉重的教训。
单词 "Harmony（和谐）" 出现在上面的结论中。这是将来对 JavaScript 扩展时项目的标准名称。Harmony 会是所有人都同意的方案。在 ECMAScript 3.1 发布后（以版本 5 的形式，下面我们会看到），所有 JavaScript 中要讨论的新主意都会出现在 ECMAScript Harmony 中。
在 ECMAScript 4 的漫长斗争之后，从 2008 年开始，社区就在注意力放在 ECMAScript 3.1 上。ECMAScript 4 被废弃。在 2009 年，ECMAScript 3.1 完成，并且涉及的各方都签字确认了。而 ECMAScript 4 即使还没有真正发布，也已经被公认为是 ECMAScript 的一个特定变种，所以委员会决定将 ECMAScript 3.1 重新命名为 ECMAScript 5，以避免混淆。

ECMAScript 5 成为了最受支持的 JavaScript 版本之一，也成为了很多转译器的编译目标。ECMAScript 5 被 Firefox 4 (2011)、Chrome 19 (2012)、Safari 6 (2012)、Opera 12.10 (2012) 和 Internet Explorer 10 (2012）完全支持。

ECMAScript 5 是对 ECMAScript 3 的一种相当谨慎的更新，它包括：

Getter/setters

数组和对象字面量中的尾随逗号

保留关键字可以作为属性名

新的 Object 方法（create、defineProperty、keys、seal、freeze、getOwnPropertyNames 等等）

新的 Array 方法（isArray、indexOf、every、 some、map、filter、reduce 等等）

String.prototype.trim 和属性访问

新的 Date 方法（toISOString、now、toJSON）

函数 bind

JSON

不可变的全局对象（undefined、NaN、Infinity）

严格模式

其它次要的变更（parseInt 忽略前导零、抛出的函数有正确的 this 值，等等）

ECMAScript 4 草案将这个新版本描述为编写大型应用程序而设计。如果你已熟悉 ECMAScript 6/2015，就会注意到很多来自 ECMAScript 4 的特性被重新引入了。
在我们的 JavaScript 2015 特性概述一文中，我们对 ECMAScript 2015 的新特性做了一个全面的概述。你也可以看看 ECMAScript 兼容性表，了解一下在实现方面我们现在的确切位置。

新特性小结如下：

Let（词法上的）和 const（不可重新绑定的）绑定

箭头函数（匿名函数的简写）以及词法 this（包含作用域 this）

类（原型之上的语法糖）

对象字面量提升（计算键、短方法定义等等）

模板字符串

Promise

Generator、iterable、iterator 和 for..of

函数的默认参数及剩余运算符

扩展语法

解构

模块语法

新集合（Set、Map、WeakSet、WeakMap）

代理和反射

Symbol 数据类型

类型化数组

内置支持子类化

有保证的尾调用优化

更简单的 Unicode 支持

二进制和八进制字面量
2016 年发布的版本是一个相当小的版本。它包括：

取幂运算符（\*\*）

Array.prototype.includes

一些小的更正（generator 不能与 new 一起用等等）。

ECMAScipt 2017
async/await
Object.values 和 Object.entries

字符串补白

Object.getOwnPropertyDescriptors

函数参数允许尾随逗号
es next

SIMD API

异步迭代（async/await + 迭代）

Generator 箭头函数

64 位 整型操作

Realm（状态分离/隔离）

共享内存和原子

WebAssembly
es 标准化之外的本地扩展

总结
JavaScript 的历史漫长而崎岖。它先被提议为用于 Web 的 Scheme，然后早早就被类 Java 的语法束缚住了。它的第一个原型在几周之内就被开发出来了。受市场之害，它在两年之内变了三个名字。然后被标准化了，同时得到一个听起来像皮肤病的名字。在三次成功的发布后，第四版陷入开发地狱约八年。开发方向一变再变，莫衷一是。然后，纯通过一个特性（AJAX）的成功，社区又重归行动一致，恢复了开发。第 4 版被废弃，一个次要版本，即人人皆知的 第 3.1 版本，被重命名为 第 5 版。第 6 版又在开发上花了很多年，不过这次委员会成功了，虽然又决定改名，但是这次是改为 2015。这个修订版很大，花了很多时间实现，但是最终，给 JavaScript 带来了新风。社区像以前一样活跃。Node.js、V8 和其它项目已经把 JavaScript 带到了一个前所未有的地步。Asm.js、WebAssembly 正进一步改进它。并且不同阶段活跃的提案都让 JavaScript 的未来像以前一样光明。这是一条漫长的路，充满崎岖，而 JavaScript 依然始终是最成功的语言之一。这本身就是一种证明。永远把赌注押在 JavaScript 上。

## 一切都是对象

http://www.cnblogs.com/wangfupeng1988/p/3977924.html
类继承 x
原型继承 v
typeof 3.14.toString()
typeof (1).toString()
原型继承的继承链是由实实在在的对象构成的，而类继承系统是通过抽象的类定义（class definition）来进行继承。在实际应用中，原型继承的一个最大特性就是灵活，因为继承链上的每一个对象、甚至继承链本身都是可以动态修改的。相比之下，类继承需要事先定义好所有的类和它们之间的继承关系，绝大部分类继承系统都不支持在运行时动态修改这些已经定义好的东西。有些事情在类继承系统里是做不到（或很难做到）的，比如修改原型等于同时修改了所有继承自该原型的对象，将一个原型的属性部分混入另一个原型，甚至是在现有的继承链中插入一个节点

## 大怪癖：基础类型与对象

也许在匆忙开发的 JavaScript 中，最大的错误之一是某些行为类似的对象有不同的类型。例如，字符串字面量（"Hello world"）的类型与 String 对象（new String('Hello world')）的类型就是不相同的。这就让我们有时候不得不采用不必要的、容易混淆的类型检查。

> typeof "hello world"
> < "string"

> typeof new String('hello world')
> < "object"

## 作用域只有 2 种: 全局作用域和方法作用域

## 闭包

使用闭包定义私有变量

通常，JavaScript 开发者使用下划线作为私有变量的前缀。但是实际上，这些变量依然可以被访问和修改，并非真正的私有变量。这时，使用闭包可以定义真正的私有变量：

```js
function Product() {
  var name;
  this.setName = function(value) {
    name = value;
  };
  this.getName = function() {
    return name;
  };
}
var p = new Product();
p.setName("Fundebug");
console.log(p.name); // 输出undefined
console.log(p.getName()); // 输出Fundebug
```

## prototype

每个 JavaScript 构造函数都有一个 prototype 属性，用于设置所有实例对象需要共享的属性和方法。prototype 属性不能列举。JavaScript 仅支持通过 prototype 属性进行继承属性和方法。

## 变量提升

JavaScript 会将所有变量和函数声明移动到它的作用域的最前面，这就是所谓的变量提升(Hoisting)。也就是说，无论你在什么地方声明变量和函数，解释器都会将它们移动到作用域的最前面。因此我们可以先使用变量和函数，而后声明它们。

但是，仅仅是变量声明被提升了，而变量赋值不会被提升。

f(); // 我是函数声明
function f() {
console.log('我是函数声明');
}
var f = function() {
console.log('我是赋值型函数');
}
函数声明提升覆盖变量声明提升

## apply, call 与 bind 方法

JavaScript 开发者有必要理解 apply、call 与 bind 方法的不同点。它们的共同点是第一个参数都是 this，即函数运行时依赖的上下文。

三者之中，call 方法是最简单的，它等价于指定 this 值调用函数：
var user = {
name: "Rahul Mhatre",
whatIsYourName: function() {
console.log(this.name);
}
};
user.whatIsYourName(); // 输出"Rahul Mhatre",
var user2 = {
name: "Neha Sampat"
};
user.whatIsYourName.call(user2); // 输出"Neha Sampat"
apply 方法与 call 方法类似。两者唯一的不同点在于，apply 方法使用数组指定参数，而 call 方法每个参数单独需要指定：

apply(thisArg, [argsArray])
call(thisArg, arg1, arg2, …)
var user = {
greet: "Hello!",
greetUser: function(userName) {
console.log(this.greet + " " + userName);
}
};
var greet1 = {
greet: "Hola"
};
user.greetUser.call(greet1, "Rahul"); // 输出"Hola Rahul"
user.greetUser.apply(greet1, ["Rahul"]); // 输出"Hola Rahul"
使用 bind 方法，可以为函数绑定 this 值，然后作为一个新的函数返回：

var user = {
greet: "Hello!",
greetUser: function(userName) {
console.log(this.greet + " " + userName);
}
};
var greetHola = user.greetUser.bind({greet: "Hola"});
var greetBonjour = user.greetUser.bind({greet: "Bonjour"});
greetHola("Rahul") // 输出"Hola Rahul"
greetBonjour("Rahul") // 输出"Bonjour Rahul"

## Memoization

## 块作用域

```js
for (let i = 0; i < 10; i++) {
  setTimeout(function() {
    console.log(i);
  }, 0);
}
```

for 循环创建了一个块级作用域，let 创建了一个块级作用域内变量 i,let 声明的变量只在 let 所在代码块内有效，因此每次循环的 i 都是一个新的变量,这个 i 和上一次循环的 i 本质上是不同的变量，在内存中的地址是不同的，循环进行了几次，就创建了几个变量,每一次 for 循环都重新绑定一次作用域且每-次循环结束离开作用域，变量销毁，就是 let 自身的特色

function createFunctionArray() {
var m = 'this is outer function',
arr = [];
for(var i = 0; i < 5; i++){
arr[i] = function () {
console.log(m,i);
}
}
return arr;
}
createFunctionArray()[0](); // 5
createFunctionArray()[1](); // 5
createFunctionArray()[2](); // 5
createFunctionArray()[3](); // 5
createFunctionArray()[4](); // 5
在函数 createFunctionArray 中，利用循环创造了一个数组，数组里面的每一项都是对一个函数的索引。但是输出结果并不是想象中的 1，2，3，4，5，这是为什么呢？

首先我们要知道在 for 循环中声明的 i 变量和 m 、 arr[]变量都是 createFunctionArray 函数作用域内的变量。function () { console.log(m,i); }函数在创建时，会创建[scope]属性，该属性指向函数外层的活动对象集合，这里就是 createFunctionArray 和 全局对象。然后当函数执行时，会创建函数的执行环境，通过复制[scope]的内容，创建执行环境的作用域链，再把函数自身的活动对象推到作用域链最前端。函数执行时遇到的变量就通过作用域链依次向上查找。

这里的 function () { console.log(m,i); }在执行时，其中的 m 和 i 变量不在函数自身的活动对象中，因此需要向上查找，而此时 for 循环已经结束，因此访问到的 i 变量值均是 5。

function createFunctionArray() {
let m = 'this is outer function',
arr = [];
for(let i = 0; i < 5; i++){
arr[i] = function () {
console.log(m,i);
}
}
return arr;
}
createFunctionArray()[0](); // 0
createFunctionArray()[1](); // 1
createFunctionArray()[2](); // 2
createFunctionArray()[3](); // 3
createFunctionArray()[4](); // 4
在采用了 ES6 的方式声明变量之后，可以看到能够按照预期以次输出 0、1、2、3、4，但是我们看到此时的 function () { console.log(m,i); }在执行时访问 m 和 i 变量依旧是向外查找的，也就是说函数在执行时，它的作用域链是自身的活动对象->for 循环的块级活动对象->createFunctionArray 的活动对象->全局对象，其中 for 循环的块级活动对象、createFunctionArray 的活动对象以及全局对象，这三个是外层活动对象，是在函数创建时就存在的，函数自身的活动对象是执行添加的。

为什么这时的 i 可以准确地依次输出呢？首先，let 声明的变量只在声明的{}内有效，所以 function () { console.log(m,i); } 在创建时，每次都要声明一个 i 变量，也就是说这个 i 和上一次循环的 i 本质上是不同的变量，在内存中的地址是不同的，循环进行了几次，就创建了几个变量。而之前采用 var 声明的时候，由于 i 变量提升的关系，每次的循环只是对 i 重新赋值，没有重新声明。也就是说，采用 let 声明之后，每个 function () { console.log(m,i); }执行时查找的 i 变量本质上是不同的变量。
for 循环还有一个特别之处，就是设置循环变量那部分是一个父级作用域，而循环体内部是一个单独的子作用域。

## 暂时性死区

只要块级作用域内存在 let 命令，它所声明的变量就“绑定”（binding）这个区域，不再受外部的影响。

var tmp = 123;
if (true) {
tmp = 'abc';
let tmp;
}
存在全局变量 tmp，但是块级作用域内 let 又声明了一个局部变量 tmp，导致后者绑定这个块级作用域，所以在 let 声明变量前，对 tmp 赋值会报错。
ES6 明确规定，如果区块中存在 let 和 const 命令，这个区块对这些命令声明的变量，从一开始就形成了封闭作用域。凡是在声明之前就使用这些变量，就会报错。
“暂时性死区”也意味着 typeof 不再是一个百分之百安全的操作。

typeof x; // ReferenceError
let x;
上面代码中，变量 x 使用 let 命令声明，所以在声明之前，都属于 x 的“死区”，只要用到该变量就会报错。因此，typeof 运行时就会抛出一个 ReferenceError。

作为比较，如果一个变量根本没有被声明，使用 typeof 反而不会报错。

typeof undeclared_variable // "undefined"

## 作用域链(Scope Chain)

在 JavaScript 中，函数也是对象，实际上，JavaScript 里一切都是对象。函数对象和其它对象一样，拥有可以通过代码访问的属性和一系列仅供 JavaScript 引擎访问的内部属性。其中一个内部属性是[[Scope]]，由 ECMA-262 标准第三版定义，该内部属性包含了函数被创建的作用域中对象的集合，这个集合被称为函数的作用域链，它决定了哪些数据能被函数访问。

当一个函数创建后，它的作用域链会被创建此函数的作用域中可访问的数据对象填充
在全局函数创建时，它的作用域链中会填入一个全局对象，该全局对象包含了所有全局变量
执行此函数时会创建一个称为“运行期上下文(execution context)”的内部对象，运行期上下文定义了函数执行时的环境。每个运行期上下文都有自己的作用域链，用于标识符解析，当运行期上下文被创建时，而它的作用域链初始化为当前运行函数的[[Scope]]所包含的对象。
执行此函数时会创建“活动对象(activation object)”，包含了函数的所有局部变量、命名参数、参数集合以及 this，此对象会被推入作用域链的前端，当运行期上下文被销毁，活动对象也随之销毁。
无论函数是在哪里调用，也无论函数是如何调用的，其确定的词法作用域永远都是在函数被声明的时候确定下来的。
当定义一个函数时，它实际上保存一个作用域链。
当调用这个函数时，它创建一个新的对象来储存它的参数或局部变量，并将这个对象添加保存至那个作用域链上，同时创建一个新的更长的表示函数调用作用域的“链”。
对于嵌套函数来说，情况又有所变化：每次调用外部函数的时候，内部函数又会重新定义一遍。因为每次调用外部函数的时候，作用域链都是不同的。内部函数在每次定义的时候都要微妙的差别---在每次调用外部函数时，内部函数的代码都是相同的，而且关联这段代码的作用域链也不相同。
作用域链的非自己部分在函数对象被建立（函数声明、函数表达式）的时候建立，而不需要等到执行，这部分作用域链是静态的；当函数执行时，建立一个自己当次执行的作用域，然后把这个作用域与前面的作用域链关联起来

## 执行栈

在一个函数内部定义的函数会将包含函数（即外部函数）的活动对象添加到它的作用域链中。
当我们创建一个函数时，会创建一个预先包含全局变量对象的作用域链，这个作用域链被保存在函数内部的[[scope]]属性中，当调用函数时，会为函数创建一个执行环境，然后通过复制函数的[[scope]]属性中的对象构建起执行环境的作用域链
当某个函数被调用时，会创建一个执行环境（函数一旦被调用，则进入函数执行环境）和相应的作用域链（作用域链是随着执行环境的不同而动态变化的）。（对于函数而言）之后使用 arguments 和其他命名参数的值来初始化函数的活动对象（每个执行环境都有一个变量对象，对于函数成为活动对象）。对于闭包函数而言，在作用域链中，作用域链的前端即为本函数的活动对象，外部函数的活动对象始终处于第二位，外部函数的外部函数的活动对象始终处于第三位。。。直至作为作用域链终点的全局执行环境。

## 原型与原型链

在 Javascript 中，每个函数都有一个原型属性 prototype 指向自身的原型，而由这个函数创建的对象也有一个 proto 属性指向这个原型，而函数的原型是一个对象，所以这个对象也会有一个 proto 指向自己的原型，这样逐层深入直到 Object 对象的原型，这样就形成了原型链
每个函数都是 Function 函数创建的对象，所以每个函数也有一个 proto 属性指向 Function 函数的原型。这里需要指出的是，真正形成原型链的是每个对象的 proto 属性，而不是函数的 prototype 属性，这是很重要的。

```js
const Parent = function(name) {
  this.name = name;
};
Parent.prototype.getName = function() {
  return this.name;
};
const Child = function(name) {
  Parent.apply(this, arguments);
};
const _ = function() {};
_.prototype = Parent.prototype;
Child.prototype = new _();
Child.prototype.constructor = Child;
```

## 私有变量、函数

在具体说 prototype 前说几个相关的东东，可以更好的理解 prototype 的设计意图。之前写的一篇 JavaScript 命名空间博客提到过 JavaScript 的函数作用域，在函数内定义的变量和函数如果不对外提供接口，那么外部将无法访问到，也就是变为私有变量和私有函数。

function Obj(){
var a=0; //私有变量
var fn=function(){ //私有函数

}
}
这样在函数对象 Obj 外部无法访问变量 a 和函数 fn，它们就变成私有的，只能在 Obj 内部使用，即使是函数 Obj 的实例仍然无法访问这些变量和函数

var o=new Obj();
console.log(o.a); //undefined
console.log(o.fn); //undefined

## 静态变量、函数

当定义一个函数后通过 “.”为其添加的属性和函数，通过对象本身仍然可以访问得到，但是其实例却访问不到，这样的变量和函数分别被称为静态变量和静态函数，用过 Java、C#的同学很好理解静态的含义。

function Obj(){

}

Obj.a=0; //静态变量

Obj.fn=function(){ //静态函数

}

console.log(Obj.a); //0
console.log(typeof Obj.fn); //function

var o=new Obj();
console.log(o.a); //undefined
console.log(typeof o.fn); //undefined

## 实例变量、函数

在面向对象编程中除了一些库函数我们还是希望在对象定义的时候同时定义一些属性和方法，实例化后可以访问，JavaScript 也能做到这样

function Obj(){
this.a=[]; //实例变量
this.fn=function(){ //实例方法

}
}

console.log(typeof Obj.a); //undefined
console.log(typeof Obj.fn); //undefined

var o=new Obj();
console.log(typeof o.a); //object
console.log(typeof o.fn); //function
这样可以达到上述目的，然而

function Obj(){
this.a=[]; //实例变量
this.fn=function(){ //实例方法

}
}

var o1=new Obj();
o1.a.push(1);
o1.fn={};
console.log(o1.a); //[1]
console.log(typeof o1.fn); //object
var o2=new Obj();
console.log(o2.a); //[]
console.log(typeof o2.fn); //function
上面的代码运行结果完全符合预期，但同时也说明一个问题，在 o1 中修改了 a 和 fn，而在 o2 中没有改变，由于数组和函数都是对象，是引用类型，这就说明 o1 中的属性和方法与 o2 中的属性与方法虽然同名但却不是一个引用，而是对 Obj 对象定义的属性和方法的一个复制。
这个对属性来说没有什么问题，但是对于方法来说问题就很大了，因为方法都是在做完全一样的功能，但是却又两份复制，如果一个函数对象有上千和实例方法，那么它的每个实例都要保持一份上千个方法的复制，这显然是不科学的，这可肿么办呢，prototype 应运而生。

## prototype

无论什么时候，只要创建了一个新函数，就会根据一组特定的规则为该函数创建一个 prototype 属性，默认情况下 prototype 属性会默认获得一个 constructor(构造函数)属性，这个属性是一个指向 prototype 属性所在函数的指针
当调用构造函数创建一个实例的时候，实例内部将包含一个内部指针（很多浏览器这个指针名字为\_\_proto\_\_）指向构造函数的 prototype，这个连接存在于实例和构造函数的 prototype 之间，而不是实例与构造函数之间。
\_\_proto\_\_是每个对象都有的一个属性，而 prototype 是函数才会有的属性!!!
使用 Object.getPrototypeOf()代替\_\_proto\_\_!!!
对象具有属性\_\_proto\_\_，可称为隐式原型，一个对象的隐式原型指向构造该对象的构造函数的原型，这也保证了实例能够访问在构造函数原型中定义的属性和方法。
一个对象实例通过内部属性[[Prototype]]跟踪其原型对象。可以调用对象的 Object.getPrototypeOf()方法读取[[Prototype]]属性的值,大部分 JavaScript 引擎在所有对象上都支持一个名为\_\_proto\_\_的属性，该属性可以直接读写[[Prototype]]属性。
