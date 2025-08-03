---
layout: default
title: Projects
nav_order: 2
---

[Home](index.md)

## List

- [Sensor System for Predictive Maintenance](#sensor-system-for-predictive-maintenance)
- [ML Regression Toolkit](#ml-regression-toolkit-internship)
- [Extended Kalman Filter for a Quadcopter](#extended-kalman-filter-for-a-quadcopter)
- [Ancelotti Robot](#ancelotti-robot)
- [SiiuuTunes](#siiuutunes)
- [Palletizer Robotic Arm](#palletizer-robotic-arm)
- [Bonus](#bonus)

## Projects

## Sensor System for Predictive Maintenance

Sensor module design, embedded development, and ML for predictive maintenance.  
It was developed in the scope of the [GreenAuto](https://www.agendagreenauto.pt/projeto/) Project.

You can read the full dissertation here: [Dissertation](documents/SensorSystemForPredictiveMaintenanceInIndustrialEnvironments.pdf)

### Highlights

### Lowlights

- I only noticed that there was a typo in the title the day before presenting the dissertation. Still feel

### Lessons Learned

## ML Regression Toolkit (Internship)

Python toolkit using XGBoost, SHAP, and Streamlit for regression optimization.

### Highlights

### Lowlights

### Lessons Learned

## Extended Kalman Filter for a Quadcopter

Developed a 3D position estimation system for an aerial robot using an Extended Kalman Filter (EKF). The setup involved static beacons placed at known locations, measuring distances to the robot.

Built with Webots, ROS, Python, and C++, the system integrates sensor data and simulates beacon-based localization. The project covered EKF development, implementation, and analysis of results.

### Highlights

- Had to understand how to apply theory to practice.
- Gained a lot of experience with handling messy tools like WeBots. The support was poor and ChatGPT was still at a point where you were lucky if it was available due to the high demand, so I spent many hours banging my head against the wall.
- Got to see lots of cool drones in one of the laboratories of the Universidad de Sevilla, namely through the [Griffin](https://griffin-erc-advanced-grant.eu/) project.
- The report and presentation were done fully in Spanish.

### Lowlights

- At the time, my knowledge was more limited regarding software tools like Docker. It slowed me down considerably due to having to work with tools like ROS and WeBots.

### Lessons Learned

### Cool Drones

Open to see some cool drones:

![Big Boy](/images/projects/ekf/ganda_drone.jpg)

![Tunnel Inspection Boy](/images/projects/ekf/longo.jpg)

![Birdie](/images/projects/ekf/passaro.jpg)

![Blurry Pipe Boy](/images/projects/ekf/pipe.jpg)

## Palletizer Robotic Arm

3D Printed Palletizer servo-controlled arm. Objective: pick up pieces and organized them by colour. Components: servo motors, colour sensor, lcd, ATmega328p.

### Highlights

- Inspired interest in embedded systems
- Used different types of components
- Hardware restrictions lead to creative solutions
  - The microcontroller only has 2 ports capable of running the servo motors, so separate transistors were used to make a "pin selector" to change how the pins were connected to each servo.

### Lowlights

- It was during the covid lockdown, so access to hardware tools was quite limited which made it harder to debug.
- The component precision was low, so the whole project was a bit finnicky.
- Single buttons make for annoying *"User Interfaces"*.

### Lessons Learned

- One must be careful with hardware, frying the chip is not difficult
- Necessity really leads to enginuity

## Ancelotti Robot

### Highlights

### Lowlights

### Lessons Learned

## SiiuuTunes

### Highlights

### Lowlights

### Lessons Learned

## Bonus

#### Ray Tracer

I followed this book to practice some C/C++ while learning something outside "my realm": [Ray Tracing In One Weekend](https://raytracing.github.io/books/RayTracingInOneWeekend.html). It takes you from nothing to creating an image like this:

![Final rendered image](/images/projects/craysiete/lindissimo.png)

It is quite easy to follow and super satisfying to see some basic renders. The final results is very "bare bones", so a typo will leave you with something wrong like this:

![Oopsie](/images/projects/craysiete/lindissirrissimo.png)

It only took like 1 hour to render, yey.
