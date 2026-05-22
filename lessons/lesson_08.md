---
layout: default
render_with_liquid: false
nav_order: 8
title: "Robotics Lesson 08 — Servo Motors & Robotic Arms"
---

# Lesson 08: Servo Motors & Robotic Arms

**Course:** Robotics & Arduino | **Lesson 08 of 12**

> Control servo angle with the Servo library, sweep motion and build a simple arm.

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

1. Servo basics: brushless motor with positional control (0–180°), built-in feedback loop.
2. Three wires: Power (red → 5V), GND (brown/black → GND), Signal (yellow/orange → pin).
3. Include the Servo library: `#include <Servo.h>` and `Servo myServo;`
4. In setup: `myServo.attach(9);`
5. Set angle: `myServo.write(90);` — servo moves to 90°.
6. Sweep: `for(int angle=0; angle<=180; angle+=1) { myServo.write(angle); delay(15); }`
7. Reverse sweep back from 180° to 0°.
8. Control with potentiometer: `int angle = map(analogRead(A0), 0, 1023, 0, 180); myServo.write(angle);`
9. Wire a second servo for a pan-tilt system (horizontal + vertical).
10. Build a basic arm: two servos mounted at base and elbow, controlled by two potentiometers.

---

## Extension Challenges

- Add a third servo as a gripper that opens/closes on button press.
- Program the arm to move through a saved sequence of positions.
- Mount the HC-SR04 on the pan servo to create a scanning radar.

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

← [Back to Course](../index.html) | Next: [Lesson 09](lesson_09.html) →
