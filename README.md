# Git几种开发流简介

* [前期准备](#pre)
* [全Master开发](#allmaster)
* [分branch开发](#branch)
* [fork社会化开发](#fork)


<a name="pre"></a>
## 前期准备
先熟悉git几个核心命令

* `git config` 是用来配置git一些设置的，例如肯定需要配置的当前用户名和对应的email
```shell
$ git config --global user.name "dwzhan"
$ git config --global user.email "dwzhan@iflytek.com"
$ git config --list --global
```

* `git clone` git 克隆一个仓库出来，用意类似 `svn checkout`
```shell
$ git clone http://172.16.16.34/dwzhan/gittest.git
```

* `git status` 查看当前工作空间的文件状态，用意类似 `svn status`
```shell
$ git status
```

* `git add` 把某些修改了的文件加入到要提交的空间，用意类似 `svn changelist`
```shell
$ git add README.md
```

* `git commit` 把提交空间的文件提交到仓库, 用意类似 `svn commit`. 区别在于git是提交到本地仓库svn是提交到中心仓库
```shell
$ git commit -m "Add test word for read me file"
```

<a name="allmaster"></a>
## 全Master开发

全Matster开发意味着队伍里的人都在master branch上面提交代码，这样git的使用和svn上的trunk很类似了。下面是一个例子：
Dev 1
```shell
$ echo "this is commit 1" >> test.txt
$ git add test.txt
$ git commit -m "commit 1"
$ git push
```
Dev 2
```shell
$ echo "this is commit 2" >> test.txt
$ git commit -m "commit 2"
$ git pull
$ git push
```
Dev 1
```shell
$ git pull
```

<a name="branch"></a>
## 分branch开发
