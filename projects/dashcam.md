---
layout: default
title: IoT Dashcam Crash Detection System
nav_order: 11
---

[Back](../)

## IoT Dashcam Crash Detection System

Spain recorded more than 141,000 traffic casualties in 2019. Identifying the cause of an accident is difficult without reliable evidence, so we built a dashcam that detects the impact on its own and sends the footage out automatically.

### Hardware

- Raspberry Pi 4 Model B (4GB RAM)
- Sense HAT, which provided the accelerometer and the LED matrix
- Camera Module V2

### How It Worked

The system ran three threads in parallel.

The camera thread continuously wrote video into a circular buffer. When a crash was detected, it saved the last 10 seconds from that buffer and captured 5 still images.

The crash detection thread monitored the accelerometer for sudden changes in motion. If the reading crossed a threshold, it triggered the crash routine.

The communication thread ran a Telegram bot. It handled user registration and then sent the alert, the video and the images to every subscribed user. The LED matrix displayed a warning at the same time.

![tinonininin](/images/projects/dashcam/tinoninoini.jpeg)

![tinoni](/images/projects/dashcam/tinoni.gif)

### Tech Explored

- Raspberry Pi
- Time-Series data
- Crash detection
- Telegram bot API
- Multithreading

### Highlights

- Working with the Python libraries for the Raspberry Pi is quite easy.
- The Telegram integration was also quite easy.

### Lowlights

- Accidentally broke a camera 🙃.
- Detecting a crash only using accelerometer data is not a solved problem as it is almost indistinguishable from a hard brake.

### Lessons Learned

- Developing code for a Raspberry Pi inside the running Raspberry Pi is not optimal.
