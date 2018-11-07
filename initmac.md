## Python

- conda 配置

```bash
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --set show_channel_urls yes
conda update conda
```

- 创建 python 环境

```bash
# python2
conda create -n py2 python=2
conda activate py2
python --version
conda deactivate
# python3
conda activate
python --version
conda deactivate
conda info -e
# pipenv 与 conda 不兼容
# pip install pipenv
```

## Node.JS

- 版本管理

```bash
# win
nvm node_mirror https://npm.taobao.org/mirrors/node/
nvm npm_mirror https://npm.taobao.org/mirrors/npm/
nvm install latest
nvm root
# *nix
uname -sr # 查看内核
# 帮助文档：https://mirrors.tuna.tsinghua.edu.cn/help/centos/
# 帮助文档：https://opsx.alibaba.com/mirror
# 帮助文档：https://mirrors.163.com/
curl -L https://git.io/n-install | bash #安装路径:$HOME/n/bin
. ~/.bash_profile
n latest # 安装node latest
n bin latest
n-update # 更新 n
# n-uninstall # 卸载 n
```

- Node.js 配置

```bash
npm config set registry https://registry.npm.taobao.org
npm get prefix #输出加入path环境变量
npm i -g yarn tyarn
yarn config set registry https://registry.npm.taobao.org
tyarn global bin的输出加入path环境变量
tyarn global add cnpm
cnpm get prefix #输出加入path环境变量
tyarn global add node-gyp
node-gyp install --dist-url=https://npm.taobao.org/mirrors/node
```

## Rust

- 配置 rustup 中国镜像源

  ```bash
  # 环境变量
  export RUSTUP_DIST_SERVER=https://mirrors.ustc.edu.cn/rust-static
  export RUSTUP_UPDATE_ROOT=https://mirrors.ustc.edu.cn/rust-static/rustup
  ```

- rustup.sh `curl https://sh.rustup.rs -sSf | sh`
- 配置 Rust Crates 镜像

```
  vi $HOME/.cargo/config

[source.crates-io]
registry = "[https://github.com/rust-lang/crates.io-index](https://github.com/rust-lang/crates.io-index)"
replace-with = 'ustc'
[source.ustc]
registry = "git://mirrors.ustc.edu.cn/crates.io-index"
```

- 添加 nightly

```bash
rustup install nightly
rustup default nightly
rustup update
rustup show
```

```bash
rustup component add rustfmt-preview
```

## 资源下载

- [lantern](https://raw.githubusercontent.com/getlantern/lantern-binaries/master/lantern-installer.dmg)
- [Chrome dev](https://www.google.com/chrome/?hl=zh-CN&extra=devchannel)
- [VS Code](https://code.visualstudio.com/Download)
- [Android Studio](https://developer.android.com/studio/index.html?hl=zh-cn)
- [Android NDK](https://developer.android.com/ndk/downloads/index.html)
- [IntelliJ IDEA](https://www.jetbrains.com/idea/download/)
- [Python](https://mirrors.tuna.tsinghua.edu.cn/anaconda/miniconda/?C=M&O=D)
- [TIM](http://office.qq.com/download.html)
- [WeChat](https://weixin.qq.com)
- [MiCloud](https://i.mi.com/static2?filename=MicloudWebStatic/res/home/mi-lab.htm&locale=zh_CN#3)
- [JDK](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
- [LLVM-Clang](http://releases.llvm.org/download.html)
- gradle: `brew install gradle`

## ~/.bash_profile

```bash
export PATH="/miniconda3/bin:$PATH"
export PATH="/mongodb/bin:$PATH"
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
alias proxy="export http_proxy=http://127.0.0.1:52029&&export https_proxy=http://127.0.0.1:52029"
```
