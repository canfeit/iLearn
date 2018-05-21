## 路径
* __dirname：当前文件所在目录，模块导入使用的相对路径。electron 打包后文件在asar包内，如app.asar\main.js，app.asar\index.html
* process.execPath：执行文件安装路径
* process.cwd()：执行文件启动路径，child_process.fork，fs等使用的相对路径。
* process.resourcesPath：electron应用，资源文件路径
## Web Worker子线程
* 渲染进程中,有跨域问题
## child_process.fork子进程
* 主进程和渲染进程中
