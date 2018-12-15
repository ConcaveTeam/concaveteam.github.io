---
layout: page
title: Sprint 2
---

## Software

<img src="images/sprint2depthmap.png" width="50%">

For the second sprint we tried to generate depth maps from both stereo vision and a single camera using machine learning.
The second method was very computationally expensive and we were unable to get any legitimate results from it.
We were able to generate depth maps from the stereo vision but they were very sparse due to camera mounts being not very rigid and calibration issues.
So we used a setup where we ran the monocular computer vision on both cameras and cross checked before locking on a target.

## Electrical/Firmware

<img src="images/sprint2firm.jpg" width="80%">

We calculated the mass of the launcher and the mounts and estimated the torque required to move the setup by calculating the locations of the COMs. We built an external circuit to power the servos since 3.3v from the teensy 3.6 wasn’t enough to get the motors moving. We also modified the firmware to be able to trigger the launcher. In order to optimize communication between the computer and the firmware over ROS, we automatically generated an arduino library to process new types including an aiming type and a trigger type.

## Mechanical

<img src="images/pic02.jpg" height="300em">
<img src="images/sprint2rend.jpg" height="300em">

For our final product, we chose to work on improving the function and increasing the aesthetics of the mechanical system. We reoutfitted our mechanism with an upgraded Nerf launcher that featured modifications to its trigger, motor, flywheels, barrel and battery. With the new launcher, the darts were able to fly faster, with higher accuracy and precision which decreased the latency of the entire system. We also added additional circular bearings to reduce the shear on the bearing support for the tilt servo.

To increase the visual appeal of the total system, we remade everything out of clear acrylic. With the smooth finish and transparent qualities that would expose the inner workings of our system, we believed that acrylic would give our mechanism a slick and elegant look that the MDF did not achieve. Acrylic was chosen as it had similar material properties to the MDF in terms of machinability concerns although additional provisions had to be made for differing chemical properties in terms of assembly. While the acrylic proved to be less forgiving as it is more brittle than MDF, the rigidity improved our stereo vision as the base was less flexible and was affected less by the uneven surface that it was lying on. We also edited some of our designs with visuals in mind such as the circular base. 
