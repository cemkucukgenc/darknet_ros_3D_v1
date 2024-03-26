# Human and Object Detection with Intel D435 Depth Camera

### Table of contents
1. [Introduction](#introduction)
2. [Installation guide](#installation_guide)
    1. [System setup](#system_setup)
    2. [Installing dependencies](#installing_dependencies)
    3. [Building project](#building_project)
3. [Launching project](#launching_project)

## 1. Introduction <a name="introduction"></a>

Human and object detection with Intel D435 Depth Camera is applied by using `darknet_ros` package. Setup is done according to the video in the following youtube link with the source code in the drive link.
- https://github.com/leggedrobotics/darknet_ros
- https://www.youtube.com/watch?v=jxH68h8wzTM
- https://drive.google.com/drive/folders/1UHXizZZQEcFSx9R2IreEWMQO6SBcUyPy

## 2. Installation guide <a name="installation_guide"></a>

### 2.1. System setup <a name="system_setup"></a>
This project is developed for `Ubuntu 18.04` with `ROS Melodic`. Be sure your system has the same configuration. You can check the following links to install them:

 - `Ubuntu 18.04` setup guide link: https://releases.ubuntu.com/bionic/ 
 - `ROS Melodic` setup guide link: https://wiki.ros.org/melodic/Installation/Ubuntu 

 It is required that the `ROS Melodic` should be sourced in each terminal to run the simulation as mentioned in the `ROS Melodic` setup guide link. To do that,
 ```
source /opt/ros/melodic/setup.bash
 ```
should be sourced in each terminal. To make it easier, it can be added to the `.bashrc` file for automatic sourcing. Details can be found in the `ROS Melodic` setup guide link. Sourcing `ROS Melodic` will no longer be mentioned in further steps.

Bonus: If you have a different Linux or ROS distro than specified requirements, you may prefer to use a Docker container. To do that, check the `docker` folder.

### 2.2. Installing dependencies <a name="installing_dependencies"></a>

To have a clear installation, updating and upgrading your system is recommended.
```
sudo apt-get update
sudo apt-get upgrade
```

For the installation of packages, basic tools are required. 
```
sudo apt install git wget libtool apt-utils python-catkin-tools
```

### 2.3. Building project <a name="building_project"></a>

Open a terminal (will be mentioned as T1) and create a directory preferably in the `home` location as
```
mkdir -p sabes_ws
cd sabes_ws
```
Clone the project repository (T1)
```
git clone git@gitlab.lrz.de:innok-roboter/human_and_object_detection/darknet_ros_3d_v2.git
```
To build the project in `sabes_ws/darknet_ros_3d_v2/catkin_ws` (T1)
```
cd darknet_ros_3d_v2/catkin_ws
catkin build
```

## 3. Launching project <a name="launching_project"></a>

To run the project (T1)
```
source /sabes_ws/darknet_ros_3d_v2/catkin_ws/devel/setup.bash
roslaunch
```
