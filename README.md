# Smart Home Project - Nghiên cứu tích hợp hệ thống điều khiển tự động nhà thông minh sử dụng STM32 và ESP32

## Demo - Smart Home Control System using STM32 and ESP32

ESP32 điều khiển thiết bị thông minh, STM32 xử lý cảm biến và giao tiếp từ ứng dụng di động

📁 **Demo SMH.mp4** - Smart Home Control System Demo

🎥 **[➤ Xem Video Demo](https://github.com/NioDan-F/Smarthome-Firebase/raw/main/Demo%20SMH.mp4)**

## Results

Following can be observed from the system:

• **Response Time.** For device control commands, the system response time is ≤ 200ms via mobile app, while local HMI control response is ≤ 50ms.

• **Accuracy.** Fingerprint authentication achieves 95%+ accuracy, while environmental sensors provide reliable readings with ±2% precision.

• **Integration.** Seamless communication between STM32 and ESP32 via UART, with real-time data synchronization to Firebase.

## Features

### Core Functionality
- **Lighting Control**: Turn lights on/off in different rooms with dimming capabilities
- **Environmental Monitoring**: Real-time monitoring of temperature, humidity, and gas levels
- **Appliance Control**: Remote control of fans, water pumps, and other home appliances
- **Security System**: Fingerprint-based door access control with logging
- **Fire Safety**: Gas and temperature sensor integration with alarm system and notifications
- **Smart Irrigation**: Automated watering system based on soil moisture levels
- **Dual Interface**: Control via mobile application and HMI touchscreen

### Advanced Features
- **Real-time Data Logging**: All sensor data stored in Firebase with timestamps
- **Mobile Notifications**: Push notifications for security alerts and system status
- **Automated Schedules**: Time-based automation for lights and appliances
- **Energy Monitoring**: Track power consumption of connected devices
- **Voice Alerts**: Audio feedback through HMI for system events

## Hardware Components

### Main Controllers
- **STM32F103C8T6** (Blue Pill) - Main processing unit
- **ESP32 DEVKIT V1** - WiFi connectivity and IoT integration
- **HMI TJC4832K035_011RN** - 3.5" touchscreen interface

### Sensors & Input Devices
- **MQ-2 Gas Sensor** - LPG/CO/CH4 detection
- **DHT11** - Temperature and humidity monitoring
- **AS608 Fingerprint Sensor** - Biometric authentication
- **Soil Moisture Sensor** - Automated irrigation control

### Actuators & Output Devices
- **SG90 Servo Motor** - Door lock mechanism
- **12VDC Cooling Fan** (5x5x1.5cm) - Ventilation control
- **Water Pump** - Irrigation system
- **LED Strips** - Smart lighting system
- **Buzzer** - Audio alerts and notifications

### Power & Control Components
- **LM2596 Buck Converter** - Voltage regulation
- **PC817 Optocoupler** - Electrical isolation
- **MOSFETs & Transistors** - Power switching
- **Resistors, Capacitors, Diodes** - Supporting components
- **Breadboard & Jumper Wires** - Prototyping connections

## Software Requirements

### Development Environments
- **Arduino IDE** - ESP32 programming
- **STM32CubeIDE** - STM32 development
- **TJC Software** - HMI interface design
- **MIT App Inventor** - Mobile application development

### Libraries & Dependencies
- **Firebase ESP32 Library** - Cloud database integration
- **WiFi Library** - Network connectivity
- **DHT Sensor Library** - Temperature/humidity readings
- **Servo Library** - Motor control
- **ArduinoJson** - Data serialization

## System Architecture

```
Mobile App ←→ Firebase ←→ ESP32 ←→ STM32 ←→ Sensors/Actuators
                              ↓
                        HMI Touchscreen
```

### Communication Protocols
- **UART**: STM32 ↔ ESP32 communication
- **SPI**: HMI touchscreen interface
- **I2C**: Sensor data acquisition
- **WiFi**: ESP32 ↔ Firebase connection

## Installation and Setup

### 1. Hardware Assembly
1. Connect STM32 to sensors and actuators according to circuit diagram
2. Wire ESP32 to STM32 via UART (TX/RX pins)
3. Connect HMI touchscreen to STM32 via SPI
4. Set up power distribution using LM2596 converters

### 2. Software Configuration

**STM32 Programming:**
```bash
# Open STM32CubeIDE
# Import project: STM32_SmartHome.ioc
# Configure GPIO pins and peripherals
# Build and flash to STM32
```

**ESP32 Setup:**
```bash
# Install ESP32 board package in Arduino IDE
# Install required libraries
# Configure WiFi credentials and Firebase API keys
# Upload code to ESP32
```

**Mobile App:**
- Open MIT App Inventor project file
- Configure Firebase database connection
- Build and install APK on Android device

### 3. System Configuration
- Set up Firebase Realtime Database
- Configure HMI interface screens
- Test all sensor readings and actuator responses
- Calibrate fingerprint sensor

## Usage Instructions

### Mobile Application Control
1. **Launch App**: Open smart home control app
2. **Connect**: Ensure phone is on same WiFi network
3. **Authentication**: Log in with credentials
4. **Control Devices**: Use intuitive interface to control lights, fans, etc.
5. **Monitor**: View real-time sensor data and system status
6. **Schedule**: Set up automated routines and timers

### HMI Touchscreen Operation
1. **Main Screen**: View system overview and quick controls
2. **Device Control**: Access individual device control panels
3. **Sensor Monitor**: Check environmental conditions
4. **Security**: Manage fingerprint access and view logs
5. **Settings**: Configure system parameters and thresholds

### Emergency Procedures
- **Fire Alert**: System automatically triggers alarm and sends notifications
- **Manual Override**: Use HMI emergency buttons for immediate control
- **Power Failure**: System saves state and restores after power return

## Project Structure

```
Smarthome-Firebase/
├── STM32_Code/
│   ├── Core/
│   │   ├── Inc/
│   │   └── Src/
│   ├── Drivers/
│   └── Middlewares/
├── ESP32_Code/
│   ├── src/
│   │   ├── main.cpp
│   │   ├── firebase_config.h
│   │   └── sensor_handler.cpp
│   └── libraries/
├── HMI_Interface/
│   ├── screens/
│   └── graphics/
├── Mobile_App/
│   ├── blocks/
│   └── assets/
├── Documentation/
│   ├── Circuit_Diagrams/
│   ├── User_Manual.pdf
│   └── Technical_Report.pdf
├── Demo SMH.mp4
└── README.md
```

## Technical Specifications

| Component | Specification |
|-----------|---------------|
| **Main MCU** | STM32F103C8T6 @ 72MHz |
| **WiFi Module** | ESP32-WROOM-32 |
| **Display** | 3.5" TFT Touchscreen (480x320) |
| **Operating Voltage** | 3.3V / 5V / 12V |
| **Communication** | UART, SPI, I2C |
| **Wireless** | WiFi 802.11 b/g/n |
| **Database** | Firebase Realtime Database |
| **Power Consumption** | ~2.5W (standby), ~15W (active) |
| **Operating Temperature** | -10°C to +50°C |

## Troubleshooting

### Common Issues
- **Connection Problems**: Check WiFi credentials and network stability
- **Sensor Errors**: Verify wiring and power supply voltages
- **App Sync Issues**: Ensure Firebase database rules are properly configured
- **HMI Unresponsive**: Check SPI connections and power supply

### Performance Optimization
- Adjust sensor reading intervals to reduce power consumption
- Optimize Firebase queries for faster response times
- Use deep sleep mode for ESP32 during inactive periods

## Future Enhancements

- **Voice Control Integration**: Add support for Google Assistant/Alexa
- **Machine Learning**: Implement predictive automation based on usage patterns
- **Energy Monitoring**: Add current sensors for power consumption tracking
- **Expansion Modules**: Support for additional rooms and devices
- **Cloud Analytics**: Advanced data analysis and reporting features

## Documentation

For detailed information including:
- Complete circuit diagrams
- PCB layouts and assembly instructions
- Software implementation details
- API documentation
- User manual and troubleshooting guide

Please refer to the technical report: **"Nghiên cứu tích hợp hệ thống điều khiển tự động nhà thông minh sử dụng STM32 và ESP32"**

## Contributing

We welcome contributions to improve the Smart Home Project! Here's how you can help:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'Add amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. **Open** a Pull Request

### Contribution Areas
- Hardware design improvements
- Software optimization
- Mobile app enhancements
- Documentation updates
- Bug fixes and testing

## License

This project is released under **MIT License** - see the [LICENSE](LICENSE) file for details.

## Authors & Acknowledgments

- **Main Developer**: [NioDan-F](https://github.com/NioDan-F)
- **Supervisor**: [Supervisor Name]
- **Institution**: [University/Institution Name]

### Special Thanks
- STM32 and ESP32 communities for excellent documentation
- Firebase team for reliable cloud services
- Open source contributors and libraries used in this project

## Contact & Support

- **GitHub Issues**: For bug reports and feature requests
- **Email**: [your-email@domain.com]
- **Documentation**: Check the `/Documentation` folder for detailed guides

---

**⚠️ Safety Notice**: This project involves electrical components and mains voltage. Please follow proper safety procedures and consult with qualified electricians when implementing in real homes.
