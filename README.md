git常用命令简介
==============

git配置
-------

###设置姓名和邮箱
git config --global user.name "名字"
git config --global user.email "邮箱"

###设置换行符
git config --global core.autocrlf true
git config --global core.safecrlf true

###初始化一个git库
mkdir dir
cd dir
git init

###将文件添加到库
git add file
git commit -m 'commit message'

###查看文件当前状态
git status

###取消文件修改的跟踪
git reset

查看提交历史
------------

###查看所有提交历史
git log

###查看单行历史
git log --pretty=oneline

###查看指定用户提交记录
git log --pretty=oneline --author='username'



