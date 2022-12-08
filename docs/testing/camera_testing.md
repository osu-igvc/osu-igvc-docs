---
title: Sensor Testing
parent: Project Testing
layout: default
---

# Camera Testing

## UNIT: Basic Video Reception
The test is completed to test video reception.

### Criteria:
- Camera stream received by computer
- Stream is at least 30 frames per second
- Stream is at least 1080p

### Methodology:
1. Connect camera to computer (via ethernet or USB)
2. Load up any software needed to stream video to computer
  a. For blackfly cameras use SpinView/Spinnaker
  b. For Realsense camera use Intel software provided (Link for repo to be added)
3. Start streaming video 

## UNIT: Video Clarity

### Criteria:
- Camera focus is clear
- Camera stream quailty is at least 1080p
- Camera is mounted with minimal shaking

### Methodology:
1. Connect camera to computer
2. Load up streaming software
3. Stream video
4. Review quaility (manually and through algorithms)
  a. If quality is not sufficent change settings and repeat
  
  
  

