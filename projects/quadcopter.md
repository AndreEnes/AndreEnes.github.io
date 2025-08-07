---
layout: default
title: Projects
permalink: /projects/
nav_order: 7
---

[Back](/projects/)

## Extended Kalman Filter for a Quadcopter

This project focused on 3D localization of an aerial robot (UAV) using an Extended Kalman Filter (EKF) with beacon-based distance measurements. It was implemented using Python, C++, ROS, and Webots to estimate the UAV’s position by fusing noisy data from static beacons with a motion model. The work included:

- Designing state and measurement models for UAV motion.
- Developing a nonlinear observation model based on beacon distances.
- Implementing an EKF with dynamic Jacobian updates.
- Creating ROS nodes for beacons, the UAV, and the filter logic.
- Running simulations and visualizations in Webots and Jupyter.

Extensive testing demonstrated that the EKF accurately estimated the UAV’s position under various conditions, including sensor noise, beacon layout changes, and signal loss.
You can check the report [here (in spanish)](/documents/ROS_EKF_WITH_BEACONS.pdf).

![simulation](/images/projects/ekf/simulation.jpg)

### Tech Explored

- ROS
- WeBots
- [FilterPy](https://filterpy.readthedocs.io/en/latest/#)
- Extended Kalman Filter

### Highlights

- Had to understand how to apply theory to practice.
- Gained a lot of experience with handling messy tools like WeBots. The support was poor and ChatGPT was still at a point where you were lucky if it was available due to the high demand, so I spent many hours banging my head against the wall.
- Got to see lots of cool drones in one of the laboratories of the Universidad de Sevilla, namely through the [Griffin](https://griffin-erc-advanced-grant.eu/) project.
- The report and presentation were done fully in Spanish.

### Lowlights

- At the time, my knowledge was more limited regarding software tools like Docker. It slowed me down considerably due to having to work with tools like ROS and WeBots.
- I had a basically incompatible schedule with my group partner, so working together was not easy and there was some duplicated work.

### Lessons Learned

- Although software development tools like Docker are often not the most important part of a project, they make it easier to get to your end goal.
- Robotics is a really broad field and the possibilities are never ending.
- Unless open source tools get a dedicated team to them, documentation and tutorials will probably be scarce.
- Probing around is a good way to learn.
- Try to be ready for meetings ahead of time. Having clear goals is a timesaver.

### Cool Drones

Here are some pictures of cool drones that were in the [Griffin](https://griffin-erc-advanced-grant.eu/) project laboratory:

![Big Boy](/images/projects/ekf/ganda_drone.jpg)

![Tunnel Inspection Boy](/images/projects/ekf/longo.jpg)

![Birdie](/images/projects/ekf/passaro.jpg)

![Blurry Pipe Boy](/images/projects/ekf/pipe.jpg)
