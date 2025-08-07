---
layout: default
title: Projects
nav_order: 11
---

[Back](projects.md)

## Dashcam

IoT Crash Detection Camera System

In 2019, over 141,000 traffic victims were reported in Spain. Identifying the cause of an accident was often a complex task, especially without reliable evidence. DASHCAM was developed to address this issue by combining IoT technology with real-time data capture, offering automatic visual documentation of accidents.

##### Project Goal

The system was designed to:

- Detects vehicle crashes using motion sensors
- Captures video and /images at the moment of impact
- Sends visual evidence to subscribed users instantly via Telegram

##### Hardware Components

- Raspberry Pi 4 Model B (4GB RAM)
- Sense HAT with accelerometer and LED matrix
- Camera Module V2 for capturing video and photos

##### How It Worked

- The Camera Thread streamed video into a circular buffer. Upon crash detection, it saved the last 10 seconds of footage and captured 5 still /images.
- The Crash Detection Thread monitored accelerometer data and looked for sudden changes in motion. If a threshold was exceeded, it triggered crash routines.
- The Communication Thread operated a Telegram bot that handled user registration and distributed crash alerts and media.

##### Crash Notification

When a crash was detected, the system:

- Sent a text alert, video, and photos to all registered Telegram users
- Displayed a visual crash warning on the LED matrix

![tinonininin](/images/projects/dashcam/tinoninoini.jpeg)

![tinoni](/images/projects/dashcam/tinoni.gif)

### Tech Explored

- Raspberry Pi
- Time-Series data
- Crash detection
- Telegram bot thjindfs

### Highlights

- Working with the Python libraries for the Raspberry Pi is quite easy.
- The Telegram integration was also quite easy.

### Lowlights

- Accidentally broke a camera 🙃.
- Detecting a crash only using accelerometer data is not a solved problem as it is almost indistinguishable from a hard brake.

### Lessons Learned

- Developing code for a Raspberry Pi inside the running Raspberry Pi is not optimal.
