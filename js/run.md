```js
// index.js
const http = require("http");
function startServer() {
  console.log("starting");
  http.createServer((_, res) => res.end("hi")).listen(8000);
  console.log("started");
}
startServer();
```

- `node index`启动一个 node.js 应用
- C++层初始化，node.exe 的入口 src/node_main.cc 的 main 函数
- src/node.cc 的 Start 函数-》LoadEnvironment 函数
- 初始化 process 对象,添加 binding/dlopen 等方法，其余方法见 [Node.js Doc](https://nodejs.org/dist/latest/docs/api/process.html)
- js 层初始化，加载 lib/internal/bootstrap/node.js,传入 process 对象，交给 vm 编译执行其 startup 人口函数
- 将命令行参数传递到 process.argv
- Module_load,使用 fs.read 读取入口文件交给 vm 编译执行
