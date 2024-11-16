# Realsense及realsense-ros的安装与使用

## 1 安装 librealsense

详细使用文档见 [librealsense](https://github.com/IntelRealSense/librealsense)  
建议安装librealsense-V2.48.0,  高版本可能有未知bug。 安装有两种方式，一种是使用apt-get自动安装，另一种是手动编译安装。建议使用手动安装，已知自动安装会出现rules冲突bug。

### 手动安装

首先在[Release](https://github.com/IntelRealSense/librealsense/releases)中找到对应版本
然后在Assets中下载所需的压缩包,在文件下载处，打开终端
```
  tar -zxvf librealsense-2.48.0.tar.gz
```
cd 到解压后的根目录下，打开终端,安装依赖
```
  sudo apt-get update && sudo apt-get upgrade && sudo apt-get dist-upgrade  
  sudo apt-get install git libssl-dev libusb-1.0-0-dev libudev-dev pkg-config libgtk-3-dev
```
执行rules设置脚本和kernel设置
```
  ./scripts/setup_udev_rules.sh
  #如果你的ubuntu是LTS版本的，请执行这句话
  ./scripts/patch-realsense-ubuntu-lts.sh
  #如果你的cpu是arm64架构，请执行这句话
  #./scripts/patch-ubuntu-kernel-4.16.sh
```
之后，开始编译源文件
```
  mkdir build && cd build
  cmake ../ -DCMAKE_BUILD_TYPE=Release
  make -jx #x是你编译要使用的核心数，可以填4或8
  sudo make install
```
安装完成，打开终端，运行`realsense-viewer`检验是否安装成功。  
**tips:** 安装好的包在`/usr/local/lib`中，头文件在`/usr/local/include`

## 2 安装 realsense-ros
同样地，在[ros-release](https://github.com/IntelRealSense/realsense-ros/releases)中找到对应的版本，**注意：一定要是ros而不是ros2** 。下载后解压。  
下面新建一个ros工作空间并使用catkin编译和安装
```
  mkdir -p ~/ros_ws/src && cd ~/ros_ws/src
  mv "你下载的解压后的文件地址" ~/ros_ws/src
  catkin_init_workspace
  cd ..
  catkin_make clean
  catkin_make -DCATKIN_ENABLE_TESTING=False -DCMAKE_BUILD_TYPE=Release
  catkin_make install
```
将你新建的工作空间加入进环境变量
```
  echo "source ~/ros_ws/devel/setup.bash" >> ~/.bashrc
  source ~/.bashrc
```
使用`roslaunch realsense2_camera rs_t265.launch`检验是否安装成功
source devel/setup.bash
rosrun topic_tools throttle messages /camera/fisheye1/image_raw 4.0 /fisheye1 && rosrun topic_tools throttle messages /camera/fisheye2/image_raw 4.0 /fisheye2
