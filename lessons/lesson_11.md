---
layout: default
render_with_liquid: false
nav_order: 11
title: "Robotics Lesson 11 — Building Your First Autonomous Robot"
---

# Lesson 11: Building Your First Autonomous Robot

**Course:** Robotics & Arduino | **Lesson 11 of 12**

> Combine motors, ultrasonic sensor and decision logic for autonomous obstacle avoidance.

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

1. Review the complete chassis wiring: motors, L298N, HC-SR04, Arduino and battery.
2. Write the `getDistance()` helper function that returns distance in cm.
3. Write `forward()`, `backward()`, `turnLeft()`, `turnRight()`, `stopAll()` motor functions.
4. Main loop: `int d = getDistance(); if(d > 20) { forward(); } else { avoidObstacle(); }`
5. Write `avoidObstacle()`: stop → back up 300ms → stop → turn right 500ms → check distance → repeat if needed.
6. Upload and test in an open area. Does the robot navigate without hitting walls?
7. Tune the distance threshold (20cm) and turn duration (500ms) for your environment.
8. Add a mount for the ultrasonic sensor — tilt it slightly downward to detect low obstacles.
9. Test on a maze: create a simple cardboard maze and time how long to escape.
10. Add an LED status indicator: green = clear, red = obstacle detected.

---

## Extension Challenges

- Add a servo that pans the sensor left/right to choose the better direction.
- Add line sensors to keep the robot on a track while avoiding obstacles.
- Add a companion mode: robot follows a person by maintaining 30cm distance.

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

← [Back to Course](../index.html) | Next: [Lesson 12](lesson_12.html) →
