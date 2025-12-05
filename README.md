# Haptic Feedback Shoes
## Intelligent Directional Vibration Guidance System

![Platform: ESP32-C3](https://img.shields.io/badge/Platform-ESP32--C3-green)
![Sensors: VL53L0X](https://img.shields.io/badge/Sensors-VL53L0X-blue)
![Wireless: ESP--NOW](https://img.shields.io/badge/Wireless-ESP--NOW-orange)
![Category: Assistive Technology](https://img.shields.io/badge/Category-Assistive%20Technology-purple)

---

## ߚ Overview

Haptic Feedback Shoes enable navigation awareness using vibrational cues instead of sight. Sensors detect obstacles around the wearer, and lightweight motors provide immediate feedback based on direction.

This improves:
- Spatial awareness
- Reaction time
- Mobility confidence

No audio. No screens. Only instinctive tactile feedback.

---

## ߧ How It Works

Each shoe embeds an ESP32-C3 with distance sensors:

| Shoe | Sensors | Action | Wireless Role |
|------|---------|--------|---------------|
| Right Shoe | 2 × VL53L0X | Front + Right obstacle detection | ESP-NOW Sender |
| Left Shoe | 1 × VL53L0X | Left obstacle detection | ESP-NOW Receiver |

Trigger logic:
- < 90 cm (900 mm) = vibration event
- If front sensor triggered → both shoes vibrate
- If right sensor triggered → right shoe vibrates
- If left sensor triggered → left shoe vibrates
- Right shoe transmits "YES" wirelessly when front triggers

---

## ߛ️ Hardware Summary

- ESP32-C3 Super Mini
- VL53L0X Time-of-Flight sensors
- ERM coin vibration motors
- Transistor-based motor drivers
- Custom PCB
- Li-ion powered

Charging:
- TP4056 charger
- Status LEDs for charging/full indicators

### Additional Badges
![Power: Li-ion Battery](https://img.shields.io/badge/Power-Li--ion%20Battery-red)
![Driver: Transistor](https://img.shields.io/badge/Driver-Transistor-lightgrey)
![Motors: ERM](https://img.shields.io/badge/Motors-ERM-yellow)
![Custom PCB](https://img.shields.io/badge/PCB-Custom%20Design-blueviolet)

---

## ߓ Wireless Communication — ESP-NOW

- Ultra-low latency
- No router required
- Direct peer-to-peer communication
- Reliable directional feedback

Master → Slave messaging keeps the system synchronized.

---

## ߔ Firmware Capabilities

- Continuous sensor monitoring
- Vibration PWM control (future-ready)
- Debounced ESP-NOW transmissions
- Direction classification
- Debug logs for testing
- Low-power wearable operation

---

## ߧ‍♂️ Target Use-Case

Assistive wearable for:
- Low-vision mobility support
- Training obstacle awareness
- Indoor safety in unfamiliar environments

Designed for practical navigation assistance.

---

## ✨ Credits — Project Roles

| Role | Contribution | Responsible |
|------|--------------|------------|
| Project Owner | Full project concept, system architecture | Ruturaj |
| Electronics Design | PCB layout and component integration | Ruturaj |
| Firmware Engineer | ESP-NOW communication, sensor logic | Ruturaj |
| Embedded Development | Motor control and calibration | Ruturaj |
| Hardware Assembly | Soldering, wiring, and build | Ruturaj |
| Field Testing | Real-world evaluation | Ruturaj |

This is an independent engineering project.
Designed, built, programmed, and tested by a single creator.

---

## ߓ Firmware Code

Firmware will be added later:

- Right Shoe ESP32-C3 firmware
- Left Shoe ESP32-C3 firmware

---

## ߎ Vision

Make technology an extension of instinct.

Every step counts. Make every step smarter.
