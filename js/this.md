this:当前执行上下文环境
它可以在函数调用时修改，在函数没有调用的时候，this 的值是无法确定。
在全局执行环境中 this 指向(window/global/module.exports)
如果是 obj.func()这一类型的，那么就是方法调用，如果是 func()这一类型的那么就是函数调用，在方法调用中，this 就是 obj 本身的引用，如果是函数调用，情况就复杂了，

1. 浏览器
   - 严格模式下：undefined
   - 非严格模式下:window
2. Node.js REPL
   - 严格模式下：undefined
   - 非严格模式下:global
3. Node.js 模块
   - 函数内部
     - 严格模式下：undefined
     - 非严格模式下: global
   - 全局代码
     - module.exports

在事件处理器和一些核心模块的回调函数中,node.js 使用 call 给回调函数绑定了 this,这与浏览器中不同

.bind() 创建了一个永恒的上下文链并不可修改。一个绑定函数即使使用 .call() 或者 .apply()传入其他不同的上下文环境，也不会更改它之前连接的上下文环境，重新绑定也不会起任何作用。只有在 new 构造器调用时，可以改变上下文

箭头函数拥有静态的上下文环境，不会因为不同的调用而改变，即使使用.call() 或者 .apply()上下文更改的方法。普通函数可以改变调用时的上下文环境

```js
const events = require("events");
g = "global"; //global 全局变量在模块间共享
exports.m = "module.exports";
console.log("全局", this); //module.exports
(function() {
  console.log("全局函数", Object.prototype.toString.call(this), this.g); //global
})();
(() => {
  console.log("全局箭头函数", this); //module.exports
})();
const channel = new events.EventEmitter();
channel.on("join", function() {
  console.log("事件处理函数", this.constructor.name); //EventEmitter
});
channel.on("leave", () => {
  console.log("事件处理箭头函数", this); //module.exports
});
require("http").get("http://so.com", function() {
  console.log("http回调函数", this.constructor.name); //ClientRequest
});
require("http").get("http://so.com", () => {
  console.log("回调箭头函数", this); //module.exports
});
setTimeout(function() {
  console.log("setTimeout回调", this.constructor.name); //Timeout
});
require("fs").readFile(__filename, function() {
  console.log("fs回调", Object.prototype.toString.call(this)); //global
});
class Planet {
  info() {
    console.log(this.constructor.name);
  }
}
var earth = new Planet("Earth");
earth.info(); //Planet
setTimeout(earth.info); //Timeout,对象方法作为函数参数传入setTimeout
channel.emit("join");
channel.emit("leave");
```
