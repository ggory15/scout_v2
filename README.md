# Scout Simulation Operation Process

## 0. clone git repository & add gazebo_model_path
```
git clone --recursive git@github.com:ggory15/scout_v2.git -b noetic-devel

cd scout_v2/scout_gazebo/worlds/gazebo_map_for_khnp
echo "export GAZEBO_MODEL_PATH=:$GAZEBO_MODEL_PATH:$(pwd)/refracted_corridor_map:$(pwd)/rough_terrain_map:$(pwd)/stair_map:$(pwd)/qr_codes:$(pwd)/manipulator_map:$(pwd)/disturbance_map:$(pwd)/common" >> ~/.bashrc
```

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
hector_gazebo_plugins

## 3.	About Usage

### Launch Gazebo
```
roslaunch scout_gazebo scout_playpen.launch
```

### Launch Rviz
```
roslaunch scout_viz view_robot.launch
```

### Launch Navigation
```
roslaunch scout_navigation amcl_demo.launch
```
 
## Original Code
The original code is from official github of scout-v2 [Click](https://github.com/agilexrobotics/ugv_gazebo_sim). 


