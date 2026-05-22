---
layout: default
render_with_liquid: false
nav_order: 12
title: "Robotics Lesson 12 — Capstone — Full Autonomous Obstacle-Avoiding Robot"
---

# Lesson 12: Capstone — Full Autonomous Obstacle-Avoiding Robot

**Course:** Robotics & Arduino | **Lesson 12 of 12**

> Complete chassis assembly, full wiring, production code, calibration and testing.

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

1. Final assembly: attach motors to chassis, mount wheels, secure Arduino and L298N with screws or Velcro.
2. Cable management: use cable ties to secure wires away from wheels and motors.
3. Power: connect 9V or 12V battery pack to L298N Vs. Connect Arduino via USB bank or Vin.
4. Full wiring checklist: all IN1-IN4, ENA/ENB, HC-SR04 Trig/Echo, common GND confirmed.
5. Load production code: combines all functions from Lessons 07, 08, 10 and 11 into one clean sketch.
6. Add a startup sequence: robot beeps, all LEDs flash once, then begins autonomous mode.
7. Calibration: run on test track, adjust THRESHOLD_DISTANCE, TURN_TIME and BACK_TIME constants.
8. Test suite: 10 obstacle avoidance runs. Log success/fail. Target: 9/10 without getting stuck.
9. Battery test: run until battery low. Record runtime. Consider power optimisation.
10. Final demo: photograph/video the robot navigating an obstacle course. Celebrate!

---

## Extension Challenges

- Add an app control layer using Bluetooth (HC-05 module) to switch between modes.
- Program a return-to-home feature using compass and encoder modules.
- Design and 3D print a custom chassis or sensor mount for your robot.

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

← [Back to Course](../index.html) | 🎉 Course Complete — Build your robot!
