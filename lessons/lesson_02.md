---
layout: default
render_with_liquid: false
nav_order: 2
title: "Robotics Lesson 02 — Understanding the Arduino Board"
---

# Lesson 02: Understanding the Arduino Board

**Course:** Robotics & Arduino | **Lesson 02 of 12**

> Deep dive into pins, power, digital vs analog and common board variants.

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

1. Digital pins: can be INPUT or OUTPUT, read HIGH (5V) or LOW (0V).
2. Analog pins A0–A5: read values 0–1023 (10-bit ADC) representing 0–5V.
3. PWM pins (marked ~): 3, 5, 6, 9, 10, 11 — output simulated analog using `analogWrite()`.
4. Power pins: 5V, 3.3V, GND. Vin accepts 7–12V from battery.
5. Current limits: max 40mA per pin, 200mA total from all pins.
6. Build a basic LED circuit: LED + 220Ω resistor from pin 9 to GND.
7. Use `analogWrite(9, 128)` for 50% brightness (PWM value 0–255).
8. Use `analogRead(A0)` to read the potentiometer wired to A0.
9. Print the potentiometer value to Serial Monitor at 9600 baud.
10. Map the potentiometer value to LED brightness: `analogWrite(9, map(val,0,1023,0,255))`.

---

## Extension Challenges

- Use PWM to fade an LED in and out smoothly in a loop.
- Wire two LEDs and make them inversely proportional to each other using one potentiometer.
- Read the temperature from the built-in Arduino chip and display it on Serial Monitor.

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

← [Back to Course](../index.html) | Next: [Lesson 03](lesson_03.html) →
