---
layout: default
title: Curriculum Vitae
nav_order: 14
---

[Home](../)

## Core Technical Skills

- **Programming Languages:** C/C++, Python, TypeScript, AssemblyScript, Bash, IEC 61131-3
- **Tools & Platforms:** Git, Docker, CI/CD (GitHub Actions, Zuul), CMake, Bazel, ROS, WebAssembly
- **Quality & Safety:** ASAN/TSAN, Valgrind, Static Analysis (Coverity, SonarQube)
- **Languages:** Portuguese (Native), English (C2), Spanish (B1), German (A2/B1)

---

## Work Experience

### Software Engineer – Critical Techworks

*January 2024 – Present*

[Crowd Data Collector](https://www.bmwgroup.com/en/innovation/connected-car.html) is BMW's project for in-vehicle data collection. The most unique component is an "app runtime for the car" that lets teams deploy small, sandboxed workloads over-the-air onto vehicle ECUs, delivering connected-vehicle features and data products at software speed instead of firmware-release cycles. Over 2+ years I've worked both sides of the platform: contributing to the runtime itself and designing the data-collection jobs that run on it.

#### Edge Computing & WebAssembly Platform

*September 2025 – Present*

Contributed to the hardware-agnostic C++14 / POSIX framework that orchestrates sandboxed WebAssembly workloads across multiple ECU architectures, **deployed on every BMW vehicle produced since 2025**, the [Neue Klasse](https://www.bmwgroup.com/en/company/neue-klasse.html).

- **Sandboxed Execution:** Built permission-gated system services in the JIT WebAssembly runtime, so a single compiled job runs sandboxed across every supported ECU.

- **Job Lifecycle:** Contributed to the cross-ECU job lifecycle and its API, from install and validation through update and uninstall.

- **Production Hardening:** Hardened the runtime with ASAN/TSAN, Valgrind, and Coverity, plus rate-limiting and RAM monitoring to keep jobs stable on constrained hardware.

- **AUTOSAR Metrics:** Added monitoring and metrics to a classic AUTOSAR ECU, extracting data over UDP via hardware debuggers.

#### In-Vehicle Data Collection Jobs & SDK Ecosystem

*March 2024 – September 2025*

Delivered vehicle-side data products across BMW's electric fleet and SDK tooling that accelerated job authoring across vehicle programs and releases.

- **Data Products:** Designed and shipped in-vehicle data-collection jobs end to end, from trigger and activation logic to signal processing and backend delivery.

- **SDK & Code Generation:** Co-designed a TypeScript SDK that turns CAN signal definitions into ready-to-use, typed code. Jobs read signals through a simple API instead of decoding CAN by hand.

- **Developer Experience:** Cut repetitive decoding work and kept generated code in step with evolving platform APIs.

#### C++ Academy

*January 2024 – March 2024*

- Three-month **intensive C++ programme** (OOP, concurrency, memory management, CI/CD with Docker and GitHub Actions).

---

## Projects

### Research Scholarship – GreenAuto Programme – DIGI2 Laboratory, FEUP

*December 2022 – October 2023*

Designed and developed a wireless IoT sensor system for predictive maintenance on Automated Guided Vehicles and nearby machinery in an industrial setting as part of the GreenAuto project for automotive industry sustainability.

- **Embedded Development:** Built firmware on Teensy and ESP-12E microcontrollers integrating accelerometers, digital/analog/ultrasonic microphones, and IR temperature sensors. Implemented signal processing pipelines (DFT, STFT, wavelet transforms), SD card logging, and real-time WiFi data streaming.
- **Data Pipeline:** Collected vibration, acoustic, and temperature data from industrial AGVs and machines; designed preprocessing with time-domain features to minimize wireless transmission overhead and ingestion into database systems.
- **ML Anomaly Detection:** Trained and deployed supervised models (XGBoost, Decision Trees) achieving accurate anomaly detection for fault identification. Evaluated unsupervised approaches (Isolation Forest, Autoencoders) and conducted comparative cost-performance analysis of sensor options.
- **Outcome:** Completed full dissertation and presentation materials; demonstrated extension of Industry 4.0 capabilities to legacy equipment, reducing downtime and optimizing maintenance scheduling.

### Summer Internship – ML Toolkit – DIGI2 Laboratory, FEUP

*July 2022 – September 2022*

Built a Python toolkit for solving generic regression problems by finding optimal input parameters for desired target outputs. Designed with a modularized ML architecture to support integration with multiple frontends beyond the initial Streamlit UI.

- **Model Training & Optimization:** Implemented XGBoost regressors with automated hyperparameter tuning via Hyperopt and simulated annealing (SciPy's dual_annealing) for finding optimal parameter configurations.
- **User Interface & Interpretability:** Developed an interactive Streamlit interface for model training, predictions, and parameter optimization. Integrated SHAP-based feature importance analysis with beeswarm plots for intuitive model explainability.
- **System Features:** Supported both continuous and discrete variables, incremental model retraining for reduced computational overhead, JSON-based project configuration templates for reproducible workflows.

### EBEC Porto 2022 – Challenge Lead

*October 2021 – May 2022*

Designed and executed the Team Design challenge for EBEC Porto 2022 (200+ participants, 24-hour format) in partnership with Saltpay (portable ATM software).

- **Challenge:** Developed an ATM prototype challenge where participants build devices for withdrawal selection, card insertion, and token dispensing.
- **Event Execution:** Coordinated 200+ participants at FEUP, provided technical support for electronics integration, circuit troubleshooting, and hardware issues.
- **Outcome:** Successfully delivered Portugal's largest engineering competition.

---

## Achievements

- **Top 10 – Hackacity 2023:** Smart city data challenge on CO₂ reduction – Porto Digital
- **2nd Place – Datattack 2023:** 24h data science challenge for Civil Protection – IEEE Student Branch Porto
- **3rd Place – EESTEC Challenge Porto 2022:** Machine learning competition on colour blindness detection

---

## Education

- **M.Sc. in Electrical and Computer Engineering** – FEUP (2021–2023)
  - Specialization: Industrial Automation, Embedded Systems, and Robotics
- **B.Sc. in Electrical and Computer Engineering** – FEUP (2018–2021)
- **Erasmus+ Exchange Semester** – Universidad de Sevilla (2022–2023)
