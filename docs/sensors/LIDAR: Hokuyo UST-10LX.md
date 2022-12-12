---
title: LIDAR Hokuyo UST-10LX
layout: default
parent: Sensors
---

# LIDAR: LIDAR: Hokuyo UST-10LX
## Setup
For the Hokuyo UST-10LX we were able to use the urg_node package for ROS2 which can be found [here](https://github.com/ros-drivers/urg_node). After following the instructions on GitHub for installing urg_node then all that is left to do is power the Lidars, and then run them with the urg_node package which will then post the topics into ROS2
## Running
The Lidar requires 12V of power and must be connected to the computer using ethernet. To start up the urg_node package in Ubuntu 20.04 you must first have ROS2 and the urg_node package installed. Then in the terminal you need follow the steps below. 
- run the command "source /opt/ros/foxy/setup.bash"
- then launch urg_node by going to /opt/urg_node
## Visualizing with Rviz
Assuming ROS2 is installed you can visualize the Lidar point cloud in RVIZ. To do this you must first start RVIZ by going to ros2 file location and running RVIZ. Then you need to start the urg_node and begin publishing the data using the instructions above. Once the Lidar is running you should be able to add the topic /scan in RVIZ, if the topic is not visible then try restarting both the urg_node and RVIZ. Once the topic is added to RVIZ you must select a reference frame, if you are just running the Lidar, you can select the Lidar local frame which can be found in the terminal running the urg_node. Once you have the topic and reference frame you should be able to see the point cloud visualized in RVIZ.  
## Troubleshooting
If the Lidar doesn’t publish data to ROS2 you should check to ensure that the urg_node package is installed correctly and that ROS2 and that all wires are connected and confirmed to be working.  
