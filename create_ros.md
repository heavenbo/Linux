# How to create a ros package
## 1.Create a ROS Workspace:
* `mkdir -p ~/<package_name1>/src` 
* `cd ~/<package_name1>/`
* `catkin_make`
* `source devel/setup.bash`
* `echo $ROS_PACKAGE_PATH #check`#
## 2.Creating a catkin Package
* `cd ~/<package_name1>/src`
* `catkin_create_pkg <package_name2> [depend1] [depend2] [depend3] #std_msgs rospy roscpp`
## 3.Building a catkin workspace and sourcing the setup file
* `cd ~/package_name1` `catkin_make`
* To add the workspace to your ROS environment you need to source the generated setup file: `. ~/package_name1/devel/setup.bash`
## 4.Customizing Your Package
* write package.xml(still to learn)
## 5.create msg and srv
### 5.1 Introduction to msg and srv
* msg: msg files are simple text files that describe the fields of a ROS message. They are used to generate source code for messages in different languages.
* srv: an srv file describes a service. It is composed of two parts: a request and a response.
### 5.2 create msg
* `roscd package_name2`
* `mkdir msg`
* `touch name1.msg`
* adding multiple elements, one per line,like string first_name
### 5.3 create srv
* `roscd package_name2`
* `mkdir srv`
* `touch name2.srv`
* wirte it(need to learn)
## 6.Writing a Simple Publisher and Subscriber
### 6.1 Writing the Publisher Node
* `roscd package_name2`
* `mkdir src`
* touch talker.cpp
* wirte it(need to learn)
### 6.2 Writing the Subscriber Node
* `roscd package_name2`
* `mkdir src`
* touch listener.cpp
* wirte it(need to learn)
## 7.edit CMakeLists.txt
(need to learn)
## 8.catkin_make(In your catkin workspace)
* then we can Examining the Simple Publisher and Subscriber
## 9. Writing a Simple Service and Client
