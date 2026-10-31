# Echo: Zero

> *"When the world goes silent, we still transmit."*

## Overview
**Echo: Zero** is a handheld, off-grid emergency communication device built to maintain vital links when cellular networks, internet infrastructure, and power grids fail during natural disasters or remote expeditions. The project bridges traditional manual telegraphy (Morse code) with modern packet-based radio frequencies for reliable, low-power communication.

---

## Current Features & Codebase
* **Morse Code Decoder:** Translates real-time input signals into readable text.
* **I2C LCD Integration:** Displays status outputs and decoded messages via a 16x2 I2C Liquid Crystal display.
* **Modular C++ Architecture:** Clean, structured firmware built for microcontrollers.

---

## Target Hardware Architecture & Roadmap
The system design incorporates the following specifications and planned expansions:
* **Processing:** Dual ESP32 microcontrollers (utilizing standard D-pin configurations).
* **Long-Range Communication:** SX1278 Ra-02 LoRa modules (433 MHz) paired with IPEX snap-on antennas for peer-to-peer off-grid links.
* **Location Tracking:** NEO-6M GPS modules for automated distress coordinate broadcasting.
* **Audio Layer:** Microphone amplifiers, MAX98357A audio amplifiers, and mini speakers for acoustic signaling and voice transmission.
* **Power Management:** 3.7V LiPo pouch cells configured for portable operation.
* **Communication Protocols:** Operating across ESP-NOW and custom LoRa mesh networks.

---

## Applications & Future Development
* **Field Deployment:** Designed as an adaptable, low-cost emergency node for disaster management and tactical off-grid communication challenges.
* **Product Scaling:** Engineered with modular protocols and custom routing to evolve into a certified standalone safety device.

---

## Repository Structure
```text
├── MorseDihcoder.ino         # Main firmware sketch for signal processing
├── LiquidCrystal_I2C.cpp     # C++ source file for I2C LCD control
└── LiquidCrystal_I2C.h       # C header file for display communication
