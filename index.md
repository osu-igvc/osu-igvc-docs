---
title: Project Overview
layout: home
nav_order: 1
---

# IGVC Project Overview
  The goal is to compete in the IGVC competition after Spring 2023 with a Polaris Gem2 vehicle that has a maunal and autonomous mode. In order to create a autonomy software package quickly we are using exisiting software and integrating it into one. 
  
## Hardware and Drive-By-Wire (DBW)
  Using a ROS2 node a PS4 controller is used to control the veocity and steering angle of the vehicle. The DBW team worked on manual operation and some autonomy features such as the braking system, E-Stops, electrical system, and the steering system. 
  
  For navigation and perception a list of hardware was selcted:
  - 2 planar Lidars (Hokuyo UST-10LX and Hokuyo UTM-30LX)
  - 1 GPS (VectorNav 300)
  - 1-4 Blackfly cameras (Blackfly PGE-31S4C-C from Flir)
  - 1 Realsense camera (Intel D455)

## Software and Algorithms
  Algorithms were utilized to detect lanes and objects in ROS2.
  The Lane Detection alorithm uses the Odometry to find the average distance between the two white lines on the screen. 
  The Blob detection uses depth readings and video outputs to detect a specified color and identify it as an object. 
  A GUI will display the course map and the status of onboard systems. 
  
