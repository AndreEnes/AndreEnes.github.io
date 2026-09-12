---
layout: default
title: Ancelotti Robot - Real-Time Facial Gesture Animatronic
nav_order: 8
---

[Back](../)

## Ancelotti Robot: Real-Time Facial Gesture Animatronic

We built a robotic head, AnimaTRON 1.0, that imitated human facial movements in real time. A webcam fed [MediaPipe's Face Mesh](https://ai.google.dev/edge/mediapipe/solutions/vision/face_landmarker), which gave us the facial landmarks. We then mapped the normalised distances between those landmarks onto the eight servos in the head, covering eye movement, eyebrow position and mouth motion.

The servos were driven by a Pololu Mini Maestro controller. We first interfaced with it through an Arduino UNO, but the Maestro accepts serial commands directly, so we later removed the Arduino and drove it from Python alone.

The original plan was to use Botszy, a professional animatronic rigging platform, but we ran into compatibility problems and implemented the control ourselves instead.

The code is [on GitHub](https://github.com/AndreEnes/Ancelotti_Robot), and the [report](/documents/Ancelotti_Robot.pdf) has more detail.

![lindu](/images/projects/ancelotti/image21.gif)
![final](/images/projects/ancelotti/ancelotti.gif)

### Tech Explored

- MediaPipe's FaceMesh
- Face Capturing
- Digital to Analogue interface
- Servo motor control

### Highlights

- The project revisited an animatronic head from the year before. Starting from scratch turned out to be faster than building on what was there, and we got further with it.
- It was very easy to understand if something was going wrong by making a stupid face.
- The project was inspired by a friend of the professor who was a puppeteer who had worked on Star Wars. Very random.

### Lowlights

- We really tried to make Botszy work, but it was simply not very good. Scheduled to be released in 2022...
- The servo control was very sensitive to small changes. We could have implemented a signal attenuator to make it smoother.

### Lessons Learned

- ML models made for smartphones run really well on laptops.
- It is often worth it to see what else is available.
- Simple ideas and simple implementations make people happy.
