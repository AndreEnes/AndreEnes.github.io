---
layout: default
title: Curriculum Vitae
nav_order: 14
---

[Home](../)

## Core Technical Skills

- **Domains:** Safety-critical automotive, embedded and edge systems, applied machine learning
- **Programming Languages:** C/C++, Python, TypeScript, AssemblyScript, Bash
- **Tools & Platforms:** Git, Docker, CI/CD (GitHub Actions, Zuul), CMake, Bazel, ROS, WebAssembly, JTAG Debuggers
- **Quality & Safety:** ASAN/TSAN, Valgrind, Static Analysis (Coverity, SonarQube)
- **Languages:** Portuguese (Native), English (C2), Spanish (B1), German (A2, studying for B1)

---

## Work Experience

### Software Engineer – Critical Techworks

*January 2024 – Present*

[Crowd Data Collector](https://www.bmwgroup.com/en/innovation/connected-car/data-ecosystem.html) is BMW's project for in-vehicle data collection. Its most unusual component is an "app runtime for the car": teams deploy small sandboxed workloads over the air onto vehicle ECUs. New features do not have to wait for a firmware release. For almost three years I have worked on both sides of it, the runtime itself and the jobs that run on top of it, together with teams in Germany and China.

#### Edge Computing & WebAssembly Platform

*September 2025 – Present*

A hardware-agnostic C++14 and POSIX [framework](/projects/runtime/) that orchestrates sandboxed WebAssembly workloads across several ECU architectures. It is **deployed on every BMW [Neue Klasse](https://www.bmwgroup.com/en/company/neue-klasse.html) vehicle**.

- **Sandboxed Execution:** Built permission-gated system services in the WebAssembly runtime. A job is compiled once and then runs sandboxed on every supported ECU.
- **Job Lifecycle:** Contributed to the cross-ECU job lifecycle and its API, covering install, validation, update and uninstall.
- **Production Hardening:** Hardened the runtime with ASAN, TSAN, Valgrind, Coverity and SonarQube, run through the Zuul CI pipelines. Added rate-limiting and RAM monitoring to keep jobs inside the memory budget of constrained hardware.
- **Observability:** Built a [per-job metrics service](/projects/metrics/) for the platform's runtime on BMW's Heart of Joy, a Classic AUTOSAR ECU, and validated the whole path on the target with hardware-in-the-loop tests and a JTAG debugger.

#### In-Vehicle Data Collection Jobs & SDK Ecosystem

*March 2024 – September 2025*

- **Data Products:** Designed and shipped over a dozen [in-vehicle data-collection jobs](/projects/jobs/) across BMW's electric fleet, several of them end to end: trigger and activation logic, signal processing, and delivery to the backend.
- **SDK & Code Generation:** Co-designed and built most of a [TypeScript SDK](/projects/sdk/) that turns CAN and FlexRay signal definitions into typed AssemblyScript code. Jobs receive named, typed signals instead of decoding raw payloads by hand.
- **API Evolution:** Kept the generated code in step with the platform APIs as they changed across vehicle programmes and releases.

#### C++ Academy

*January 2024 – March 2024*

Three-month intensive C++ programme at the start of the role, covering OOP, concurrency, memory management, and CI/CD with Docker and GitHub Actions.

---

## Academic Experience

### Research Scholarship – GreenAuto Programme – DIGI2 Laboratory, FEUP

*December 2022 – October 2023*

My M.Sc. dissertation, done on a research scholarship within the GreenAuto project for automotive industry sustainability. A wireless IoT sensor system for predictive maintenance on Automated Guided Vehicles and the machinery around them.

- **Embedded Firmware:** Built Teensy and ESP-12E firmware collecting vibration, sound and temperature, with DFT, STFT and wavelet processing on the device, SD card logging and real-time WiFi streaming.
- **Anomaly Detection:** Benchmarked five supervised and three unsupervised models. XGBoost was the best, reaching an F1 of 0.99 on the most imbalanced dataset (9% anomalies); the unsupervised models could not separate the faults.
- **Data Pipeline:** Chose time-domain features for preprocessing, mainly to keep the wireless traffic down.
- **Outcome:** Showed that predictive maintenance can be retrofitted to legacy AGV equipment. Full dissertation and presentation available on the [project page](/projects/sensorSystem/).

### Summer Internship – ML Toolkit – DIGI2 Laboratory, FEUP

*July 2022 – September 2022*

A Python toolkit that finds the input parameters producing a desired target output for a regression problem.

- XGBoost regressors with hyperparameter tuning through Hyperopt, and simulated annealing (SciPy's dual_annealing) to search the parameter space.
- SHAP feature-importance analysis, so the model could be inspected rather than taken on trust.
- A Streamlit interface, with the machine learning kept separate from the UI so that it could be driven from another frontend.

---

## Volunteering

### President of the General Assembly – BEST Porto

*2022 – 2023*

Chaired the general assembly of [BEST Porto](https://bestporto.org/), the local branch of the [Board of European Students of Technology](https://best.eu.org/index.jsp).

### EBEC Porto 2022 – Challenge Lead

*October 2021 – May 2022*

Designed and ran the Team Design challenge for EBEC Porto 2022, the largest engineering competition in Portugal, in partnership with Saltpay.

- Wrote the challenge itself: teams built an ATM prototype handling withdrawal selection, card insertion and token dispensing.
- Coordinated more than 200 participants over the 24-hour format at FEUP, and provided the on-site electronics support, from circuit troubleshooting to failing hardware.

---

## Achievements

- **Top 10 – Hackacity 2023:** Smart city data challenge on CO₂ reduction (Porto Digital)
- **2nd Place – Datattack 2023:** 24h data science challenge for Civil Protection (IEEE Student Branch Porto)
- **3rd Place – EESTEC Challenge Porto 2022:** Machine learning competition on colour blindness detection

---

## Education

- **M.Sc. in Electrical and Computer Engineering** – FEUP (2021–2023)
  - Specialisation: Industrial Automation, Embedded Systems, and Robotics, including IEC 61131-3 PLC programming
  - Dissertation: [Sensor System for Predictive Maintenance in Industrial Environments](/documents/SensorSystemForPredictiveMaintenanceInIndustrialEnvironments.pdf)
- **B.Sc. in Electrical and Computer Engineering** – FEUP (2018–2021)
- **Erasmus+ Exchange Semester** – Universidad de Sevilla (2022–2023, during the M.Sc.)
