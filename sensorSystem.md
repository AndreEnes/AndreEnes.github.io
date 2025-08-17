---
layout: default
title: Sensor System for Industrial Predictive Maintenance
nav_order: 5
---

[Back](projects.md)

## Sensor System for Industrial Predictive Maintenance

Sensor module design, embedded development, and ML for predictive maintenance.  
It was developed in the scope of the [GreenAuto](https://www.agendagreenauto.pt/projeto/) Project.

This project explored the implementation of Predictive Maintenance in manufacturing environments that relied on legacy machinery lacking modern sensor capabilities. A wireless sensor system was developed using IoT hardware and Machine Learning algorithms to monitor equipment health through vibration, sound, and temperature data.

The system was designed specifically for Automated Guided Vehicles (AGVs) and nearby machines, with a focus on cost-effectiveness and space constraints. Data preprocessing techniques based on time-domain features were employed to minimize wireless data transmission. Supervised learning models delivered highly accurate anomaly detection results, while unsupervised models performed poorly. A comparative analysis of sensors with varying costs was also conducted to evaluate their performance.

This work demonstrated how emerging technologies could extend Industry 4.0 capabilities to older equipment, reducing downtime and optimizing maintenance schedules.

You can read the full dissertation here: [Dissertation](/documents/SensorSystemForPredictiveMaintenanceInIndustrialEnvironments.pdf). For a more condensed version, check out the [slides](/documents/Dissertation_Presentatio.pdf) for the presentation.

![testbed](/images/projects/sensor_system/testbed.jpg)

### Tech Explored

#### Embedded Systems

- Accelerometers, microphones (analog, digital, ultrasonic), IR temperature sensors
- Microcontrollers (Teensy, ESP-12E), ADC, EEPROM, SD card
- WiFi communication, power management, level shifting
- Custom hardware testbeds

#### Signal Processing

- Discrete and Short-Time Fourier Transforms (DFT, STFT)
- Wavelet, Empirical Mode, and Hilbert-Huang Transforms
- Envelope detection, signal filtering, time-frequency analysis

#### Machine Learning & Data Analysis

- Time-series preprocessing, outlier removal
- Supervised models: XGBoost, Decision Trees
- Unsupervised models: Isolation Forest, Autoencoders
- Anomaly detection, dataset creation, evaluation metrics

#### Software & Infrastructure

- Firmware design with finite state machines
- SD card logging, real-time WiFi streaming
- Database integration, model automation scripts

#### Research & System Design

- Predictive vs. preventive vs. reactive maintenance
- Sensor selection and cost-performance analysis
- Integration with legacy industrial systems

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
- Researching related concepts was challenging due to significant overlap and subtle differences between them. To clarify these relationships, I even created a diagram that maps out how the concepts connect:

![nomenclature](/images/projects/sensor_system/nomenclature.png)

### Lessons Learned

- You can't do everything. You can't test everything. Exploration is crucial, but it has to end at a certain time. Otherwise, you'll be stuck in the universe of possibilities.
- Code becomes legacy the moment it is written.
- One looks at a million datasets, but none ever truly matches your expectations.
