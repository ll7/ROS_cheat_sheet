# ROS_cheat_sheet
ROS_cheat_sheet

## Create a new workspace

make directory, first build
```
mkdir -p ~/new_workspace_ws/src
cd ~/new_workspace_ws/
catkin build
```
set new workspace path
```
export ROS_PACKAGE_PATH=~/new_workspace_ws/:/opt/ros/kinetic/share
```
