# Git几种开发流简介

* [前期准备](#pre)
* [全Master开发](#allmaster)
* [分branch开发](#branch)


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
```test
$ git clone http://172.16.16.34/dwzhan/gittest.git
```

* `git status` 查看当前工作空间的文件状态，用意类似 `svn status`
```test
$ git status
```

* `git add` 把某些修改了的文件加入到要提交的空间，用意类似 `svn changelist`
```test
$ git add README.md
```

* `git commit` 把提交空间的文件提交到仓库, 用意类似 `svn commit`. 区别在于git是提交到本地仓库svn是提交到中心仓库
```test
$ git commit -m "Add test word for read me file"
```

<a name="allmaster"></a>
## 全Master开发

