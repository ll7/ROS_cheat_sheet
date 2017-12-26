# ROS_cheat_sheet
ROS_cheat_sheet

### Create a new workspace with catkin_make
[ros.org: create a workspace](http://wiki.ros.org/catkin/Tutorials/create_a_workspace)  
[nice video](https://www.youtube.com/watch?v=7QgjR6m-0KM)

```
source /opt/ros/kinetic/setup.bash
```

make directory, first build
```
mkdir -p ~/new_workspace_ws/src
cd ~/new_workspace_ws/src
catkin_init_worksapce
cd ..
catkin_make
```
New folder are created. Check with:
```
ls
``` 
build: where executables will be located  
devel: setup files and environments stuff

```
echo ${ROS_PACKAGE_PATH}
source devel/setup.bash
```
update package path:
```
echo ${ROS_PACKAGE_PATH} ~/new_workspace_ws/src:/opt/ros/kinetic/share
```
check current workspace directory
```
echo $ROS_PACKAGE_PATH
```
### 2 ways to create package
1. by hand  
2. `catkin_create_pkg` (recommended)
#### create package by hand
```
cd ~/new_workspace_ws/src
mkdir new_package
cd new_package/
nano CMakeLists.txt
```
Use your favourite terminal text editor.  
Paste:

```
cmake_minimum_require(VERSION 2.8.3)
project(package_demo)

find_package(catkin REQUIRED COMPONENTS)
```
save the file

#### create package with `catkin_create_pkg`
```
cd ~/new_workspace_ws/src/
catkin_create_pkg new_package dependend_package1 dependend_package2
```

### Finally, make package
```
cd ~/new_workspace_ws/
catkin_make
```
## Create a new node with python
Create the new node `new_node.py` in your src folder of your new package.  
Make the new node executable:
```
chmod +x new_node.py
```
## QT Creater Plugin
[QT Creater Plugin](https://ros-industrial.github.io/ros_qtc_plugin/index.html)  
[yt video](https://www.youtube.com/watch?v=MPovFrZloaY&index=2&list=PL4p99tXbgB8_ajY8p6TRZx1gqhp5pRMB-)  

A few things have changed comparing this video and the recent version of QT Creater (2017/12).  

New Project > Other Projects > ROS Workspace

Name: your new sub workspace
Workspace Path: your old parent workspace  

Furthermore, you can't add empty folders, somehow...
Workorund. Start console in your new package, create the first line of whatever file you are going to create in the src subfolder of the package. Then, continue your work in QT :+1:

