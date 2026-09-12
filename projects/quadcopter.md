---
layout: default
title: Beacon-Based 3D Localisation of a Quadcopter Using Extended Kalman Filter
nav_order: 7
---

[Back](../)

## Beacon-Based 3D Localisation of a Quadcopter Using Extended Kalman Filter

We estimated the 3D position of a quadcopter with an Extended Kalman Filter, fusing a motion model with distance measurements from static RF beacons. It runs in Python on ROS Noetic, simulated in Webots, with the filter itself built on FilterPy.

The beacons are Webots emitter and receiver pairs, each on its own channel so that the drone can tell them apart. Distance is estimated from signal strength, which is noisy, and that noise is the reason the filter is there in the first place. We ran it with both the Crazyflie and the DJI Mavic 2 PRO models.

The estimate held up in simulation under sensor noise, changes to the beacon layout and loss of signal.

The code is [on GitHub](https://github.com/AndreEnes/ROS_Quadcopter_EKF), and the report is [here](/documents/ROS_EKF_WITH_BEACONS.pdf), written in Spanish.

![simulation](/images/projects/ekf/simulation.jpg)

### Tech Explored

- ROS
- Webots
- [FilterPy](https://filterpy.readthedocs.io/en/latest/#)
- Extended Kalman Filter

### Highlights

- Had to understand how to apply theory to practice.
- Gained a lot of experience with handling messy tools like Webots. The support was poor and ChatGPT was still at a point where you were lucky if it was available due to the high demand, so I spent many hours banging my head against the wall.
- Got to see lots of cool drones in one of the laboratories of the Universidad de Sevilla, namely through the [Griffin](https://griffin-erc-advanced-grant.eu/) project.
- The report and presentation were done fully in Spanish.

### Lowlights

- At the time, my knowledge was more limited regarding software tools like Docker. It slowed me down considerably due to having to work with tools like ROS and Webots.
- My partner and I had schedules that barely overlapped, and we did not set up any way to track who was doing what. Some work got done twice as a result.

### Lessons Learned

- Although software development tools like Docker are often not the most important part of a project, they make it easier to get to your end goal.
- Robotics is a really broad field and the possibilities are never-ending.
- Unless open source tools get a dedicated team to them, documentation and tutorials will probably be scarce.
- Probing around is a good way to learn.
- Try to be ready for meetings ahead of time. Having clear goals is a timesaver.

### Cool Drones

Here are some pictures of cool drones that were in the [Griffin](https://griffin-erc-advanced-grant.eu/) project laboratory:

![Big Boy](/images/projects/ekf/ganda_drone.jpg)

![Tunnel Inspection Boy](/images/projects/ekf/longo.jpg)

![Birdie](/images/projects/ekf/passaro.jpg)

![Blurry Pipe Boy](/images/projects/ekf/pipe.jpg)
