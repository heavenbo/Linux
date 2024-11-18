# 连接本地到github
## 输入自己的用户名和邮箱
 `git config --global user.name "yourname"`  
 `git config --global user.email "youremail@163.com"`  
## 设置SSH key
`ssh-keygen -t rsa -C "youremail@163.com"`  
 `cd ~/.ssh`  
 去对应默认路径里用记事本打开id_rsa.pub，得到ssh key公钥。
 ## 为github账号配置SSH key
  接下来，切换到个人github账号里，点击右上角用户头像下的小三角，找到setting， 
  在右侧菜单栏中找到SSH and GPG keys，选择new SSH key，输入title， 
  下面key的内容就是本机ssh key 公钥，直接将id_rsa.pub中的内容粘贴过来就可以， 
  然后点击下面的add SSH key即可完成.

  ## git clone指定分支
  git clone -b <branchname> <remote-repo-url>
