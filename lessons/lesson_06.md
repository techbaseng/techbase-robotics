---
layout: default
render_with_liquid: false
nav_order: 6
title: "Robotics Lesson 06 — Controlling Motors — DC Motors & L298N"
---

# Lesson 06: Controlling Motors — DC Motors & L298N

**Course:** Robotics & Arduino | **Lesson 06 of 12**

> How DC motors work, using the L298N dual motor driver and controlling speed/direction.

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

1. DC motor basics: two wires, reverse polarity reverses direction, higher voltage = faster spin.
2. Why a driver? Arduino pins can't supply enough current for motors. The L298N provides up to 2A per channel.
3. L298N connections: ENA/ENB for speed (PWM), IN1/IN2 for motor A direction, IN3/IN4 for motor B.
4. Power: Motor supply (6–12V battery) to L298N Vs and GND. Arduino GND to L298N GND (common ground!).
5. Wire Motor A: IN1 → pin 7, IN2 → pin 8, ENA → pin 9 (PWM).
6. Forward: `digitalWrite(7,HIGH); digitalWrite(8,LOW); analogWrite(9,200);`
7. Backward: `digitalWrite(7,LOW); digitalWrite(8,HIGH); analogWrite(9,200);`
8. Stop: `digitalWrite(7,LOW); digitalWrite(8,LOW);`
9. Wire Motor B on IN3/IN4/ENB. Test both motors moving together.
10. Build helper functions: `void forward(int spd)`, `void backward(int spd)`, `void stopAll()`.

---

## Extension Challenges

- Add acceleration: gradually increase PWM from 0 to 255 over 2 seconds.
- Use a potentiometer to control motor speed in real time.
- Make the motors run at different speeds to cause the robot to curve left or right.

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

← [Back to Course](../index.html) | Next: [Lesson 07](lesson_07.html) →
