# ROS_cheat_sheet
ROS_cheat_sheet

## Create a new workspace with catkin_make
[ros.org: create a workspace](http://wiki.ros.org/catkin/Tutorials/create_a_workspace)

```
source opt/ros/kinetic/setup.bash
```

make directory, first build
```
mkdir -p ~/new_workspace_ws/src
cd ~/new_workspace_ws/
catkin_make
```
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
