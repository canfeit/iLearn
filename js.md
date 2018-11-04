## Node.js 交流学习

### 第一天

- Node.js 介绍与开发环境搭建
- 常用开发工具的使用:Yarn/NPM,VS Code,Git/GitHub 等
- Node.js 基础及相关概念介绍
- Node.js Package 创建与发布

### 第二天

- Node.js 常用接口介绍和使用:fs/net 等
- Node.js 常用 Package 介绍和使用

### 第三天

- Web 开发框架 Koa2 相关概念介绍
- 简单 Web 项目开发
- 使用 Node.js 进行数据库操作

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

### Web Worker 子线程

- 渲染进程中,有跨域问题

### child_process.fork 子进程

- 主进程和渲染进程中

### 渲染进程中 child_process 和 process 功能似乎不完整，加 remote 调用？

##TODO

- 变量对象/活动对象/作用域链/原型链/闭包/this/上下文
