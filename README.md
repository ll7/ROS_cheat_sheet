# ROS_cheat_sheet
ROS_cheat_sheet

### Create a new workspace with catkin_make
[ros.org: create a workspace](http://wiki.ros.org/catkin/Tutorials/create_a_workspace)  
[nice video](https://www.youtube.com/watch?v=7QgjR6m-0KM)

```
source opt/ros/kinetic/setup.bash
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
