---
layout: default
title: Projects
nav_order: 5
---

[Back](projects.md)

## Sensor System for Predictive Maintenance

Sensor module design, embedded development, and ML for predictive maintenance.  
It was developed in the scope of the [GreenAuto](https://www.agendagreenauto.pt/projeto/) Project.

This project explored the implementation of Predictive Maintenance in manufacturing environments that relied on legacy machinery lacking modern sensor capabilities. A wireless sensor system was developed using IoT hardware and Machine Learning algorithms to monitor equipment health through vibration, sound, and temperature data.

The system was designed specifically for Automated Guided Vehicles (AGVs) and nearby machines, with a focus on cost-effectiveness and space constraints. Data preprocessing techniques based on time-domain features were employed to minimize wireless data transmission. Supervised learning models delivered highly accurate anomaly detection results, while unsupervised models performed poorly. A comparative analysis of sensors with varying costs was also conducted to evaluate their performance.

This work demonstrated how emerging technologies could extend Industry 4.0 capabilities to older equipment, reducing downtime and optimizing maintenance schedules.

You can read the full dissertation here: [Dissertation](/documents/SensorSystemForPredictiveMaintenanceInIndustrialEnvironments.pdf). For a more condensed version, check out the [slides](/documents/Dissertation_Presentatio.pdf) for the presentation.

![testbed](/images/projects/sensor_system/testbed.jpg)

### Tech Explored

#### Embedded Systems

- Accelerometers
- Digital and Analog Microphones
- ADC
- IR Temperature Sensors
- WiFi
- SD Card
- EEPROM

#### Data Analysis

- Data Cleaning
- Time-Series Data
- Preprocessing
- Signal Processing
- ACABAR ISTO

### Highlights

- Got to work on several different layers:
  - Sensor selection
  - Firmware development
  - Data analysis
  - Machine Learning
  - Databases
- Very satisfying to work on a brand new project.
- Research is cool. Felt like I was doing work that can be useful for the future.
- Biggest project to date.

### Lowlights

- I only noticed that there was a typo in the title the day before presenting the dissertation. Still feel a bit embarrassed.
- I didn't have a lot of support, so I felt a bit lost, especially in the beginning.

### Lessons Learned

- You can't do everything. You can't test everything. Exploration is crucial, but it has to end at a certain time. Otherwise, you'll be stuck in the universe of possibilities.
- Code becomes legacy the moment it is written.
- One looks at a million datasets, but none ever truly matches your expectations.
