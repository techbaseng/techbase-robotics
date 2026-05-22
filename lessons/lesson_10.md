---
layout: default
render_with_liquid: false
nav_order: 10
title: "Robotics Lesson 10 — Infrared Remote Control"
---

# Lesson 10: Infrared Remote Control

**Course:** Robotics & Arduino | **Lesson 10 of 12**

> Decode IR signals with the IRremote library and map buttons to robot actions.

---

## Learning Objectives

By the end of this lesson you will be able to:

- Understand the hardware and concepts introduced in this lesson
- Wire the required components correctly using the provided diagram
- Write and upload an Arduino sketch that implements the lesson goals
- Debug and modify the code to handle different conditions

---

## Hardware Required

See the Kit List on the [course overview page](../index.html) for the full component list. For this lesson you will specifically need the components mentioned in the steps below.

---

## Step-by-Step Guide

1. Install the IRremote library: Sketch → Include Library → Manage Libraries → search IRremote.
2. Wire IR receiver: VCC → 5V, GND → GND, Output → pin 2.
3. Include: `#include <IRremote.hpp>` and create `IRrecv irrecv(2);`
4. In setup: `irrecv.enableIRIn();`
5. In loop: `if (irrecv.decode()) { Serial.println(irrecv.decodedIRData.command); irrecv.resume(); }`
6. Press each button on your remote and note its code in Serial Monitor.
7. Map codes to actions using a `switch` statement: e.g. code 0x18 = forward, 0x52 = backward.
8. Connect motor functions: pressing up arrow → forward, down → backward, left → turn left, right → turn right.
9. Add a stop button and a horn (buzzer) button.
10. Adjust speed with volume +/- buttons using a speed variable (50–255).

---

## Extension Challenges

- Add a toggle button that switches between manual (remote) and autonomous (obstacle avoid) mode.
- Programme a button to make the robot spin 360° precisely.
- Record a button sequence that plays back a stored movement routine.

---

## Review Questions

1. Explain in your own words what this lesson's main component does.
2. What would happen if you changed one key parameter in your sketch?
3. How does this lesson's content connect to the final robot build in Lesson 12?

---

## Troubleshooting Tips

- **Nothing happens when I upload:** Check board and COM port under Tools → Board and Tools → Port.
- **Component not responding:** Check wiring. Start from power (5V/GND) and trace to each pin.
- **Erratic readings:** Check for loose connections. Add `delay(100)` to stabilise sensor reads.
- **Motor runs one way only:** Swap IN1/IN2 in your code or physically swap the motor wires.

---

← [Back to Course](../index.html) | Next: [Lesson 11](lesson_11.html) →
