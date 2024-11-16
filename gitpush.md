# 一、初次创建操作（只有第一次需要）
## 1.1连接账户
首先参照[git](https://github.com/heavenbo/Linux/blob/main/git.md)进行操作
## 1.2创建项目
在github中创建一个项目(带README.md),然后复制其ssh或者是https（一种失败可以换另外一种）
## 1.3创建本地文件夹
`cd 目标文件夹`  
`git init`  
## 1.4添加远程
`git remote add origin 复制的ssh`
## 1.5创建本地仓库分支并转移到其中
`git checkout -b main`
## 1.6快速拉取
`git pull`
## 1.7合并远程分支和本地分支
`git merge origin/main`，成功后应该可以看到文件夹里多了README.md。
# 二、后续操作
## 2.1上传本地文件
`git add` 目标文件（一般为`git add . `意为上传该文件夹所有内容）
`git commit -m "标注这次的修改"`  
`git push`  
初次上传使用`git push --set-upstream origin main`
## 2.2拉取文件
`git pull`

如果拉取文件没有变化，再使用`git merge origin/main`
