---
layout: default
render_with_liquid: false
nav_order: 5
title: "Robotics Lesson 05 — Analog Inputs — Potentiometers & Sensors"
---

# Lesson 05: Analog Inputs — Potentiometers & Sensors

**Course:** Robotics & Arduino | **Lesson 05 of 12**

> Use analogRead to read potentiometers, LDR light sensors and temperature sensors.

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

1. Wire a potentiometer: outer pins to 5V and GND, middle pin (wiper) to A0.
2. Read: `int val = analogRead(A0);` — returns 0–1023.
3. Map to angle: `int angle = map(val, 0, 1023, 0, 180);` then print.
4. Use the pot to control LED brightness via PWM: `analogWrite(9, val/4);` (1023/4 ≈ 255).
5. Wire an LDR (light dependent resistor): LDR from 5V to A1, 10kΩ resistor from A1 to GND.
6. Read the LDR: bright light = high reading, darkness = low reading.
7. Make a nightlight: if LDR reading < 400, turn on LED.
8. Wire a TMP36 temperature sensor: Vs to 5V, GND to GND, Vout to A2.
9. Convert reading to Celsius: `float temp = (analogRead(A2) * 5.0 / 1024.0 - 0.5) * 100;`
10. Print temperature to Serial Monitor every second.

---

## Extension Challenges

- Build an automatic fan: temperature > threshold → turn on a small motor via relay.
- Add a threshold pot so the user adjusts the nightlight sensitivity with a knob.
- Display all three sensor values simultaneously on Serial Monitor as a data logger.

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

← [Back to Course](../index.html) | Next: [Lesson 06](lesson_06.html) →
