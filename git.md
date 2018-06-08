# git

## commit 规范

```text
<type>:空格<subject>
// 空一行
<body>
// 空一行
<footer>
```

### type

```text
feat: 新功能（feature）,该 commit 将出现在 Change log 之中
fix: 修补bug,该 commit 将出现在 Change log 之中
docs: 文档（documentation）
style: 格式（不影响代码运行的变动）
refactor: 重构（即不是新增功能，也不是修改bug的代码变动）
test: 增加测试
chore: 构建过程或辅助工具的变动
```

### subject

```text
commit 的简短描述，不超过50个字符。
以动词开头，使用第一人称现在时，比如change，而不是changed或changes
第一个字母小写
结尾不加句号（.）
```

### body

commit 的详细描述，可以分成多行。

### footer

只用于两种情况。

```text
1.不兼容变动:如果当前代码与上一个版本不兼容，则 Footer 部分以BREAKING CHANGE开头，后面是对变动的描述、以及变动理由和迁移方法。
2.关联或关闭 Issue:如果当前 commit 针对某个issue，那么可以在 Footer 部分关闭这个 issue 。
fix #123, #245, #992
Issue #1, #2, #3
```

## Git 操作

* Merge&Pull requests

  ```bash
  # fork
  # clone fork到自己的仓库
  git clone https://github.com/canfeit/pms.git
  # 编辑修改本地仓库
  cd pms
  # 提交本地修改到github
  git add .&&git commit -m "Merge remote-tracking branch 'upstream/master'"&&git push
  # 添加源仓库
  git remote add upstream https://github.com/DXC/pms.git
  # 修改源仓库地址
  git remote set-url upstream https://github.com/DXCChina/pms.git
  # 删除源仓库
  # git remote rm <repository>
  # 查看远程仓库地址
  git remote -v
  # 从 upstream 源仓库获取更新
  git fetch upstream
  # 查看所有分支列表
  git branch -a
  # 合并源仓库更新
  git merge --no-ff upstream/master
  # 向源仓库推送更新:在 github.com 发起 pull request
  ```

* 删除本地分支 `git branch -D 分支名`
* 删除远程分支 `git push origin :分支名`
* 撤销所有未暂存修改 `git checkout .`
* 撤销所有已暂存修改 `git reset --hard`
* 清理未被git管理的文件 `git clean -xdf`
* Release

  ```bash
  git tag -a v1 -m 'version 1'
  git push origin --tags
  ```

* 删除标签

  ```bash
  git tag -d $(git tag)
  git push origin --delete tag v1
  ```

* 子仓库
 ```bash
 # 添加子模块
 git submodule add git@github.com:canfeit/appium-uiautomator2-server.git static/uiautomator2
 git submodule add git@github.com:canfeit/minicap.git static/minicap
 git submodule add git@github.com:canfeit/minitouch.git static/minitouch
 # clone 仓库，包含子模块
 git clone --recursive git@github.com:canfeit/testwa.git
 # 等同于
 git clone git@github.com:canfeit/testwa.git
 git submodule update --init --recursive
 # 更新子模块
 git submodule update --remote --recursive --merge
 git push --recurse-submodules=on-demand
 ```
