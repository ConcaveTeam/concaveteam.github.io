---
layout: page
title: Sprint 1
---

## Software

<iframe width="560" height="315" src="https://www.youtube.com/embed/6PP5_Vex5aE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

For the first sprint we chose to go with OpenCv object detection code which bound all objects in circles and shot at the center of the largest moving one.
It converted the location from image coordinates to spherical coordinates which could then directly be put into the servos.
We ran this on the webcam of our laptop and broadcast the required coordinates on the ROS serial monitor for the firmware to pull from and aim.
The dot follows image coordinates, so the y-axis is inverted in the video.

## Firmware/Electrical

<iframe width="560" height="315" src="https://www.youtube.com/embed/8uvGyRd6DlQ" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

The above video demonstrates a proof-of-concept mechanical aiming mechanism and the firmware controlling the hardware.
We used small servos powered by the teensy3.6 microcontroller working with firmware very similar to the one used in Lab 2 but with ability to get information from the ROS serial protocol.
We used the Hobby king Hk-15269 servos to create a pantilt mechanism similar to the one in Lab2 but outfitted with a laser point to show its targeting.
The motors were controlled by a teensy 3.6 which we chose instead of an Uno due to its higher clock speed.
Since they were low power motors they were powered directly from the microcontroller.
The firmware got coordinates from the ROS serial protocol and set the servos to that angle.

## Mechanical

<img src="images/sprint1mech.jpg" height="200em">
<img src="images/sprint1rend.png" height="200em">

In the first sprint, we chose to create a small model that can be used with the software to track a moving object. This included making a small pan-tilt mechanism to hold a laser pointer and using servo motors to move the components. The software would tell the angles at which the servos needed to move to in order to point at an object that is being tracked. This was used as a proof of concept to tell us that we could at least make a small version of a tracking mechanism. 

From here, we began to spec out materials and resources to start making a larger mechanism that would be the basis of our MVP. These materials, such as various motors or servos, would be going towards making a pan-tilt mechanism to hold a Nerf gun. We decided to use a Nerf Stryfe due to its relatively easy trigger actuation as well as its ease of modification.
