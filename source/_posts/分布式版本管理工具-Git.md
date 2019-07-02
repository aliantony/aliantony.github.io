---
title: 分布式项目协作工具-Git
---
Git是一个分布式的源代码管理工具，毋庸置疑它已成为目前企业和个人管理源代码最主流的工具,在GitHub上有很多的开源项目，也是基于Git管理版本。如果你现在还在用Cvs,Svn这类传统的工具，现在你可以尝试Git了，相信Git会给你带来很多工作上的便利。写这篇文章是为了记录Git的基本原理和常用操作，总结一些使用的经验，希望可以帮助到有需要的人。

### 基本原理
![Git原理](/images/git.png)

### 基本概念
- 工作区：新建的文件就在工作区
- 暂存区：通过git add可以把新建的文件添加到暂存区
- 本地仓库: 通过git commit把暂存区的文件提交到本地仓库
- 远程仓库：通过git push把本地仓库的文件推送到远程仓库

### 常用命令整理
1. 在GitHub上创建一个testGit仓库，并复制地址
2. 在本地磁盘建立一个testGit目录
3. 进入testGit目录，右键点击Git Bash Here
4. 执行如下的命令
``` bash
echo "# testGit" >> README.md
git init // 初始化版本库
git add README.md //添加文件
git commit -m "first commit" //提交文件
git remote add origin https://github.com/aliantony/testGit.git //本地仓库和远程仓库建立连接
git push -u origin master //推送本地master分支的提交到远程仓库， -u选项指定origin为默认主机，后面可以直接使用git push命令推送到默认主机
```
