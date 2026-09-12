---
layout: default
title: Vehicle Bus Signal SDK
nav_order: 18
---

[Back](../)

## Vehicle Bus Signal SDK

I co-designed one of the SDKs that the [data collection jobs](../jobs/) are written with, and built most of it. It takes [CAN](https://en.wikipedia.org/wiki/CAN_bus) and [FlexRay](https://en.wikipedia.org/wiki/FlexRay) signal definitions and generates typed code, so a job subscribes to a signal and receives a named, typed value instead of decoding raw payloads by hand. Other SDKs do the same for other protocols, such as [SOME/IP](https://some-ip.com/). The SDK itself is written in TypeScript, but the code it generates is AssemblyScript, because that is what the jobs are written in. At the time of writing, around 40 developers write their jobs with it.

> This is a high-level description of the work. It intentionally omits proprietary interfaces, identifiers, and vehicle data.

### What It Does

A developer selects the signals a job needs. The SDK reads their definitions from the signal catalogue, validates them, and generates the decoders, subscriptions and simulation resources for them. A malformed definition fails at generation time, not in the vehicle.

### Bit-Level Decoding

CAN and FlexRay signals are packed at arbitrary bit offsets, and a field can span a byte boundary. The generated decoders read and combine the right bit fragments, then apply each signal's transformation and validity rules before handing the value to the job. A one-bit mistake in an offset does not crash anything, but it produces plausible values that are wrong.

### Testing

The SDK generates readable JSON signal references for simulation and converts them into binary traces, and back again, so the conversion itself can be tested in both directions. An integration job exercises the whole generated path.
