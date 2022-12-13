---
title: Sensor Testing
parent: Project Testing
has_children: true
layout: default
---
# Sensor Testing Overview

## Camera Testing

###   Blackfly camera
        - Will be used to feed live video back to algorithms and mapping software.
 
###   Realsense camera
        - Backup camera; if needed can be used for extra footage behind vehicle for parking test.


## Lidar Testing 
  - Lidar will be used to create a map of the area, to detect objects, and to detect pedestians.


## GPS Testing
  - Testing functionality, various environments, and different calibration tests to guarentee data output is as accurate as possible.


## Software
  - Software testing will include testing any software included with the hardware or used for hardware functionality. This does not include the algorithms made for     perception and mapping. 

## Algorithm Testing
    - Testing will include Unit and Stress tests for each algorithm and will be updated as needed.

###   Blob detection
      - Unit and Stress tests to make sure algorithm can detect blobs under a varity of environmental conditions.

###   Lane Detection
      - Unit and Stress tests to ensure algorithm can detect lanes in any footage given. 



