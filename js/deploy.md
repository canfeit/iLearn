Nginx

作用

Nginx 作为静态资源服务器和反向代理服务器,用于处理静态资源,实现静态资源缓存与压缩,使页面首次加载时间缩短 70%左右.

部署

安装

将项目包及运行环境上传至服务器.

rpm 方式: > rpm -ivh nginx-\*

yum 方式: > yum install nginx

配置

使用项目目录下 nginx.conf 替换原/etc/nginx/nginx.conf(替换前需先备份),需修改其中 upstream backend 的 server IP 及静态资源路径.

启动:> nginx

特性

Nginx epoll 与非阻塞异步 IO 模型提高静态资源响应效率;

Sendfile 零拷贝系统调用加快文件读取操作;

Gzip 支持静态资源压缩率达 70%以上;

反向代理与高效的请求转发功能可实现分布式高可用架构

Nodejs

作用

用于提供 web 服务,进行数据库操作,提供 Restful 接口,实现模型及看板组件管理

部署

安装

将项目包及运行环境上传至服务器.

手动安装:

Zip 版解压: > unzip node-\* -d node

Tgz 版解压: > tar -zxf node-v7.10.0-linux-x64.tar.gz

将其 bin 目录加入系统 path 环境变量.

安装 pm2

Npm 方式: > npm i –g pm2

手动安装:

将 pm2.tar.gz 解压到 node 的 lib/node_modules 目录:

> tar -zxf pm2.tar.gz

进入 node 的 bin 目录,执行:

> ln -s ../lib/node_modules/pm2/bin/pm2 pm2

添加系统环境变量:

export NODE_ENV=production

在建模项目目录下执行:

> pm2 restart pm2.json --update-env

> pm2 startup

> pm2 save

特性

Node.js 是服务端 javascript 引擎,基于 V8,使用异步非阻塞 IO 模型,性能出众;

开发部署简单学习成本低,可快速开发产品原型并迅速迭代,可节约大量时间和人力成本;

由 Node.js 基金会维护,生态系统活跃,在国内外各大互联网公司均有应用,是一套成熟稳定的互联网产品解决方案.

Nginx 维护

停止:nginx –s stop

启动:nginx

重载配置: nginx –s reload

重启:nginx –s stop&&nginx

Node 维护

停止:pm2 stop server

启动:pm2 start server

重启:pm2 restart server --update-env

找不到 npm:ln -s ../lib/node_modules/npm/bin/npm-cli.js npm

Node 权限不足:chmod –R 655 node 的 bin 目录
