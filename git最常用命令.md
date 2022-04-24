# git最常用命令

## 一般流程：本地库前期准备，add，commit，push

### 本地库

git init 初始化仓库

git remote add tag remoteRepo  远程库起别名

### 暂存区

git add xxx 添加文件到暂存区

#### 版本控制（

git reflog 查看commit的日志

git reset --hard 版本id  切换版本

git commit -m "log message" file 提交文件到本地库

git push 

## 特殊流程：分支管理，与远程库互动,版本控制

### 分支管理

#### 增删改查

git branch hot-fix  （该分支会备份一份主分支）（刚刚初始化的空master不能创建分支）

git branch -v 查看分支

#### 分支合并互动（把你的新业务链并到主master业务上）

git checkout hot-fix 切换分支，此时进入到子分支拓展业务或者完善代码

（此处在子分支修改完内容，假设改了hello.txt)

git add hello.txt 添加到暂存区

git commit -m "" hello.txt 提交本地库

git reset --soft 版本号   撤回commit

(此处在子分支上完善了一下hello.txt的代码，想合并到主线上)

**git checkout master**(这步很关键，要在主分支上进行子分支合并)

**git merge hot-fix** 合并子分支（有关冲突的介绍自行百度）

#### 本地分支推送到远程指定分支(流程)

git add ./(不知道有啥用，创建目录？)

git add txt

git commit -m "" txt

git push  远程库别名 本地分支：远程想推到的分支

本地分支添加删除

远程分支添加删除

本地分支推送

## 个人想实现的功能

在本地完成

git reset --hard 版本号  版本穿梭

## 辅助命令

# git使用总结

## 日常常用命令

git init 

git remote -v 查看所有远程库(github)别名

git remote add jvc httpsxxxxxx.  起别名

git (ref)log

git reset --hard xxx  版本切换

git branch -v  当前分支

git branch xxx  新增分支

git checkout xxx 切换分支

git merge xxx(在当前yyy上将xxx合并进来)(冲突问题删除特殊符号然后留下内容)

git clone httpxxxx

git pull 远程库别名 远程分支名 与本地当前分支合并

git add xxx   添加到暂存区

git commit -m "xxx"  提交到本地库

git push 别名 master    推送本地master分支到远程库