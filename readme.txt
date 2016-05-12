$ mkdir learngit
$ cd learngit
$ pwd//创建版本库:
$ git init//把这个目录变成Git可以管理的仓库:

$ git add readme.txt//把文件添加到缓冲区：
$ git commit -m "wrote a readme file”//把文件提交到仓库：

$ git status//让我们时刻掌握仓库当前的状态：
$ git diff readme.txt //查看difference
$ git log//显示从最近到最远的提交日志
$ git reflog//记录每一次命令

$ git reset --hard HEAD^//回退到上一个版本

$ git checkout -- readme.txt//当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时
$ git reset HEAD readme.txt//已经提交到缓冲区时，回到了上一步之前的状态
$ rm test.txt//删除文件
$ git rm test.txt//确实需要删除时，从版本库中删掉
$ git checkout -- test.txt//错删时，把误删的文件恢复到最新版本（用版本库里的版本替换工作区的版本）

$ ssh-keygen -t rsa -C "youremail@example.com”//创建SSH Key

$ git remote rm origin//解决办法：fatal: remote origin already exists.
$ git remote add origin git@github.com:tianyayuan/learngit.git//本地关联远程库
$ git push -u origin master
//由于远程库是空的，我们第一次推送master分支时，加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。
$ git push origin master//把本地master分支的最新修改推送至GitHub
$ git clone git@github.com:tianyayuan/gitskills.git//从远程到本地

$ git checkout -b dev//创建dev分支，然后切换到dev分支
$ git branch//查看当前分支
$ git checkout master//切回master分支
$ git merge dev//用于合并指定分支到当前分支
$ git branch -d dev//删除dev分支

$ git log --graph --pretty=oneline --abbrev-commit//可以看到分支的合并情况
$ git merge --no-ff -m "merge with no-ff" dev
//本次合并要创建一个新的commit,从分支历史上就可以看出分支信息。










