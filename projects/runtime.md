---
layout: default
title: A Portable Job Runtime for Vehicle ECUs
nav_order: 17
---

[Back](../)

## A Portable Job Runtime for Vehicle ECUs

Since 2025 I have worked on the C++ runtime core behind BMW's Crowd Data Collector, the part that installs, validates and executes [data collection jobs](../jobs/) on vehicle ECUs. The core ships in every vehicle of BMW's [Neue Klasse](https://www.bmwgroup.com/en/company/neue-klasse.html).

> This is a high-level description of the work. It intentionally omits proprietary interfaces, identifiers, and vehicle data.

I contributed to it as part of a larger engineering team. I did not design its architecture, so this is a description of a codebase I worked on rather than one I own.

### The Idea

A vehicle does not have one kind of ECU. It has several, with different hardware, different security mechanisms, different operating systems. One is based on Arch Linux, one on QNX and one on Android. The obvious approach is to write the job management logic once per ECU and then maintain all of them separately.

Instead, the core owns the reusable part: receiving a job, checking that it is valid for this vehicle, installing it, keeping it so that it survives a restart, running it, and releasing what it held when the vehicle shuts down. Everything platform-specific sits behind interfaces that each ECU implements for itself, and the core depends on the interface rather than on any implementation.

The idea itself is not new. What makes it demanding is where it ships. This is automotive software, developed under ISO 26262 and ASPICE, on hardware with little memory or CPU to spare. That leaves little room to check things while the code runs, so most of the checking happens before it ships, through static analysis and sanitisers in testing.

Not everything is caught before shipping. What gets through usually comes back from the test fleet as a coredump and logs, not as a reproduction.

None of that changes the rule: a job that misbehaves must never affect the vehicle.

### What I Worked On

- Permission-gated system services in the WebAssembly runtime, so that a job can only reach what its manifest declares.
- Parts of the job lifecycle and the API around it, covering installation, validation, update and removal.
- Hardening the runtime with tools such as Valgrind, ASAN and Coverity.
- Root-causing and fixing bugs from coredumps and logs, once the integration teams ruled out their own code.
- Rate limiting and memory monitoring, so that one job cannot spend what the rest of the ECU needs.
