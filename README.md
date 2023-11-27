[![ROS2](https://github.com/IMRCLab/motion_capture_tracking/actions/workflows/ROS.yml/badge.svg?branch=ros2)](https://github.com/IMRCLab/motion_capture_tracking/actions/workflows/ROS.yml)

# motion_capture_tracking
Fork of https://github.com/IMRCLab/motion_capture_tracking/
* Merged ros2 branch into main
* Verified to work on ROS2 Humble with Ubuntu 22.04 with Vicon Tracker 4.0
* Used Vicon with IP address of 192.168.10.1 as default in both source code and launch file 

This repository is a ROS package that provides an abstraction of different motion capture systems (Vicon, OptiTrack, Qualisys) with three different tracking modes: i) Tracking of rigid bodies poses via the official software (e.g., Vicon Tracker) using unique marker arrangements, ii) Tracking of rigid bodies poses with custom frame-to-frame tracking with identical marker arrangements, iii) Tracking of unlabeled marker positions using custom frame-to-frame tracking.

## Building

To build from source, clone the latest version from this repository into your catkin workspace and compile the package using

```
cd ros_ws/src
git clone --recurse-submodules https://github.com/uah-crablab/motion_capture_tracking.git
cd ../
colcon build
```

## Running
`ros2 launch motion_capture_tracking launch.py`

or

`ros2 run motion_capture_tracking motion_capture_tracking_node` 
