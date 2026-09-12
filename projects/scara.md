---
layout: default
title: SCARA Robotic Arm Project
nav_order: 10
---

[Back](../)

## SCARA Robotic Arm Project

Modelling and controlling a SCARA robotic arm.

I defined the reference frames with the Denavit-Hartenberg method for the forward kinematics, then derived the geometric equations for the inverse. The existing code had to be extended there, because θ₂ has more than one valid solution and it only handled one.

The Jacobian turned end-effector velocities into joint velocities. I also added two trajectory modes, linear and circular, both correcting for deviation along the way.

The project was done in a custom simulator, created by my professor at the time, so I don't have any pictures of it working. Here is one of a SCARA robot to give more context: ![SCARA](/images/projects/scara/SCARA_robot_2R.png)

### Highlights

- Working with Robotics topics is fun.
- Having to think in 3 dimensions is satisfying. I wish I had taken up technical drawing. I should learn it and CAD as well (although I've had some exploration time with it).

### Lowlights

- Working with a custom simulator came with some "lack of documentation" problems.

### Lessons Learned

- It's ok to ask stupid questions. I had totally forgotten what the "Inner Product" was and sent an email to my Professor, who answered me in person. He made me understand I was being a dummy, but in a kind way. I've had worse responses.
