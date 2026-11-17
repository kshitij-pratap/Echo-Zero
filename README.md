# Echo: Zero

> *"When the world goes silent, we still transmit."*

## Overview
**Echo: Zero** is a handheld, off-grid emergency communication device built to maintain vital links when cellular networks, internet infrastructure, and power grids fail during natural disasters or remote expeditions. The system combines manual telegraphy (Morse code), packet-based LoRa radio, live GPS telemetry, and audio signaling in a standalone portable unit.

---

## Implemented Features
* **Long-Range Off-Grid Messaging:** Peer-to-peer text and telemetry transmission over 433 MHz LoRa (SX1278), paired with low-latency local links via ESP-NOW.
* **Hardware Morse Code Transceiver:** Physical button input with real-time Morse-to-text decoding, calibrated input timing windows, and wireless packet transmission.
* **Live GPS Telemetry:** Integrated NEO-6M GPS module for acquiring and broadcasting real-time distress coordinates, including fallback handling when a satellite lock is unavailable.
* **OLED Graphical Interface:** 1.3-inch SH1106 OLED display rendering live system status, incoming and outgoing messages, GPS coordinates, and custom UI animations.
* **Audio & Acoustic Stage:** Integrated microphone input and amplified speaker output (MAX98357A) for audio transmission and acoustic alerts.

---

## Hardware Architecture
* **Microcontroller:** ESP32
* **Radio Transceiver:** SX1278 Ra-02 LoRa module (433 MHz) with external antenna
* **GPS Receiver:** NEO-6M GPS module
* **Display:** 1.3-inch I2C SH1106 OLED display
* **Audio Stage:** Microphone module, MAX98357A amplifier, and mini speaker
* **Power Supply:** 5V USB power via portable power bank / host USB (standalone LiPo battery integration in progress)

---

## Applications & Scaling
* **Field Deployment:** Self-contained, low-cost emergency communication node for disaster response, search-and-rescue coordination, and off-grid expeditions.
* **Product Development:** Engineered with modular firmware and custom packet routing to evolve into a certified standalone safety device.

---

## Repository Structure
```text
├── EchoZero/
│   ├── EchoZero.ino              # Master firmware (OLED, LoRa, GPS, Morse, Audio)
│   ├── Adafruit_SH110X/          # SH1106 OLED display driver library
│   ├── Adafruit_GFX_Library/     # Core graphics library for OLED UI
│   ├── LoRa/                     # SX1278 LoRa radio communication library
│   └── TinyGPSPlus/              # NMEA GPS parsing library
├── MorseDihcoder.ino             # Initial Morse decoder prototype sketch
├── LiquidCrystal_I2C.cpp         # I2C LCD source file (reserved for upcoming LCD build)
├── LiquidCrystal_I2C.h           # I2C LCD header file (reserved for upcoming LCD build)
└── README.md
