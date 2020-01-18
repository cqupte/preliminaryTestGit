# git 使用学习

### 文件添加到版本库



1. git add 文件   							放到暂存区
2. git commmit                              提交到仓库
   1. -m   “ 。。。 ”           提交时的注释



注：git log      						  查看历史版本

​		git status  						查看是否被修改

​		git diff 文件名 				  查看具体区别

### 部署到远端

1. 先在找到GitHub上的对应仓库，没有就新建
2. Git remote add origin  https://github.com/cqupte/xxx.git  <---远端的GitHub库的https网址
3. git push -u origin master   





##  Git基本常用命令

mkdir： XX（创建一个空目录XX指目录名）

pwd：  显示当前目录的路径

git init  把当前的目录变成可以管理的git仓库，生成隐藏的.git文件。

git add XX  把XX文件添加到暂存区。

git commit -m “XX” 提交文件 -m后面的是注释

git status 查看仓库状态

git diff XX   查看XX文件修改了哪些内容

git log 查看历史记录

git reset -hard HEAD^ 或者git reset -hard HEAD~ 回退到上一个版本   （如果想回退到100个版本，使用git reset -hard HEAD~100）

cat XX 查看XX文件内容

git reflog  查看历史记录的版本号id

git checkout --XX    把XX文件在工作区的修改全部撤销

git rm XX  删除XX文件

git remote add origin https://github.com/cqupte/xxx.git  关联一个远程库

git push -u （第一次提交要用-u以后不需要）origin master把当前master分支推送到远程库

git clone https://github.com/cqupte/xxx.git   从远程库中克隆

git checkout -b dev 创建dev分支  并切换到dev分支上

git branch  查看当前所有分支

git checkout master 切换回master分支

git merge dev 在当前分支上合并dev分支

git branch -d dev  删除dev分支

git branch name 创建分支

git stash 把当前的工作隐藏起来等以后恢复现场后继续工作

git stash list 查看所有被隐藏的文件列表

git stash apply 恢复被隐藏的文件，但是内容不删除

git stash drop删除文件

git stash pop 恢复文件的同时也删除文件

git remote 查看远程库的信息

git remote -v 查看远程库的详细信息

git push origin master    Git会把master分支推送到远程库对应的远程分支上




