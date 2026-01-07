# Real-Time-Crop-Monitoring-and-Alert-System-Using-CropBot
## 📌Project Overview

The Real-Time Crop Monitoring and Alert System using CropBot is an IoT-based solution designed to help farmers monitor field conditions in real time. It continuously tracks environmental parameters such as soil moisture, temperature, humidity, and rainfall, and sends instant alerts when abnormal conditions are detected, enabling timely action and improved crop yield.

## 🎯Objectives

 1. Monitor crop field conditions in real time

2. reduce manual field inspection

3. Provide instant alerts to farmers

4. Improve crop productivity and resource management

## 🛠️Technologies & Tools Used

**Microcontroller:** ESP32

**Sensors:**

Soil Moisture Sensor

Temperature & Humidity Sensor (DHT11/DHT22)

Rain Sensor

**Cloud Platforms:** ThingSpeak,Blynk IoT

**Mobile Dashboard:** ThingSpeak,Blynk IoT

**Alert System:** Telegram Bot

**Programming Language:** Arduino C/C++

## ⚙️System Architecture

- Sensors collect real-time field data

- ESP32 processes the sensor readings

- Data is uploaded to ThingSpeak Cloud

- Live monitoring via Blynk mobile app

- Alerts are sent to farmers through Telegram

## 🔄Working Principle

1. The CropBot continuously reads sensor values

2. If parameters cross predefined thresholds, alerts are triggered

3. Farmers receive instant notifications on Telegram

4. Historical data is stored in the cloud for analysis

## 📥Inputs

`Soil moisture level`

`Temperature`

`Humidity`

`Rain detection`

## Connections

### 1. DHT11 Sensor (Temp & Humidity)
   
`VCC` → 3.3V (or 5V)

`GND` → GND

`DATA` → GPIO 4 (DHTPIN)

### 2. Soil Moisture Sensor (Analog type)

`VCC` → 3.3V

`GND` → GND

`Analog OUT` → GPIO 34 (SOIL_MOISTURE_PIN)

### 3. LDR (Light Sensor with voltage divider)

`One end of LDR` → 3.3V

`Other end of LDR` → 10kΩ resistor to GND, and connect that middle node (junction) to:

`GPIO 35` → (LIGHT_SENSOR_PIN)

### 4. Relay Module (To Control DC Motor)

`VCC` → 5V (from ESP32 or external)

`GND` → GND

`IN` → GPIO 14 (RELAY_PIN)

`COM` → One wire from DC motor power (e.g., + of external 12V)

`NO (Normally Open)` → DC motor + input

`GND of DC motor power `→ Motor GND

**⚠️Important:** If your DC motor requires higher voltage or current, use an external power supply for the motor and do not power it from the ESP32.

### 5. ESP32 Board

Powered via USB or 5V source.

Connect all GNDs together (ESP32, sensors, relay, motor power supply if shared).

## 📤Outputs

- Live sensor data on Blynk dashboard

- Graphical data visualization on ThingSpeak

- Alert messages via Telegram

## 📁Project File Structure
```
Real-Time-Crop-Monitoring/
│
├── code/
│   └── cropbot.ino
│
├── images/
│   ├── hardware_setup.jpg
│   └── output_dashboard.png
│
├── docs/
│   └── project_report.pdf
│
└── README.md
```

## ▶️How to Run the Project

1. Install Arduino IDE

2. Install ESP32 board support

3. Add required libraries (Blynk, DHT, WiFi)

4. Connect sensors to ESP32 as per circuit diagram

5. Update WiFi credentials, Blynk token, and Telegram Bot details

6. Upload the code to ESP32

7. Monitor data and alerts in real time

## 📸Output Screenshots

Blynk Mobile Dashboard

ThingSpeak Graphs

## Telegram Alert Messages

(Add screenshots in the images folder and link them here)

## 🚀Future Enhancements

- AI-based crop disease detection

- Automatic irrigation control

- Integration with weather forecasting APIs

- Camera-based crop monitoring using OpenCV

## 📜 License

This project is open-source and available for educational and research purposes.
