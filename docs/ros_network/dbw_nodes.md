---
title: Drive-By-Wire Nodes
layout: default
parent: ROS2 Nodes
grand_parent: Ros network overview
nav_order: 1
---

# Drive-By-Wire Nodes
  List of Nodes made to connect to the Drive by wire system
  
## Joystick Node
### About / Logistics
  This node was created in Visual Studio for Ubuntu 20.04 and ROS2
  The node takes in any "event" on the controller such as a button press or joystick movement and publishes it. The subscriber takes this event data and maps it using a state transform. This mapped data is the published to use to control the vehicle's speed and steering angle.

### Setup and Running
  To setup the node on Lab computer:
    1. Open terminal
    2. Run publisher through ROS2 in one terminal window
    3. Run Subscriber through ROS2 in second terminal window

 

