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

创建分支：git branch <name>

切换分支：git checkout <name>

创建+切换分支：git checkout -b <name>

合并某分支到当前分支：git merge <name>

删除分支：git branch -d <name>

> Git支持多种协议，默认的git://使用ssh，但也可以使用https等其他协议。
> //git@github.com:hardyio/learngit.git
> //https://github.com/hardyio/learngit.git

