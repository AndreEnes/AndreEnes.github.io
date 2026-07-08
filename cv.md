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

Crowd Data Collector is BMW's in-vehicle application platform, an "app runtime for the car" that lets teams deploy small, sandboxed workloads over-the-air onto vehicle ECUs, delivering connected-vehicle features and data products at software speed instead of firmware-release cycles. Over 2+ years I've worked both sides of the platform: contributing to the runtime itself and designing the data-collection jobs that run on it.

#### Edge Computing & WebAssembly Platform

*September 2025 – Present*

Contributed to the hardware-agnostic C++14 / POSIX framework that orchestrates sandboxed WebAssembly workloads across multiple ECU architectures, **deployed on every BMW vehicle produced since 2025**, the [Neue Klasse](https://www.bmwgroup.com/en/company/neue-klasse.html).

Developed BMW's in-vehicle data collection platform: a hardware-agnostic C++14 Posix-based framework that orchestrates sandboxed WebAssembly workloads across multiple ECU architectures, **deployed on every BMW vehicle produced since September 2025**. Worked across the platform core runtime, the WebAssembly execution engine, and a vehicle-specific platform variant.

- **Platform Core:** Contributed to the cross-ECU foundation providing full job lifecycle management — receive, install, validate, execute, update, and uninstall — including job API interfaces, manifest handling, persistent data management, and diagnostics integration.
- **WebAssembly Runtime:** Developed permission-gated system services within the JIT-compiled WebAssembly runtime, enabling sandboxed near-native execution of data-collection jobs with cross-ECU portability from a single compiled artifact.
- **Vehicle Platform Variant:** Contributed to a platform variant deployed on next-generation vehicle ECUs, addressing platform identity separation across hardware lines, platform-specific message/data layout handling, and observability lifecycle via in-vehicle metrics and monitoring infrastructure.
- **Production Hardening:** Drove production hardening using ASAN/TSAN, Valgrind, and Coverity static analysis; worked with rate limiting, RAM monitoring, and metrics subsystems to ensure in-vehicle application stability.
- **AUTOSAR Platform Metrics:** Implemented monitoring and metrics infrastructure for a classic AUTOSAR ECU platform, extracting data via hardware debuggers and transmitting over UDP; addressed low-level multi-core communication challenges; contributed to custom testing infrastructure.
- **Integration & Testing:** Maintained CI pipelines with dual CMake/Bazel builds and automated sanitizer/analysis checks for safety-critical automotive software.

#### In-Vehicle Data Collection Jobs & SDK Ecosystem

*March 2024 – September 2025*

Developed in-vehicle data-collection jobs deployed across BMW's electric fleet, along with SDK tooling to accelerate job authoring — versioned per vehicle program and release.

- **Job Development:** Designed and implemented vehicle-side data products encompassing trigger/activation logic, signal collection and processing pipelines, and backend delivery contracts with event routing to backend receivers.
- **Code Generation & SDK Automation:** Developed TypeScript-based code generation tools that fetch manifest and API specifications to automatically generate automotive protocol handling code (including CAN message decoding). Integrated generated outputs into build pipelines with linting, unit, and integration testing to ensure quality and consistency.
- **Developer Experience:** Improved developer productivity by automating repetitive packet decoding tasks, reducing manual implementation effort and mismatch risks across systems. Continuously evolved generation templates and configuration to maintain alignment with evolving platform APIs and use-case requirements.
- **Safety-Critical Systems & DevOps:** Developed embedded scripts for telemetry collection in resource-constrained automotive systems. Contributed to CI/CD infrastructure, quality gates, and release workflows to support platform stability.

#### C++ Academy

*January 2024 – March 2024*

- Three-month intensive C++ programme (OOP, concurrency, memory management, CI/CD with Docker and GitHub Actions).

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
