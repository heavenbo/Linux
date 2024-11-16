# 操作
首先参照[git](https://github.com/heavenbo/Linux/blob/main/git.md)进行操作
# 创建项目
在github中创建一个项目(带README.md),然后复制其ssh或者是https（一种失败可以换另外一种）
# 创建本地文件夹
`cd 目标文件夹`  
`git init`  
# 添加远程
git remote add origin 复制的ssh
# 快速拉取
git fetch origin
# 合并远程分支和本地分支
git merge origin/main，成功后应该可以看到文件夹里多了README.md。

# 上传本地文件
`git add 目标文件（一般为git add . 意为上传该文件夹所有内容）`  
`git commit -m "标注这次的修改"`  
`git push`  
# 拉取文件
git pull:即为拉取文件到对应本地仓库
