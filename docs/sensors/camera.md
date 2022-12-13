---
title: Vision
layout: default
parent: Sensors
---
# Vision Sensors

## Blackfly
For the RGB data collection required for many aspects of the algoritham, including lane detection and blob detection we are using a couple of blackfly cameras mounted ontu the car. These blackflys are POE and we will be using Spinnaker SDK driver made for ROS2, the information on spinnaker and installation instruction can be found [here](https://github.com/berndpfrommer/flir_spinnaker_ros2).
### Running the Blackfly
Since the Blackfly is POE you only need to worry about making sure the camera is connected to the computer either directly or through an ethernet switch. Then you need to launch spinnaker by going to the location spinnaker is installed too and running spinnaker. you can run SpinView to test the camera output in real time.
### Troubleshooting
One of the major issued we have run into while running blackflys through the spinnaker SDK has been bandwith issues while using the ethernet switch. This issue has been fixed temporarily by plugging the camera directly into the computer and plans have been made to purchase an ethernet switch with the required bandwidth. 



