# 🏠 Smart Home Project with STM32 & ESP32

A complete demo of a smart home system using **STM32 (Blue Pill)** and **ESP32**, enabling full control and monitoring via:

- 📱 Android mobile app  
- 🖥️ Touchscreen HMI interface  
- ☁️ Firebase Realtime Database with push notifications  

---

## 🚀 Core Features

- **Lighting Control** – Toggle lights in different rooms/zones  
- **Environmental Monitoring** – Live temperature, humidity, and gas data  
- **Appliance Control** – Remotely operate fans, water pumps, and more  
- **Security System** – Fingerprint-based door unlocking  
- **Fire & Gas Alerts** – Real-time gas leaks and high-temp detection with notifications  
- **Smart Irrigation** – Auto water pump triggered by soil moisture sensor  
- **Dual UI** – Control system from both mobile app and HMI touchscreen  

---

## 🧰 Hardware Used

- STM32F103C8T6 (Blue Pill)  
- ESP32 DevKit V1  
- TJC4832K035_011RN – 3.5″ HMI touchscreen  
- MQ‑2 gas sensor, DHT11 (temp/humidity sensor), soil moisture sensor  
- SG90 servo, 12 V DC fan  
- AS608 fingerprint sensor  
- LM2596 buck converter, PC817 optocoupler  
- MOSFETs, transistors, diodes, resistors, capacitors  
- Breadboard, jumper wires  

---

## 💻 Software Stack

- IDEs: STM32CubeIDE, Arduino IDE  
- Realtime database: Firebase  
- Frontend:
  - HMI UI created using TJC (Nextion-compatible) software  
  - Mobile app built with MIT App Inventor  

---

## ⚙️ Setup & Deployment

1. Clone the repository:
   ```bash
   git clone https://github.com/NioDan-F/Smarthome-Firebase.git
   ```

2. Refer to the provided schematics and wiring in the project report.

3. Flash firmware:
   - Use **STM32CubeIDE** for STM32  
   - Use **Arduino IDE** for ESP32  

4. Upload HMI screen layout using TJC software.

5. Set up Firebase:
   - Configure your DB URL, API key, etc.  
   - Connect the Android app for live control and monitoring  

📘 For full schematics, wiring, deployment steps, and usage guide, refer to the project report:  
**_“Research on Integrating an Automated Smart Home System Using STM32 and ESP32”_**

---

## 📹 Demo Video
https://user-images.githubusercontent.com/218482220/461159236-d7dc2ed1-0180-4162-8051-8e70659ab832.mp4
[![Watch the demo](https://img.youtube.com/vi/G2j17-QzUfQ/hqdefault.jpg)](https://youtu.be/G2j17-QzUfQ)
---

## 📁 Project Structure

- `code_esp32_SmartHome_Firebase.ino` – ESP32 code for Firebase integration  
- `stm32_main.c` – Main STM32 firmware handling sensors and devices  
- `*.HMI` – HMI configuration files  
- PCB design (`.PrjPcb`), report, and demo files included  

---

## 👤 Author

**Quyet Ba (aka NioDan-F)**  
📧 [quyet1hai@gmail.com](mailto:quyet1hai@gmail.com)

---

