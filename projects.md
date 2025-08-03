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

This project explored the implementation of Predictive Maintenance in manufacturing environments that relied on legacy machinery lacking modern sensor capabilities. A wireless sensor system was developed using IoT hardware and Machine Learning algorithms to monitor equipment health through vibration, sound, and temperature data.

The system was designed specifically for Automated Guided Vehicles (AGVs) and nearby machines, with a focus on cost-effectiveness and space constraints. Data preprocessing techniques based on time-domain features were employed to minimize wireless data transmission. Supervised learning models delivered highly accurate anomaly detection results, while unsupervised models performed poorly. A comparative analysis of sensors with varying costs was also conducted to evaluate their performance.

This work demonstrated how emerging technologies could extend Industry 4.0 capabilities to older equipment, reducing downtime and optimizing maintenance schedules.

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

This project focused on 3D localization of an aerial robot (UAV) using an Extended Kalman Filter (EKF) with beacon-based distance measurements. It was implemented using Python, C++, ROS, and Webots to estimate the UAV’s position by fusing noisy data from static beacons with a motion model. The work included:

- Designing state and measurement models for UAV motion.
- Developing a nonlinear observation model based on beacon distances.
- Implementing an EKF with dynamic Jacobian updates.
- Creating ROS nodes for beacons, the UAV, and the filter logic.
- Running simulations and visualizations in Webots and Jupyter.

Extensive testing demonstrated that the EKF accurately estimated the UAV’s position under various conditions, including sensor noise, beacon layout changes, and signal loss.
You can check the report [here (in spanish)](documents/ROS_EKF_WITH_BEACONS.pdf).

![simulation](images/projects/ekf/simulation.jpg)

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

This project explored the integration of facial gesture recognition and animatronic control by developing a system in which a robotic head imitated human facial movements in real time. Using a webcam and [MediaPipe's Face Mesh](https://ai.google.dev/edge/mediapipe/solutions/vision/face_landmarker), facial landmarks were detected and analyzed to track expressions such as eye movement, eyebrow position, and mouth motion.

Servo control of the animatronic head was achieved using a Pololu Mini Maestro controller, initially interfaced via an Arduino UNO and later optimized with a pure Python-based solution, reducing hardware complexity. The robotic head, AnimaTRON 1.0, included eight servos that replicated facial gestures based on normalized landmark distances.

Although originally intended to integrate Botszy, a professional animatronic rigging platform, the project faced compatibility issues and proceeded with a manual software implementation.

Check the [report](documents/Ancelotti_Robot.pdf) for more information.

![cabeza](images/projects/ancelotti/cabeza.jpg)

### Highlights

### Lowlights

### Lessons Learned

## SiiuuTunes

### Highlights

### Lowlights

### Lessons Learned

## Bonus

### Ray Tracer

I followed this book to practice some C/C++ while learning something outside "my realm": [Ray Tracing In One Weekend](https://raytracing.github.io/books/RayTracingInOneWeekend.html). It takes you from nothing to creating an image like this:

![Final rendered image](/images/projects/craysiete/lindissimo.png)

It is quite easy to follow and super satisfying to see some basic renders. The final results is very "bare bones", so a typo will leave you with something wrong like this:

![Oopsie](/images/projects/craysiete/lindissirrissimo.png)

It only took like 1 hour to render, yey.
