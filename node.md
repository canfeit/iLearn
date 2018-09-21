## node

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
