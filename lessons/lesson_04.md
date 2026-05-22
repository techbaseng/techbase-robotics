---
layout: default
render_with_liquid: false
nav_order: 4
title: "Robotics Lesson 04 — Digital Inputs — Push Buttons"
---

# Lesson 04: Digital Inputs — Push Buttons

**Course:** Robotics & Arduino | **Lesson 04 of 12**

> Read button presses with digitalRead, understand pull-up resistors and debouncing.

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

1. Wire a push button: one pin to Arduino pin 2, other pin to GND.
2. Enable the internal pull-up resistor: `pinMode(2, INPUT_PULLUP)`.
3. With INPUT_PULLUP: button reads HIGH when not pressed, LOW when pressed.
4. Read the button: `int state = digitalRead(2);`
5. Toggle an LED when the button is pressed: `if (state == LOW) { digitalWrite(13, !digitalRead(13)); }`
6. Problem: bouncing — mechanical buttons can register multiple presses in one physical press.
7. Software debounce: record `lastDebounceTime` and only register a state change if it persists for 50ms.
8. Wire a second button on pin 3. Button 1 turns LED on, Button 2 turns it off.
9. Use an external pull-down resistor (10kΩ to GND) instead of INPUT_PULLUP and compare behaviour.
10. Print button state to Serial Monitor and observe the bounce effect before and after debouncing.

---

## Extension Challenges

- Build a two-button counter: one button increments, one decrements. Display on Serial Monitor.
- Add a long-press detection (held >1 second) that triggers a different action.
- Wire 4 buttons as a simple lock combination — correct sequence unlocks (LED turns green).

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

← [Back to Course](../index.html) | Next: [Lesson 05](lesson_05.html) →
