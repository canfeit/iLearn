```bash
brew services start rethinkdb
echo 'export PATH="/usr/local/opt/sqlite/bin:\$PATH"' >> ~/.bash_profile
export LDFLAGS="-L/usr/local/opt/sqlite/lib"
export CPPFLAGS="-I/usr/local/opt/sqlite/include"
export PKG_CONFIG_PATH="/usr/local/opt/sqlite/lib/pkgconfig"
```

lib/units 每个模块作为一个子进程启动
res/app,angular 前端,components/stf 前端逻辑
pug 页面通过 angular 调用方法发送 websocket
express 端接受 websocket 请求，push.send 消息到 zeromq,zeromq 订阅消息转换为 events 事件消息,监听事件,runAgentCommand/runServiceCommand 与手机通信
