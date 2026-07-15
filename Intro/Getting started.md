# Getting Started with the Arduino Nano-Compatible Microcontroller

## 1. Introduction

An Arduino Nano-compatible board is a small programmable device that can control lights, sensors, motors, and many other electronic parts. It is great for beginners because it is small, affordable, and easy to connect.

---

## 2. Objectives

By the end of this guide, you will be able to:

- To understand what an Arduino Nano-compatible board is
- To identify the main parts of the board
- To connect the board safely to a computer and components
- To upload a simple program
- To run a basic project using software such as PictoBlox

---

## 3. Platform Choices

There are several ways to program an Arduino Nano-compatible board.

### Option 2: PictoBlox
- Best for children and visual learners
- Uses blocks instead of text
- Makes coding easier by showing actions visually

## 4. Setup - Wiring Diagram and Step by Step

### What you need

- Arduino Nano-compatible board
- USB cable
- Computer
- Breadboard (optional)
- LED
- Resistor (220Ω)
- Jumper wires

### Important safety note
- Always unplug the board before changing wires
- Do not connect components incorrectly
- Make sure the board is powered only through the USB cable

### Basic wiring diagram

```

### Step-by-step setup

1. Connect the Arduino Nano-compatible board to your computer using the USB cable.
2. Wait for the computer to recognize the board.
3. Place the LED on the breadboard.
4. Connect one leg of the LED to the resistor.
5. Connect the other side of the resistor to pin D13 on the board.
6. Connect the LED’s other leg to GND.
7. Open PictoBlox or Arduino IDE.
8. Select the correct board type and port.
9. Upload your first program.

### Simple wiring explanation
Think of the board as the brain. The wires are the nerves. The LED is the body part that reacts.

---

## 5. Coding - PictoBlox

PictoBlox is a block-based coding platform that is easy for beginners to understand.

### How to start with PictoBlox

1. Open PictoBlox on your computer.
2. Create a new project.
3. Choose the board type as Arduino Nano-compatible.
4. Add a block for the LED.
5. Turn the LED on and off with delays.

### Example simple program

```text
When Green Flag clicked
Set LED on pin D13 to ON
Wait 1 second
Set LED on pin D13 to OFF
Wait 1 second
Repeat forever
```

### What this program does
- The LED turns on
- It waits for one second
- It turns off
- It repeats again and again

This is a great first project because it teaches the basic idea of input, output, and timing.

---

## 6. Simulation

Simulation means testing your project on the screen before using real hardware.

### Why simulation is helpful
- It helps beginners learn without making mistakes
- It lets you see what the code will do
- It is safer and faster for practice

### In PictoBlox
- You can run the program in simulation mode
- You can check whether the LED turns on and off as expected
- If something does not work, you can fix the code before connecting real wires

### Example simulation idea
Imagine the LED is a tiny lamp. When the code says “turn on,” the lamp lights up. When the code says “turn off,” the lamp goes dark.

---

## 7. Conclusion

You have now learned the basics of using an Arduino Nano-compatible microcontroller. You know what it is, how it can be connected, and how simple programs can make it do useful things.

The most important lessons are:
- start small
- connect wires carefully
- test your code step by step
- have fun while learning

With practice, you can build lights, sensors, robots, and many more exciting projects.

---

## Quick Summary

- Arduino Nano-compatible boards are small programmable devices
- They can control electronic parts like LEDs and motors
- PictoBlox is a beginner-friendly platform for learning coding
- Simulation helps you test ideas safely before using real hardware

---

## See Also

- Arduino IDE Guide
- PictoBlox Basics
- Beginner Electronics Basics
