# autostart
## 一、nx板上的开机自启动
1. 创建开机自启动文件夹：`mkdir ~/.config/autostar`
2. `vim ~/.config/autostart/auto.desktop`

示例内容如下：  
```
[Desktop Entry] 
Encoding=UTF-8
Type=Application  
Categories=true  
Version=1.0  
Name=vnc-server   
Exec=sh /home/drone/auto.sh #注意这里是绝对路径  
Path=/home/yy  
Terminal=false # 是否保留终端  
StartupNotify=true # 开机自启动
```
3. 给desktop文件加上可执行权限：`sudo chmod +x ~/.config/autostart/auto.desktop`  
## 二、ubuntu电脑的开机自启动
1. 写好开机自启动脚本的程序，具体语法见：[shell脚本语法](https://www.runoob.com/linux/linux-shell.html)
2. `cd /etc/systemd/system`
3. `sudo vim auto.service`

示例内容如下：
```
[Unit]
Description =record system reboot time and open clash

[Service]
ExecStart= /home/boyheaven/script/auto_run_script.sh 

[Install]
WantedBy =default.target
```
4. `systemctl daemon-reload`
5. `systemctl enable auto.service`
