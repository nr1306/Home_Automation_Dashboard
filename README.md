# Homemade Automation Dashboard

## OVERVIEW

This project delivers a **production-ready IoT-based home automation system** integrating **ESP32 microcontrollers** and **DS18B20 sensors** into a responsive **Qt Quick dashboard**. It is designed for real-time monitoring and control of multiple home devices via **AWS IoT Core** and the **MQTT protocol**.

It features two key components:

- **IoT Device Layer**: ESP32 boards equipped with DS18B20 temperature sensors, configured to communicate securely via MQTT.
- **Qt Quick Dashboard**: A responsive, cross-platform UI built with **QML** (frontend) and **C++** (backend) that manages device states, visualizes data, and enables remote control.

This architecture ensures **secure cloud communication**, **fast device status updates**, and **scalable design** for adding more devices in the future.

### Technologies Used

- Qt Quick (QML)
- C++
- AWS IoT Core
- MQTT Protocol
- ESP32 Microcontrollers
- DS18B20 Sensors
- Qt Creator (Development Environment)

---

## PROJECT STRUCTURE

```plaintext
.
├── src/                       # Core source code
│   ├── backend/               # C++ backend logic
│   ├── frontend/               # QML components for UI
│   └── mqtt/                   # MQTT communication handlers
├── resources/                  # Images, icons, and other assets
├── tests/                      # Unit, system, and regression tests
├── docs/                       # Documentation and diagrams
├── CMakeLists.txt              # Build configuration
└── README.md                   # Project documentation

```
---

## WORKFLOW DIAGRAM

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/5e147e1c-7067-4d59-8563-0ca6320ca7df" />


---

## HOW TO RUN

Follow these steps to set up and run the project locally:

### 1. Prerequisites
Ensure the following are installed:
- Qt 5/6 with Qt Quick and CMake support
- AWS IoT Core account with configured Thing, certificate, and policy
- MQTT broker details (AWS IoT Core or external)
- ESP32 development environment (Arduino IDE or PlatformIO)

### 2. Configure IoT Devices
1. Flash ESP32 boards with firmware to read DS18B20 data and publish via MQTT.
2. Configure AWS IoT certificates and attach them to each device.

### 3. Build and Run the Qt Quick Dashboard
```bash
git clone https://github.com/20IT121/Homemade_Automation-Dashboard.git
cd Homemade_Automation-Dashboard
mkdir build && cd build
cmake ..
make
./HomemadeAutomationDashboard

```
### 4. Interact with the Dashboard

- View real-time temperature readings from DS18B20 sensors.
- Control connected devices remotely.
- Monitor device states securely through AWS IoT Core.

---

## CONTRIBUTING

Contributions are welcome!
- Fork the repository
- Create a new branch: git checkout -b feature-name
- Commit your changes: git commit -m "Add feature"
- Push to the branch: git push origin feature-name
- Open a Pull Request

We appreciate feature suggestions, bug reports, and performance improvements.

