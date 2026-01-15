# Linux安装VPN
1.按照windows系统新建一个文件夹clash

2.进入网址https://ppv2.cc 找到Linux使用教程下载客户端，下载文件**clash-linux-amd64-v3-v1.10.0.gz**

3.在文件管理器找到下载文件，使用ctr+C和ctr+v将下载文件转移至clash文件夹

4.打开clash文件夹，鼠标右键选择‘在终端打开’。

5.执行命令`gzip -d clash-linux-amd64-v3-v1.10.0.gz`，解压文件

6.再执行：`mv clash-linux-amd64-v3-v1.10.0 clash`，进行重命名。（在Linux中ctr+c与ctr+v复制粘贴功能只在文件管理器中有用，在终端中只能运用鼠标右键进行复制粘贴）

7.复制指令`wget -O config.yaml https://ppv2.cc/link/XkrbmwzF1W9mNk4x?clash=1`

8.执行指令：`chmod +x clash`

9.再执行指令：`./clash -d .` 会出现如图画面即可
          <img width="705" alt="图片1" src=photo\clash.png>

   **注：这一步后可以按ctr+c调出命令行**
   
10.打开电脑设置，选择网络，这一步参照Linux使用教程的步骤五即可

11.之后点击网页的Linux使用教程的步骤四的 Clash Dashboard 

12.进行切换节点、测延迟等操作。

**注意事项**：在以后开机使用VPN后都要使用./clash -d .命令打开程序。并且不能关闭此终端。（可以另起一个终端页面实行其他命令）
