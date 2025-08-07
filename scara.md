---
layout: default
title: Projects
nav_order: 10
---

[Back](projects.md)

## SCARA Robot

This project involved modeling and controlling a SCARA robotic arm using direct and inverse kinematics, Jacobian analysis, and trajectory planning.

##### Direct Kinematics

Reference frames were defined using the Denavit-Hartenberg method, allowing computation of transformation matrices. Joint inputs were read from a spreadsheet and applied to the robot using existing functions.

##### Inverse Kinematics

Geometric equations were derived to calculate joint values from target coordinates. Input constraints were checked, and existing code was updated to handle multiple θ₂ solutions.

##### Jacobian and Velocity Control

The Jacobian matrix was used to convert desired end-effector velocities into joint velocities, enabling real-time velocity control through matrix operations and feedback.

##### Trajectory Control

Two modes of trajectory control were implemented: linear and circular. Both included real-time correction for path deviations and automatic stopping at the destination.

The project was done in a custom simulator, created by my professor at the time, so I don't have any pictures of it working. Here is one of a SCARA robot to give more context: ![SCARA](/images/projects/scara/SCARA_robot_2R.png)

### Highlights

- Working with Robotics topics is fun.
- Having to think in 3 dimensions is satisfying. Wish I took up technical drawing. I should learn it and CAD as well (Although I've had some exploration time with it).

### Lowlights

- Working with a custom simulator came with some "lack of documentation" problems.

### Lessons Learned

- It's ok to ask stupid questions. I had totally forgotten what the "Inner Product" was and sent an email to my Professor, for which we answered me in person. He made me understand I was being stupid, but in a kind way. I've had worse experiences.
