---
title: Current Status
layout: default
nav_order: 2
---

# Current Status

## DBW functionality:

**Functional**
- Joystick control
- Throttle and steering 
- Blinkers
- Buzzer
- Safety enable
- E-stop functionality

**Not Functional**
- Brake control

## Autonomy Functionality

### Sensors



### Computer Vision

Computer vision is necessary to detect lanes, pedestrians, and some obstacles in the road.

**Lane Tracking**

Needs tuning
{: .label .label-orange}

Lane tracking is necessary for lane keeping during navigation. Our plan is to extract lane positions from the image and geometrically project them onto the costmap used for path planning. Currently, we can detect lanes in certain lighting conditions. The algorithm first masks for all yellow and white in a region of interest in front of the vehicle. The remaining pixels are combined into a histogram along the width of the camera frame. If a lane is present, two peaks will appear on the histogram - these peaks are chosen to be the lanes. The algorithm referenced was largely derived from [Automatic Addison](https://automaticaddison.com/the-ultimate-guide-to-real-time-lane-detection-using-opencv/).

This method works under good lighting conditions and when little white-color pollution is in frame. Additional tuning will be necessary to achieve robust and safe functionality.



**Pedestrian Detection**

Detection works, need to extract position
{: .label .label-orange}

One functional test for IGVC is detecting a "pedestrian," simulated by a mannequin in the road with an orange high-vis vest. Within the constraints of the competition, pedestrian detection boils down to orange-blob detection. This is done with simple HSV masking of the color orange within a region of interest. Gaussian filters, erosion, and dilation operations are performed to reduce noise in the image. Contours are then found and the largest is determined to be the blob.

This can result in false detections. For example, an orange ladder in the lab space is sometimes detected as a pedestrian. Future implementations should include secondary detections - such as other colors or features - to combine with the primary color detection.


### State Estimation

State estimation is critical to the vehicle's performance. Currently, an unscented Kalman filter (UKF) provided by the *robot_localization* package is used to compute odometry.

**Visual Odometry**
Visual odometry (VO) is performed with the Intel Realsense D455's RGBD image stream. The *rgbd_odometry* node, provided from the VSLAM package *RTABMAP_ROS*, computes odometry information using optical flow. The image stream is highly compressed, and odometry can be lost under some conditions like an object passing too close in front of the camera. The VO information is fused in the UKF.

**IMU**
Inertial measurements from the D455 are fused in the UKF to provide more information on linear accelerations and angular velocities. In the future, the VectorNav VN-300's IMU will be fused but it must be properly calibrated beforehand.

**Laser Odometry**
We experimented with laser odometry from the 30 meter Hokuyo's laser scan, but found it to decrease the performance of the UKF's estimate. We will likely approach this again with different parameters later.


### Simultaneous Localization and Mapping (SLAM)

Rudimentary SLAM is performed with the *slam_toolbox* ROS package. Results are not production ready, but are promising. The package uses the odometry estimate from the UKF and laser scans from the forward-facing Hokuyo lidar to map. 


### Graphical User Interface (GUI)

The GUI has not been improved since the initial updates at the beginning of the semester. Our plan is to overhaul it by developing it in JavaScript as an Electron app. This will allow us to achieve a much smoother and cleaner interface purpose-built for both touchscreen and keyboard/mouse usage. The original GUI is built using PyQT 6, which is functional but leaves much to be desired.


# Next Steps


