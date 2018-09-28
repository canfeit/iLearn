# initpc

## 资源下载

* [lantern-win.exe](https://raw.githubusercontent.com/getlantern/lantern-binaries/master/lantern-installer.exe)

  [lantern-mac.dmg](https://raw.githubusercontent.com/getlantern/lantern-binaries/master/lantern-installer.dmg)

* [Chrome dev](https://www.google.com/chrome/?hl=zh-CN&extra=devchannel)
* [Android Studio](https://developer.android.com/studio/index.html?hl=zh-cn)
* [Android NDK](https://developer.android.com/ndk/downloads/index.html)
* [Visual Studio](https://www.visualstudio.com/zh-hans/thank-you-downloading-visual-studio/?sku=Community)
* [VS Code](https://code.visualstudio.com/Download)
* [IntelliJ IDEA](https://www.jetbrains.com/idea/download/)
* [Python](https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/)
* NVM:`curl -L https://git.io/n-install | bash` [nvm-win](https://github.com/coreybutler/nvm-windows)
* [TIM](http://office.qq.com/download.html)
* [WeChat](https://weixin.qq.com)
* [MiCloud](https://i.mi.com/static2?filename=MicloudWebStatic/res/home/mi-lab.htm&locale=zh_CN#3)
* [WinSCP](https://winscp.net/eng/download.php)
* [PuTTY](https://winscp.net/eng/downloads.php#putty)
* Ubuntu on Windows in Microsoft Store
* [JDK](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
* [win10+/360 Driver.exe](https://dl.360safe.com/drvmgr/360DrvMgrInstaller_beta.exe)
* [Git](https://git-scm.com/downloads)
* [LLVM-Clang](http://releases.llvm.org/download.html)
* [Visual C++ Build Tools](https://www.microsoft.com/zh-CN/download/details.aspx?id=48159)
## android-ndk
* on mac
```bash
echo 'export PATH="/Users/wuwei/android-ndk:$PATH"' >>~/.bash_profile
brew install gradle
```
```bash
# added by Miniconda3 4.5.11 installer
export PATH="/miniconda3/bin:$PATH"
export PATH="/android-ndk:$PATH"
export ANDROID_HOME=/Users/$(whoami)/Library/Android/sdk
export RUSTUP_DIST_SERVER=https://mirrors.ustc.edu.cn/rust-static
export RUSTUP_UPDATE_ROOT=https://mirrors.ustc.edu.cn/rust-static/rustup
export PATH="$ANDROID_HOME:$ANDROID_HOME/build-tools/28.0.3:$ANDROID_HOME/platform-tools:$ANDROID_HOME/tools/bin:$PATH"
export PATH="$HOME/.cargo/bin:$PATH"
export JAVA_7_HOME=`/usr/libexec/java_home -v 1.7` 
export JAVA_8_HOME=`/usr/libexec/java_home -v 1.8` 
export JAVA_10_HOME=`/usr/libexec/java_home -v 10` 
export JAVA_HOME=$JAVA_10_HOME 
alias jdk7="export JAVA_HOME=$JAVA_7_HOME" 
alias jdk8="export JAVA_HOME=$JAVA_8_HOME" 
alias py2="conda activate py2"
alias py3="conda activate"
alias code="\code-insiders .||\code ."
alias proxy="export http_proxy=http://127.0.0.1:54818&&export https_proxy=http://127.0.0.1:54818"
export GH_TOKEN=6dd0b530aee381409756cf6c47234659d0abd2fb
export github_clientId=d7b249385469cd9d91a1
export github_secret=6d3b839368ff06b9d1167b8ed394e61c69b284a7
# export TESTWA_PORTAL_URL=http://192.168.0.143:8008/agent/client

```
* on linux
```bash
echo 'export PATH="/Users/wuwei/android-ndk:$PATH"' >>~/.bashrc
```
## Python

```bash
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --set show_channel_urls yes
conda update conda
# 创建python环境
conda create -n py2 python=2
conda activate py2
python --version
conda deactivate

conda create -n py3 python=3
conda activate py3
python --version
conda deactivate
conda info -e
# pipenv与conda不兼容
pip install pipenv
```

## Node.JS

```bash
# Windows
nvm node_mirror https://npm.taobao.org/mirrors/node/
nvm npm_mirror https://npm.taobao.org/mirrors/npm/
nvm install latest
# npm --add-python-to-path --python_mirror=https://npm.taobao.org/mirrors/python/ --vs2017 install --global --production windows-build-tools
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
# Node.js 配置
npm config set registry https://registry.npm.taobao.org
npm i -g tyarn
tyarn global bin的输出加入path环境变量
tyarn global add tyarn
npm uninstall -g tyarn
tyarn global add cnpm
tyarn global add node-gyp
node-gyp install --dist-url=https://npm.taobao.org/mirrors/node
```

## Rust

* 配置 rustup 中国镜像源

  ```bash
  # 环境变量
  export RUSTUP_DIST_SERVER=https://mirrors.ustc.edu.cn/rust-static
  export RUSTUP_UPDATE_ROOT=https://mirrors.ustc.edu.cn/rust-static/rustup
  ```

* [rustup.exe](https://win.rustup.rs/)
* rustup.sh `curl https://sh.rustup.rs -sSf | sh`
* 配置 Rust Crates 镜像
```
  vi $HOME/.cargo/config

[source.crates-io]
registry = "[https://github.com/rust-lang/crates.io-index](https://github.com/rust-lang/crates.io-index)"
replace-with = 'ustc'
[source.ustc]
registry = "git://mirrors.ustc.edu.cn/crates.io-index"
```
* 添加 nightly
```bash
rustup install nightly
rustup default nightly
rustup update
rustup show
```

```bash
rustup component add rustfmt-preview
```

