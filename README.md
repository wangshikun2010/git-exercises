git常用命令简介
==============

git配置
-------

#### 设置姓名和邮箱

	git config --global user.name "名字"
	git config --global user.email "邮箱"

#### 设置换行符
	git config --global core.autocrlf true
	git config --global core.safecrlf true

#### 初始化一个git库
	mkdir dir
	cd dir
	git init

#### 将文件添加到库
	git add file
	git commit -m 'commit message'

#### 将本地的test分支追加到远程的master分支上面
	git push origin

#### 查看文件当前状态
	git status

#### 取消文件修改的跟踪
	git reset

查看提交历史
------------

#### 查看所有提交历史
	git log

#### 查看单行历史
	git log --pretty=oneline

#### 查看指定用户提交记录
	git log --pretty=oneline --author='username'

设置别名，HOME目录下的.gitconfig
--------
	[alias]
  	co = checkout
  	ci = commit
  	st = status
  	br = branch
  	hist = log --pretty=format:\"%h %ad | %s%d [%an]\" --graph --date=short
  	type = cat-file -t
  	dump = cat-file -p

checkout
--------

#### checkout指定提交
	git hist
	git checkout <hast>
	cat file

#### checkout主分支的最新版本
	git checkout master
	cat file

#### 查看文件
	cat file

在撤销前，未添加之前撤销本地的修改
---------------------------------
	git checkout master
	git status
	git checkout file
	git status
	cat file

在提交之前，恢复已跟踪的更改
----------------------------
	git status
	git add file
	git status
	git reset 或者 git reset HEAD file
	git checkout file
	git status