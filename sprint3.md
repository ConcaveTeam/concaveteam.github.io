---
layout: page
title: Sprint 3
---

## Software

<img src="images/depth2.png" width="50%">

For the third sprint we were able to generate much better depth maps but they still had a slight amount of noise and switched erratically between multiple moving objects.
So we had a backup code which relied on trigonometry to estimate the distance between the detected object and the cameras.
The legacy code for the triangulation system exists in the software's `ssreekanth2000-patch-1` branch on `src/TrackMono/TrackMono.cpp`.

## Firmware/Electrical

<iframe width="560" height="315" src="https://www.youtube.com/embed/zrE_tocqXjA" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

We had to change the trigger mechanism to facilitate the new design with servos.
Rather than a subscription model which our aiming mechanism used, we use a service which pulls the trigger on a signal, returning a completion status.
The above video demonstrates shooting Julian as he moves around.
Internally, we use a service rather than a subscription to control the trigger, cluttering the serial communication less.

## Mechanical

<img src="images/sprint2pic.jpg" height="300em">
<img src="images/sprint3rend.jpg" height="300em">

This sprint features a different camera mount which reduces jiggling, which increases the effectiveness of stereo vision.
During this sprint, we began design and fabrication of the final components needed to create a functioning minimum viable product. The first of these components was an actuation system for the Nerf launcher’s trigger. During operation, the launcher cannot be manually triggered by an outside object. To resolve this issue, we decided to mount two servos, one on each side of the Nerf gun’s trigger, that are connect using servo horns and spring wire. By changing the servo angles, the spring wire pulls the trigger back and, thus, fires a dart.

The other component we focus on was a support system to help stabilize the motion of the pan-tilt mechanism. The base servo that operated the horizontal angle movement didn’t support the weight above it well and needed assistance. So we decided to implement a lazy susan mechanism which consisted of free-moving ball bearings that were enclosed beneath the U-mount that held up the Nerf launcher and its holster. This solution added more consistency and much needed support. We also redesigned the camera mounts for a single angle and to be much more rigid.
