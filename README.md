# Haptic Feedback Shoes  
### Intelligent Directional Vibration Guidance System

---

## ߚ Overview

Haptic Feedback Shoes enable navigation awareness using **vibrational cues** instead of sight.  
Sensors detect obstacles around the wearer, and lightweight motors provide immediate feedback based on direction.

This improves:
- Spatial awareness  
- Reaction time  
- Mobility confidence  

No audio. No screens. Only instinctive **tactile feedback**.

---

## ߧ How It Works

Each shoe embeds an ESP32-C3 with distance sensors:

| Shoe | Sensors | Action | Wireless Role |
|------|---------|--------|---------------|
| **Right Shoe** | 2 × VL53L0X | Front + Right obstacle detection | ESP-NOW Sender |
| **Left Shoe** | 1 × VL53L0X | Left obstacle detection | ESP-NOW Receiver |

Trigger logic:
- **< 90 cm (900 mm)** = vibration event  
- If **front sensor** triggered → both shoes vibrate  
- If **right sensor** triggered → right shoe vibrates  
- If **left sensor** triggered → left shoe vibrates  
- Right shoe transmits `"YES"` wirelessly when front triggers  

---

## ߛ️ Hardware Summary

- **ESP32-C3 Super Mini**  
- **VL53L0X Time-of-Flight sensors**  
- **ERM coin vibration motor modules**  
- **Transistor-based motor drivers**  
- **Custom PCB integration**  
- **Li-ion powered**

Charging:
- **TP4056 charger**  
- **Status LEDs** for charging/full indicators  

---

## ߓ Wireless Communication — ESP-NOW

- Ultra-low latency  
- No router required  
- Direct device-to-device link  
- Reliable direction mapping feedback  

Master → Slave messaging keeps motion synchronized during travel.

---

## ߔ Firmware Capabilities

- Continuous sensor monitoring  
- Vibration PWM control (future-ready)  
- Debounced ESP-NOW transmission  
- Direction classification  
- Debug feedback over serial  
- Low-power + wearable design  

---

## ߧ‍♂️ Target Use-Case

Assistive wearable for:
- Low-vision mobility support  
- Training for obstacle awareness  
- Indoor safety in unfamiliar areas  

Designed for practical navigation — not gimmicks.

---

## ✨ Credits — Project Roles

| Role | Contribution | Responsible |
|------|--------------|------------|
| Project Owner | Full project concept, system architecture | **Ruturaj** |
| Electronics Design | PCB layout, component integration | **Ruturaj** |
| Firmware Engineer | ESP-NOW communication, sensor processing | **Ruturaj** |
| Embedded Development | Motor control logic, calibration | **Ruturaj** |
| Hardware Assembly | Soldering, wiring, enclosure | **Ruturaj** |
| Field Testing | Real-world evaluation, iteration | **Ruturaj** |

> **This is an independent engineering project.**  
> Designed, built, programmed, and tested by a single creator.

---

## ߓ Firmware Code

⚠️ Firmware will be added later.  

This section will include:
- Right Shoe ESP32-C3 firmware
- Left Shoe ESP32-C3 firmware

---

## ߎ Vision

> _Make technology an extension of instinct._  
>  
> **Every step counts. Make every step smarter.**
