---
layout: default
title: Metrics on an AUTOSAR ECU
nav_order: 15
---

[Back](../)

## Metrics on an AUTOSAR ECU

In 2026 my team took over the job runtime on BMW's [Heart of Joy](https://www.bmw.pt/pt/more-bmw/technology-and-innovation/bmw-heart-of-joy.html), a Classic AUTOSAR ECU. A team in China had built it to do the same work as [the core I work on](../runtime/). Unlike the Linux, QNX and Android ECUs the core runs on, the Heart of Joy is built around an Infineon AURIX microcontroller, so there is much less memory and CPU time to work with.

### The Metrics Service

The first new feature I built on the runtime was a metrics service that counts, for each [job](../jobs/), the data it sends and the storage it uses. On a microcontroller, measuring a job must not change its timing, so the cost has to be predictable rather than merely small.

### Validation

The same ECU runs the driving dynamics and manages the high-voltage battery, so the runtime has to be tested thoroughly enough that it never disturbs the other applications running on it. Some problems, such as timing, only appear on real hardware, so I tested the complete path on the target ECU, on a test bench I assembled. A JTAG debugger let me read the values in memory and check that each one was attributed to the right job.

### Other Work

I added persistent storage to the runtime's simulator, so jobs can be tested across restarts without hardware. I also integrated lifecycle and concurrency fixes into a vehicle release.
