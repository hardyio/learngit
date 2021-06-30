## 一个在线可视化交互学习 Git 网站，帮助快速理解 Git 操作流程。 ##
项目地址：[https://github.com/pcottle/learnGitBranching](https://github.com/pcottle/learnGitBranching)

在线体验：[https://learngitbranching.js.org/?demo](https://learngitbranching.js.org/?demo)

## 笔记 ##
…or create a new repository on the command line
(```)
git init
git add README.md
git commit -m "first commit"
git branch -M master
git remote add origin https://github.com/hardyio/test.git
git push -u origin master
(```)
…or push an existing repository from the command line
(```)
git remote add origin https://github.com/hardyio/test.git
git branch -M master
git push -u origin master
(```)
##### 安装完成后，还需要最后一步设置，在命令行输入：

* $ git config --global user.name "Your Name"
* $ git config --global user.email "email@example.com"

##### 创建一个版本库
1.创建一个空目录

* $ mkdir learngit
* $ cd learngit
* $ pwd
> /Users/michael/learngit

2.把这个目录变成Git可以管理的仓库

* $ git init
> Initialized empty Git repository in /Users/michael/learngit/.git/

##### 把文件添加到仓库

* $ git add readme.txt

##### 把文件提交到仓库
* $ git commit -m "wrote a readme file"
 
> [master (root-commit) cb926e7] wrote a readme file
> 
> 1 file changed, 2 insertions(+)
> 
> create mode 100644 readme.txt

##### git status 可以让我们时刻掌握仓库当前的状态
$ git status

##### 查看difference
$ git diff helloworld.txt

##### 命令查看--输出信息太多
$ git log

##### 简版查询
$ git log --pretty=oneline

##### 回退版本 在版本的历史之间穿梭
$ git reset --hard 3628164

##### 后悔药 记录你的每一次命令：
$ git reflog

##### 丢弃工作区的修改

$ git checkout -- readme.txt

##### 把暂存区的修改撤销掉（unstage），重新放回工作区

$ git reset HEAD readme.txt

##### 删除文件

$ git rm test.txt

##### 关联一个远程库
$ git remote add origin https://github.com/hardyio/learngit.git
##### 第一次推送master分支的所有内容

$ git push -u origin master

##### 克隆到本地库

$ git clone https://github.com/hardyio/learngit.git

##### 查看远程库信息
$ git remote -v

##### Git鼓励大量使用分支：

查看分支：git branch

创建分支：git branch \<name>

切换分支：git checkout \<name>

创建+切换分支：git checkout -b \<name>

合并指定分支到当前分支：git merge \<name>

删除分支：git branch -d \<name>

##### 创建远程分支：

1、在当前分支下创建dev的本地分支：git checkout -b dev

2、将dev分支推送到远程：git push origin dev

3、将本地分支dev关联到远程分支dev上：git branch --set-upstream-to=origin/dev

查看本地各个分支目前最新的提交：git branch -v

查看远程分支：git branch -r

查看远程各个分支目前最新的提交：git branch -r -v

查看本地分支和远程分支的映射关系：git branch -vv


> Git支持多种协议，默认的git://使用ssh，但也可以使用https(速度较慢,每次推送都必须输入口令)等其他协议。
>
> //git@github.com:hardyio/learngit.git
>
> //https://github.com/hardyio/learngit.git

##### TAG

列显已有的标签：git tag

轻量级标签：git tag v1.0.0 -m 'release v1.0.0'

打标签并添加说明：git tag -a v1.0.0 -m 'release v1.0.0'

将标签提交到远程仓库：git push origin v1.0.0

本地删除tag：git tag -d v1.0.0

远程库删除tag：git push origin :refs/tags/v1.0.0

##### 删除不想要的远程仓库提交

git reset commitId （注：不要带–hard）到上个版本

git stash 暂存修改

git push --force 强制push，远程的最新的一次commit被删除

git stash pop 释放暂存的修改，开始修改代码

git add . -> git commit -m "massage" -> git push
