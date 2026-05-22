---
layout: default
render_with_liquid: false
nav_order: 7
title: "Robotics Lesson 07 — Ultrasonic Distance Sensor (HC-SR04)"
---

# Lesson 07: Ultrasonic Distance Sensor (HC-SR04)

**Course:** Robotics & Arduino | **Lesson 07 of 12**

> Measure distance using echo timing, wire the HC-SR04 and read in centimetres.

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

1. HC-SR04 pins: VCC (5V), GND, Trig (trigger), Echo (receive).
2. Wire: VCC → 5V, GND → GND, Trig → pin 10, Echo → pin 11.
3. Principle: Trig sends a 10µs pulse. Sensor emits 8 ultrasound bursts. Echo goes HIGH until return.
4. Duration of Echo HIGH = round-trip time in microseconds.
5. Formula: distance (cm) = duration / 58.0 (based on speed of sound).
6. Code: `digitalWrite(TRIG, LOW); delayMicroseconds(2); digitalWrite(TRIG, HIGH); delayMicroseconds(10); digitalWrite(TRIG, LOW);`
7. `long duration = pulseIn(ECHO, HIGH);`
8. `float distance = duration / 58.0;`
9. Print distance to Serial Monitor. Test by moving your hand closer and further away.
10. Add an LED that turns red when distance < 20cm (obstacle nearby).

---

## Extension Challenges

- Add a buzzer that beeps faster as distance decreases (like a parking sensor).
- Log 10 readings and display the average to reduce noise.
- Mount the sensor on a servo that sweeps to scan a 180° area.

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

← [Back to Course](../index.html) | Next: [Lesson 08](lesson_08.html) →
