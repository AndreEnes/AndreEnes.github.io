---
layout: default
title: Sensor System for Industrial Predictive Maintenance
nav_order: 5
---

[Back](../)

## Sensor System for Industrial Predictive Maintenance

My master's dissertation, developed within the [GreenAuto](https://www.agendagreenauto.pt/projeto/) project. I designed a wireless sensor system that monitors the condition of industrial machines through vibration, sound and temperature, so that predictive maintenance can be applied to older equipment that was never built with sensors in mind.

The targets were Automated Guided Vehicles and the machines around them, which meant the modules had to be cheap and small enough to be added to equipment already in service. I built the firmware on Teensy and ESP-12E microcontrollers, with accelerometers, analogue, digital and ultrasonic microphones, and an infrared temperature sensor. To keep the wireless traffic down, the modules computed time-domain features on the device instead of streaming the raw signals.

For the detection itself, the supervised models worked and the unsupervised ones did not. XGBoost was the best, reaching an F1 of 0.99 on the most imbalanced dataset (9% anomalies, temperature excluded). One-Class SVM, Isolation Forest and Local Outlier Factor were all clearly worse, with precision as low as 0.06. I also compared sensors at different price points, to see how much detection performance the cheaper components actually cost.

You can read the full dissertation here: [Dissertation](/documents/SensorSystemForPredictiveMaintenanceInIndustrialEnvironments.pdf). For a more condensed version, check out the [slides](/documents/Dissertation_Presentatio.pdf) for the presentation.

![testbed](/images/projects/sensor_system/testbed.jpg)

### Tech Explored

#### Embedded Systems

- Accelerometers, microphones (analogue, digital, ultrasonic), IR temperature sensors
- Microcontrollers (Teensy, ESP-12E), ADC, EEPROM, SD card
- WiFi communication, power management, level shifting
- Custom hardware testbeds

#### Signal Processing

- Discrete and Short-Time Fourier Transforms (DFT, STFT)
- Wavelet, Empirical Mode, and Hilbert-Huang Transforms
- Envelope detection, signal filtering, time-frequency analysis

#### Machine Learning & Data Analysis

- Time-series preprocessing, outlier removal
- Supervised models: XGBoost, Random Forest, AdaBoost, k-NN, SVM
- Unsupervised models: Isolation Forest, One-Class SVM, Local Outlier Factor
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
