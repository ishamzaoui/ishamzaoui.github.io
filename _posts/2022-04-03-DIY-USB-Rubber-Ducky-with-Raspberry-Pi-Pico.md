---
layout: post
title: "DIY USB Rubber Ducky with Raspberry Pi Pico"
date: 2022-04-03 12:00:00 +0000
categories: projects hardware-hacking-tools
tags: [Raspberry Pi Pico, USB Rubber Ducky, HID, cybersecurity, Python]
---



## Overview
This project demonstrates how to create a **USB Rubber Ducky** using a **Raspberry Pi Pico** as a keyboard HID (Human Interface Device). The device can execute custom scripts for penetration testing, automating tasks, and ethical hacking. It supports **French (FR) and US keyboard layouts**, along with a custom scripting syntax.

### Features:
- **Raspberry Pi Pico as a USB HID Keyboard**
- **Custom scripting engine** for executing payloads
- **Support for multiple keyboard layouts (FR, US)**
- **Python-based execution engine**
- **Adafruit HID library support**

## Hardware Requirements
- **Raspberry Pi Pico**
- **USB cable**
- **Computer for writing and running scripts**

### Device Image
![Raspberry Pi Pico USB Rubber Ducky](https://ishamzaoui.github.io/images/projects/usb-rubber-ducky/device.jpg)

## Software Implementation
### 1. Setting Up the Raspberry Pi Pico
1. Download and install **MicroPython** firmware on your Raspberry Pi Pico.
2. Use **Thonny IDE** or another Python editor to upload scripts.
3. Install **Adafruit HID library** to handle keyboard emulation.

### 2. Writing Payloads
The scripting syntax allows you to define keystrokes, delays, and commands, similar to traditional USB Rubber Ducky payloads. Example syntax:

```text
WAIT 1000
WRITE Hello, World!
ENTER
```

### 3. Executing the Script
1. Write the payload script.
2. Upload it to the Raspberry Pi Pico.
3. Plug the device into a target machine, and it will execute the keystrokes automatically.

## Demonstration Video
📹 Watch the project in action: [YouTube Short](https://www.youtube.com/shorts/PNtKHNWO9b4)

## Conclusion
This project showcases how the **Raspberry Pi Pico** can be repurposed as a USB Rubber Ducky, enabling penetration testers and cybersecurity enthusiasts to create and test payloads. Future enhancements could include **GUI-based script generators**, **payload encryption**, and **multi-platform support**.

## Author
**HAMZAOUI**
