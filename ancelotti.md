---
layout: default
title: Projects
nav_order: 8
---

[Back](projects.md)

## Ancelotti Robot

This project explored the integration of facial gesture recognition and animatronic control by developing a system in which a robotic head imitated human facial movements in real time. Using a webcam and [MediaPipe's Face Mesh](https://ai.google.dev/edge/mediapipe/solutions/vision/face_landmarker), facial landmarks were detected and analyzed to track expressions such as eye movement, eyebrow position, and mouth motion.

Servo control of the animatronic head was achieved using a Pololu Mini Maestro controller, initially interfaced via an Arduino UNO and later optimized with a pure Python-based solution, reducing hardware complexity. The robotic head, AnimaTRON 1.0, included eight servos that replicated facial gestures based on normalized landmark distances.

Although originally intended to integrate Botszy, a professional animatronic rigging platform, the project faced compatibility issues and proceeded with a manual software implementation.

Check the [report](/documents/Ancelotti_Robot.pdf) for more information.

![lindu](/images/projects/ancelotti/image21.gif)
![final](/images/projects/ancelotti/ancelotti.gif)

### Tech Explored

- MediaPipe's FaceMesh
- Face Capturing
- Digital to Analog interface
- Servo motor control

### Highlights

- This project was basically a revamp of an older one made by a student in the prior year. We started from scratch and outdid his work with a fraction of the effort.
- It was very easy to understand if something was going wrong by making a stupid face.
- The project was inspired by a friend of the professor who was a puppeteer that had worked on Star Wars. Very random.

### Lowlights

- We really tried to make Botszy work, but it was simply not very good. It was schedule to be released in 2022...
- The servo control was very sensitive to small changes. We could have implemented a signal attenuator to make it smoother.

### Lessons Learned

- ML models made for smartphones run really well on laptops.
- It is often worth it to see what else is available.
- Simple ideas and simple implementations make people happy.
