---
layout: default
title: Automotive Metrics on the Heart of Joy ECU
nav_order: 15
---

[Back](../)

## Automotive Metrics on the Heart of Joy ECU

During 2026 I implemented an embedded metrics service for BMW's Crowd Data Collector, together with the hardware-in-the-loop tests that validated it on the target ECU, BMW's [Heart of Joy](https://www.bmw.pt/pt/more-bmw/technology-and-innovation/bmw-heart-of-joy.html), a Classic AUTOSAR platform.

That ECU runs its own runtime, built by a team in China to do the same job as [the core I work on](../runtime/). It is being handed over to my team, and the metrics are how we will see it running.

> This is a high-level description of the work. It intentionally omits proprietary interfaces, identifiers, and vehicle data.

### The Service

For each [job](../jobs/), the service counts the amount of data sent and the amount of memory used. An ECU has very little memory, CPU time or bandwidth to spare, and measuring a job must not change its timing, so the cost has to be predictable rather than merely small. A job only updates a metric once the operation has actually succeeded, so the numbers describe what happened rather than what was attempted. The job does not wait for them to be sent: the values are picked up at a fixed interval, handed to another ECU, and forwarded to the backend from there.

### Hardware-in-the-Loop Validation

Simulation alone is not enough for validating resource-constrained ECU software: timing and the transport underneath only misbehave on real hardware, so I tested the complete path on the target ECU. A JTAG debugger on the bench let me halt it and read the values in memory rather than infer them from the other end. The tests installed controlled jobs, made them send data and use memory, and checked that each value reached the vehicle interface attributed to the right job and at the right interval.
