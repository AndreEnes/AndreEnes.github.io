---
layout: default
title: Colour-Sorting Palletiser Robotic Arm
nav_order: 12
---

[Back](../)

## Colour-Sorting Palletiser Robotic Arm

A robotic arm in a palletiser configuration that sorts objects by colour. A TCS3200 sensor reads the colour of each piece and the arm drops it in the position assigned to that colour, driven by SG90 servos.

The interesting constraint was the Atmega328p. It had two PWM outputs available and the arm needed four servos, so I used transistors to switch which pair of servos those outputs were driving. Each servo had its own state machine, plus a calibration mode for fine positioning.

Colour detection worked from the sensor's output frequency, measured with the external timers and converted into RGB values to classify the piece. The whole flow, from detecting an object to placing it, ran as a finite state machine.

The positions for the sensor, the pickup point and each drop-off were configurable through buttons and a 16x2 LCD, which also showed the current status. Those settings were stored in EEPROM, so they survived a power cycle.

Here is a picture of the prototype (without any of the coloured pieces):

![prototype](/images/projects/palletizer/prototype.jpg)

And here is the hardware schematic:

![schematic](/images/projects/palletizer/schematic.png)

### Tech Explored

- AVR
- Servo motor control
- Colour sensor
- Embedded Programming
- Electronics

### Highlights

- Inspired interest in embedded systems
- Used different types of components
- Hardware restrictions led to creative solutions
  - The microcontroller only has 2 ports capable of running the servo motors, so separate transistors were used to make a "pin selector" to change how the pins were connected to each servo.

### Lowlights

- It was during the covid lockdown, so access to hardware tools was quite limited which made it harder to debug.
- The component precision was low, so the whole project was a bit finicky.
- Single buttons make for annoying _"User Interfaces"_.

### Lessons Learned

- One must be careful with hardware, frying the chip is not difficult.
- Necessity really leads to ingenuity.
