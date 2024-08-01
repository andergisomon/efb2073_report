+++
title = 'Introduction'
summary = "Project background, problem statement, and objectives"
draft = false
weight = 2
+++

## Project Background
Our project makes use of ESP-NOW, a wireless communication protocol developed by Espressif for short packet transmission. This versatile protocol enables multiple devices to talk to each other via Wi-Fi with ESP-NOW protocol.

In many industrial, commercial, and residential applications, traditional wired communications are still widely used for controlling various systems and devices, mostly to turn ON/OFF certain devices. Our system replaces clunky wires in exchange for modular wireless switches.

## Problem Statement
Wired systems quickly become inconvenient when many devices need to be controlled. This scalability issue can be solved using a wireless control system, which we implemented using ESP NOW.


## Objectives
> - To update currently wired switches by wireless switches
> - To enable users to control their devices from multiple location through wireless transmission
> - To use local transmission for private IoT applications/environment

## Tech stack
### NO PART of the Arduino framework was used.
{style="color: red"}

### Hardware
> - Seeed XIAO ESP32C3 boards (x2)
> - LEDs
> - Buzzer
> - Switches
> - 12V LED strip (x2)
> - DC submersible water pump

**Auxiliary hardware**
> - Portable power bank


### Software frameworks
**For embedded programming**
> - ESP IoT Development Framework (ESP IDF)
> - Powershell (for data logging)
> - Visual Studio Code + ESP IDF extension
> - IDF Frontend

**For web report**
> - Hugo (website building)
> - Git (version control)
> - GitHub Pages (static site hosting)

**Programming/markup languages**
> - C (everything else)
> - JavaScript, CSS, HTML (website report)
