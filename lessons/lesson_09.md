---
layout: default
render_with_liquid: false
nav_order: 9
title: "Robotics Lesson 09 — Line Following Robot"
---

# Lesson 09: Line Following Robot

**Course:** Robotics & Arduino | **Lesson 09 of 12**

> Use IR sensors to read a line and build a proportional steering algorithm.

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

1. IR sensor module basics: emitter + detector. When IR reflects off white: HIGH. Black absorbs: LOW.
2. Wire two IR sensors: left sensor → A0, right sensor → A1.
3. Print both sensor readings to Serial Monitor. Place over white and black surfaces to observe.
4. Mount sensors on front of chassis, 1–2cm above the ground.
5. Logic: both white = straight; left on black = turn left; right on black = turn right; both black = stop or turn.
6. Implement basic line following: `if(left==LOW && right==HIGH) { turnLeft(); } else if(right==LOW && left==HIGH) { turnRight(); } else { forward(); }`
7. Tune motor speeds so turns are responsive but not too sharp.
8. Test on a black-tape track on white paper. Adjust sensor height and speed.
9. Add a third centre sensor for smoother tracking on complex curves.
10. Add a crossroads detection: all three sensors on black = stop for 1 second then continue.

---

## Extension Challenges

- Implement proportional steering: the farther off the line, the sharper the turn.
- Add a lap counter that increments each time the robot crosses the start line.
- Time each lap and display the fastest lap on Serial Monitor.

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

← [Back to Course](../index.html) | Next: [Lesson 10](lesson_10.html) →
