# Linux 安装指南
## 一、安装双系统（win10与Linux）
### 1.准备工作
#### 1.1查看BIOS模式
使用“win+R”快捷键打开运行，输入“msinfo32”打开系统信息，查看BIOS模式，只支持模式为UEFI的电脑。
#### 1.2准备一个4G及以上的U盘
      
U盘用于安装系统，会被格式化。
#### 1.3下载镜像文件
   
我下载的是ubuntu linux 20.04（官网下载），文件大小大约为3GB
#### 1.4下载软件‘软碟通’
之后操作按照下列网站操作即可：https://blog.csdn.net/qq_43106321/article/details/105361644?utm_source=app&app_version=5.3.0&code=app_1562916241&uLinkId=usr1mkqgl919blen
或在CSDN搜索：Windows 10 安装ubuntu 18.04 双系统（超详细教程）
完全按照其操作即可，无注意事项。

## 二、利用虚拟机运行Linux（但是我的电脑运行非常卡）
操作完全按照以下网址操作即可：https://blog.csdn.net/qq_43015237/article/details/109234454?utm_source=app&app_version=5.3.0&code=app_1562916241&uLinkId=usr1mkqgl919blen

或在CSDN搜索名称：虚拟机VMware和Ubuntu的安装与配置教程（超详细，实验可行）

虚拟机下载教程看这个视频：VMware16虚拟机安装激活使用一条龙保姆级详细教程_哔哩哔哩_bilibili。
下载的安装包如果找不到,可以找我要安装包，可以QQ发，也可以用U盘。
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
          <img width="705" alt="图片1" src="https://user-images.githubusercontent.com/102459021/161947290-0c679de2-73e1-4cb7-90d1-87656e8cf2e1.png">

   **注：这一步后可以按ctr+c调出命令行**
   
10.打开电脑设置，选择网络，这一步参照Linux使用教程的步骤五即可

11.之后点击网页的Linux使用教程的步骤四的 Clash Dashboard 

12.进行切换节点、测延迟等操作。

**注意事项**：在以后开机使用VPN后都要使用./clash -d .命令打开程序。并且不能关闭此终端。（可以另起一个终端页面实行其他命令）
