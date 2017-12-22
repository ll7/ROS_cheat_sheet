# ROS_cheat_sheet
ROS_cheat_sheet

## Create a new workspace with catkin_make
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

set new workspace path
```
export ROS_PACKAGE_PATH=~/new_workspace_ws/:/opt/ros/kinetic/share
```
check current workspace directory
```
echo $ROS_PACKAGE_PATH
```
soruce setup file
```
source devel/setup.bash
```
