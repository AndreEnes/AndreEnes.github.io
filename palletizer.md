---
layout: default
title: Colour-Sorting Palletizer Robotic Arm
nav_order: 12
---

[Back](projects.md)

## Colour-Sorting Palletizer Robotic Arm

This project involved building and programming a robotic arm in a "Palletizer" configuration capable of sorting three objects based on their color. The system used a TCS3200 color sensor to identify each object's color, and a set of SG90 servo motors to control the robotic arm's movements. Once identified, the object was placed in the corresponding position for its color.

The arm's components and motion paths—including sensor, object pickup, and drop-off positions—were configurable via buttons and a 16x2 LCD, which also displayed real-time status updates. Configurations were stored in the EEPROM, enabling persistent memory between sessions.

To control four servo motors using limited PWM outputs, a transistor-multiplexing approach was implemented, optimizing pin usage on the Atmega328p microcontroller. Each servo had an associated state machine for movement control, and calibration modes were built in to allow fine-tuned positioning.

The color detection logic analyzed pulse frequency from the sensor using external timers to determine RGB values and classify the object. The system’s flow was structured as a finite state machine, allowing a seamless process from object detection to classification and placement.

Overall, the project demonstrated low-level embedded systems programming, motor control, sensor integration, and state-machine-based automation.

Here is a picture of the prototype (without any of the coloured pieces):

![prototype](/images/projects/palletizer/prototype.jpg)

And here is the hardware schematic:

![schematic](/images/projects/palletizer/schematic.png)

### Tech Explored

- AVR
- Servo motor control
- Color sensor
- Embedded Programming
- Electronics

### Highlights

- Inspired interest in embedded systems
- Used different types of components
- Hardware restrictions lead to creative solutions
  - The microcontroller only has 2 ports capable of running the servo motors, so separate transistors were used to make a "pin selector" to change how the pins were connected to each servo.

### Lowlights

- It was during the covid lockdown, so access to hardware tools was quite limited which made it harder to debug.
- The component precision was low, so the whole project was a bit finnicky.
- Single buttons make for annoying _"User Interfaces"_.

### Lessons Learned

- One must be careful with hardware, frying the chip is not difficult.
- Necessity really leads to ingenuity.
