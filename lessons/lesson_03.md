---
layout: default
render_with_liquid: false
nav_order: 3
title: "Robotics Lesson 03 — Your First Sketch — Blinking an LED"
---

# Lesson 03: Your First Sketch — Blinking an LED

**Course:** Robotics & Arduino | **Lesson 03 of 12**

> Master digitalWrite, delay, setup(), loop() and build 3 LED projects.

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

1. Wire an external LED: long leg (anode) → 220Ω resistor → pin 7. Short leg (cathode) → GND.
2. Write your own Blink from scratch. Use `pinMode(7, OUTPUT)` in setup.
3. In loop: `digitalWrite(7, HIGH); delay(1000); digitalWrite(7, LOW); delay(1000);`
4. Upload. External LED blinks at 1Hz.
5. Now add a second LED on pin 8. Make them alternate (one on, one off).
6. Build a traffic light: 3 LEDs (red/pin 5, yellow/pin 6, green/pin 7). Sequence: green 5s → yellow 1s → red 5s → repeat.
7. Add a `for` loop that cycles through 3 LEDs: `for(int i=5; i<=7; i++) { ... }`.
8. Use the Serial Monitor to print a message each time the light changes.
9. Use a variable `int delayTime = 1000;` and change it to affect all delays at once.
10. Add a function `void flashAll()` that flashes all 3 LEDs simultaneously.

---

## Extension Challenges

- Build a knight-rider scanner: 5 LEDs sweep back and forth.
- Create a reaction time tester: LED lights up after a random delay — press a button as fast as possible.
- Build a binary counter: 4 LEDs count from 0 to 15 in binary.

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

← [Back to Course](../index.html) | Next: [Lesson 04](lesson_04.html) →
