## 路径

- \_\_dirname：当前文件所在目录，模块导入使用的相对路径。electron 打包后文件在 asar 包内，如 app.asar\main.js，app.asar\index.html
- process.execPath：执行文件安装路径
- process.cwd()：执行文件启动路径，child_process.fork，fs 等使用的相对路径。
- process.resourcesPath：electron 应用，资源文件路径

## Web Worker 子线程

- 渲染进程中,有跨域问题

## child_process.fork 子进程

- 主进程和渲染进程中

## 渲染进程中 child_process 和 process 功能似乎不完整，加 remote 调用？

## 通信

- 主进程与渲染进程：异步：ipcMain.on/ipcRenderer.send,webContents.send,webContents.executeJavaScript 同步：remote.require
- 渲染进程间：webContents.send，ipcRenderer.sendTo
- 数据共享：require('electron').remote.getGlobal，Storage API，IndexedDB
