[kitchen]: ./kitchen.png

# RoboND-SLAM
ROS package that uses RTAB-Map to generate 3D maps of two different environments

![kitchen][kitchen]

## Robot ##
The robot is a simulated model of a [Waveshare Alphabot](https://www.amazon.com/gp/product/B01N1JWFKZ/ref=oh_aui_detailpage_o09_s00?ie=UTF8&psc=1)
with an RGBD camera controlled by the libgazebo_ros_openni_kinect plugin.

## Installation ##
1. Copy the ```slam_bot``` folder into the ```src``` directory of your catkin workspace.
2. Install RTAB-Map with ```sudo apt-get install ros-<ros distro>-rtabmap-ros```
3. Run ```catkin_make```

## Running ##
Once you've built and sourced the catkin workspace, run RTAB-Map with
```
src/launch/rtabmap-run
```

This script will start gazebo, rtabmap, rviz, and a teleop node.

## Mapping ##
Once all of the nodes are launched, use the teleop terminal to steer the robot through the environment.
RTAB-Map keeps track of visual features in the environment, so it will recognize previously explored areas.
Give it a try!
