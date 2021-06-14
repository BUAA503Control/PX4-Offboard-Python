# PX4-Offboard-Python
It is a case for PX4 Offboard Control using Python.

## **installation**
```
cd catkin_ws/src
git clone https://github.com/yrwang501/offb_py.git
cd ..
catkin_make
source devel/setup.bash
```

## **RUNNING**
Run MAVROS and Gazebo in two terminals:
```
source ~/catkin_ws_py/devel/setup.bash
roslaunch mavros px4.launch fcu_url:="udp://:14540@127.0.0.1:14557"
```
```
cd ~/DLR-uav-gazebo/Firmware
make px4_sitl_default gazebo
```
OR
```
cd PX4-Autopilot
source ~/PX4-Autopilot/Tools/setup_gazebo.bash ~/PX4-Autopilot/ ~/PX4-Autopilot/build/px4_sitl_default
export ROS_PACKAGE_PATH=$ROS_PACKAGE_PATH:~/PX4-Autopilot
export ROS_PACKAGE_PATH=$ROS_PACKAGE_PATH:~/PX4-Autopilot/Tools/sitl_gazebo
roslaunch px4 posix_sitl.launch
```
```
source ~/catkin_ws_py/devel/setup.bash
rosrun offb_py offb.py
```

