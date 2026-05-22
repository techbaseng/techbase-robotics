---
layout: default
render_with_liquid: false
nav_order: 1
title: "Robotics Lesson 01 — Introduction to Robotics & Arduino"
---

# Lesson 01: Introduction to Robotics & Arduino

**Course:** Robotics & Arduino | **Lesson 01 of 12**

> What robots are, how Arduino works, installing the IDE and running your first sketch.

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

1. What is a robot? Autonomous vs remote-controlled systems and real-world examples.
2. Overview of the Arduino Uno R3: microcontroller, digital pins (0–13), analog pins (A0–A5), power pins and USB.
3. Download and install the Arduino IDE from arduino.cc/en/software.
4. Connect your Arduino to your computer via USB. Select the correct board and COM port under Tools.
5. Open the Blink example: File → Examples → 01.Basics → Blink.
6. Review the sketch structure: `setup()` runs once, `loop()` runs forever.
7. Upload the sketch (click →). The built-in LED on pin 13 should blink every second.
8. Modify the delay values (e.g. 100 and 900) and re-upload. Observe the change.
9. Review basic electronics: voltage (V), current (mA), resistance (Ω) and Ohm's Law.
10. Identify and label all components in your starter kit.

---

## Extension Challenges

- Write a sketch that blinks in an SOS morse code pattern (... --- ...).
- Change the blink speed using a `for` loop counting from 1000ms down to 100ms.
- Add a second LED on pin 12 that blinks the opposite pattern.

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

← [Back to Course](../index.html) | Next: [Lesson 02](lesson_02.html) →
