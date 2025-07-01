# Smart Home Project with STM32 & ESP32

## Overview

A complete smart home demonstrator built using **STM32** and **ESP32**, featuring control and monitoring via:

- 📱 Mobile app (Android)
- 🖥️ HMI touchscreen interface
- ☁️ Firebase backend for real-time data synchronization and notifications

---

## 🚀 Core Features

- **Lighting Control**: Toggle lights across different rooms
- **Environmental Monitoring**: Real-time tracking of temperature, humidity, and gas levels
- **Appliance Management**: Remote operation of fans, water pumps, etc.
- **Security**: Fingerprint-enabled door access
- **Fire Detection & Alarm**: Gas/leak detection, high-temp alarms, and push notifications
- **Automatic Irrigation**: Soil moisture-based pump activation
- **Dual UI**: Control from both a mobile application and the HMI touchscreen

---

## 🧰 Hardware Components

- STM32F103C8T6 (Blue Pill)
- ESP32 DEVKIT V1
- TJC4832K035_011RN 3.5″ HMI touchscreen
- MQ‑2 gas sensor, DHT11 sensor
- SG90 servo, 12 V DC cooling fan
- AS608 fingerprint sensor
- LM2596 buck converter, PC817 optocoupler
- Assorted diodes, resistors, capacitors, MOSFETs, transistors
- Breadboard + jumper wires

---

## 💾 Software Stack

- IDEs: Arduino IDE, STM32CubeIDE
- Backend: Firebase Realtime Database (ESP32 integration)
- Frontend:
  - HMI config via TJC software
  - Mobile app developed in MIT App Inventor

---

## ⚙️ Setup & Usage

1. Clone the repo:
   ```bash
   git clone https://github.com/NioDan-F/Smarthome-Firebase.git
   ```
2. Follow hardware schematics and wiring in the project report.
3. Load firmware into STM32 and ESP32 using STM32CubeIDE and Arduino IDE.
4. Upload HMI layout via TJC software.
5. Configure Firebase and integrate mobile app for real-time control.

➡️ **For schematics, wiring guide, deployment steps, and usage instructions, see the project report**: *Research on Integrating an Automated Smart Home System Using STM32 and ESP32*.

---

## 📹 Demo

```markdown
### 🎥 Demo Video  
[![Watch the demo](https://img.youtube.com/vi/HB_Bb6ohP3s/hqdefault.jpg)](https://www.youtube.com/watch?v=HB_Bb6ohP3s)

```

---

## 👤 Author

**Quyet Ba (aka NioDan-F)**  
📧 [quyet1hai@gmail.com](mailto:quyet1hai@gmail.com)

---
