---
title: GPS
layout: default
parent: Sensors
---

# VN 300 information
## Setup and Operation
To start testing the VectorNav 300 download the Control Center program from the VectorNav website. The IMU for the VectorNav is placed in the middle of a test cart that also has cameras and Lidars onboard. Two antennas coming from the IMU are placed two feet apart from each other to pick up position of the cart. A USB that comes from the IMU is connected to the test computer, and the control center is launched. Data is collected from the control center. The Vector NAV ROS2 Driver that is used to put data into ROS2 is downloaded from the following website:
## Possible Issues
The IMU is not accurate enough for the position measurement needed so other data such as velocity becomes increasingly inaccurate. This can be fixed by calibrating the equipment and testing it against appropriate equipment like a speed radar gun for acceleration and velocity.  
