---
layout: default
title: In-Vehicle Data Collection Jobs
nav_order: 16
---

[Back](../)

## In-Vehicle Data Collection Jobs

For about a year and a half I designed and shipped more than a dozen vehicle-side data collection jobs for BMW's Crowd Data Collector. The jobs covered the safety, powertrain, high-voltage and thermal domains, reading signals over [SOME/IP](https://some-ip.com/) and PDU-based interfaces. They are written in AssemblyScript with the open-source toolchain from [wasm-ecosystem](https://github.com/wasm-ecosystem), compiled to WebAssembly, and run sandboxed on ECUs in production vehicles. Each job turns raw ECU signals into structured events. Those events go to many places: engineering teams, My BMW App, insurance companies, Roadside Assistance, etc.

> This is a high-level description of the work. It intentionally omits proprietary interfaces, identifiers, and vehicle data.

### What a Job Does

A job subscribes to vehicle signals and diagnostic data. Signals arrive as named, typed values, decoded by [generated code](../sdk/) rather than by hand. The job decides whether the current situation is worth recording, and sends that information to the backend as a typed Avro event. It does not send everything it reads. It can take a signal at a fixed rate, or aggregate it over a window and send a single value at the end. Thresholds, rates and activation conditions live in configuration, so changing them does not mean rewriting the job.

### Designing a Job

The triggers for collecting data come in a few shapes: mileage and elapsed time, a monitored value crossing a threshold, and context buffered around a sudden event.

Two constraints shape most of a job's design:

- **Signal quality.** A signal can be present and still be stale, unavailable or implausible. Treating it as valid corrupts the dataset without any visible error.
- **Shutdown.** The vehicle can shut down in the middle of anything. The runtime releases whatever the job held, but the job decides whether what it has collected so far is worth sending before that happens.

I tested each job three ways: the logic with unit tests, the vehicle behaviour in simulation, and the cases that mattered in a real vehicle, both normal operation and failure scenarios.
