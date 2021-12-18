[TOC]

# Scout Simulation Operation Process

## 1.	Introduction of Function Package

```
├── scout_control
├── scout_description
├── scout_gazebo
├── scout_navigation
└── scout_viz
```

​	scout_gazebo：The folder is gazebo simulation function package

​	scout_control: The folder is simulation controller function package
                : This package contains 1) Scout_Velcity Controller
                                        2) Teleop for Joystick of Keyboard 

​	scout_description: The folder is the function package of model file

​	scout_navigation: The folder is the function package of amcl, gmapping, and move_base

​	scoutviz: The folder is the function package for rviz

## 2.	Environment

### Development Environment

​	ubuntu 20.04 + [ROS Noetic desktop full](http://wiki.ros.org/noetic/Installation/Ubuntu)

### Dependency
velodyne_description
lms1xx_description 

## 3.	About Usage

### Launch Gazebo
```
rosrun scout_gazebo scout_playpen.launch
```

### Launch Rviz
```
rosrun scout_viz view_robot.launch
```

### Launch Navigation
```
rosrun scout_navigation amcl_demo.launch
```
 
## Original Code
The original code is from official github of scout-v2 [Clikc](https://github.com/agilexrobotics/ugv_gazebo_sim). 


