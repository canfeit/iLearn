* [Chrome dev](https://www.google.com/chrome/?hl=zh-CN&extra=devchannel)
* [Git](https://git-scm.com/downloads)
* [NVM](https://github.com/creationix/nvm) [nvm-win](https://github.com/coreybutler/nvm-windows)
* [JDK](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
* [360 Driver.exe](https://dl.360safe.com/drvmgr/360DrvMgrInstaller_beta.exe)
* [lantern-win.exe](https://raw.githubusercontent.com/getlantern/lantern-binaries/master/lantern-installer.exe)
  [lantern-mac.dmg](https://raw.githubusercontent.com/getlantern/lantern-binaries/master/lantern-installer.dmg)
* [TIM](http://office.qq.com/download.html)
* [WeChat](https://weixin.qq.com)
* Ubuntu on Windows in Microsoft Store
```bash
# Windows
nvm node_mirror https://npm.taobao.org/mirrors/node/
nvm npm_mirror https://npm.taobao.org/mirrors/npm/
nvm install latest
# Ubuntu
uname -sr # 查看内核
cat /etc/issue # 查看发行版本
sudo cp /etc/apt/sources.list /etc/apt/sources.list.bak
sudo vi /etc/apt/sources.list

deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-updates main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-backports main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-security main restricted universe multiverse

deb https://mirrors.aliyun.com/ubuntu/ xenial main restricted
deb https://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted
deb https://mirrors.aliyun.com/ubuntu/ xenial universe
deb https://mirrors.aliyun.com/ubuntu/ xenial-updates universe
deb https://mirrors.aliyun.com/ubuntu/ xenial multiverse
deb https://mirrors.aliyun.com/ubuntu/ xenial-updates multiverse
deb https://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse
deb https://mirrors.aliyun.com/ubuntu/ xenial-security main restricted
deb https://mirrors.aliyun.com/ubuntu/ xenial-security universe
deb https://mirrors.aliyun.com/ubuntu/ xenial-security multiverse

deb https://mirrors.163.com/ubuntu/ xenial main restricted universe multiverse
deb https://mirrors.163.com/ubuntu/ xenial-updates main restricted universe multiverse
deb https://mirrors.163.com/ubuntu/ xenial-backports main restricted universe multiverse
deb https://mirrors.163.com/ubuntu/ xenial-security main restricted universe multiverse
# 帮助文档：https://mirrors.tuna.tsinghua.edu.cn/help/ubuntu/
# 帮助文档：https://opsx.alibaba.com/mirror

sudo apt-get update
sudo apt-get upgrade
sudo do-release-upgrade
echo 'export NVM_NODEJS_ORG_MIRROR=https://npm.taobao.org/mirrors/node' >> ~/.bashrc
nvm install node

npm config set registry https://registry.npm.taobao.org
npm i -g yarn
yarn global bin的输出加入path环境变量
yarn global add yarn
npm uninstall -g yarn
yarn global add cnpm
# On Windows
npm install --global --production windows-build-tools
```
* [rustup.exe](https://win.rustup.rs/)
* rustup.sh `curl https://sh.rustup.rs -sSf | sh`
