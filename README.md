# 🌱 Smart Soil Moisture Monitoring and Pump Control System

Welcome to the **Smart Soil Moisture Monitoring and Pump Control System** repository! This project leverages the power of **ESP8266** and **Blynk** to monitor soil moisture levels and control a water pump intelligently or remotely. 🚀

---

## ✨ Features

- 🌡️ **Real-Time Moisture Monitoring**: Continuously measures soil moisture levels using an analog sensor.
- 💡 **Automated Pump Control**: Automatically activates the pump when moisture levels drop below a threshold.
- 📱 **Remote Control via Blynk**: Override automation to manually control the pump speed and operation using the Blynk app.
- 🔔 **Notifications**: Sends alerts when soil moisture is critically low.

---

## 🛠️ Hardware Requirements

- ESP8266 WiFi Module
- Soil Moisture Sensor
- Water Pump (PWM compatible)
- Relay Module (if required for the pump)
- Resistors and Jumper Wires
- Power Supply

---

## 🖥️ Software Requirements

- Arduino IDE
- Blynk App (Available on [Android](https://play.google.com/store/apps/details?id=cc.blynk) & [iOS](https://apps.apple.com/app/blynk/id808760481))

---

## 📋 Circuit Diagram

1. Connect the **soil moisture sensor** output to pin `A0`.
2. Connect the **pump control pin** to GPIO pin `4`.
3. Power the ESP8266 with a 3.3V-5V source.
4. Use a relay if the pump operates at higher voltages.

---

## 🚀 Getting Started

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/smart-soil-monitoring.git
   ```

2. Open the `soil_monitor.ino` file in the Arduino IDE.

3. Install the required libraries:
   - [Blynk](https://github.com/blynkkk/blynk-library)
   - ESP8266WiFi

4. Configure your WiFi credentials and Blynk authentication token:
   ```cpp
   char auth[] = "YourAuthToken";
   char ssid[] = "YourWiFiName";
   char pass[] = "YourWiFiPassword";
   ```

5. Upload the code to your ESP8266.

---

## 📱 Blynk App Setup

1. Create a new project in the Blynk app.
2. Add the following widgets:
   - **Gauge** (V2) to display raw sensor data.
   - **Gauge** (V3) to display moisture percentage.
   - **Switch** (V6) to enable/disable remote control mode.
   - **Slider** (V5) to adjust pump speed manually.
3. Link the virtual pins as defined in the code.

---

## 🔍 How It Works

1. **Automated Mode**:
   - The pump activates automatically if the soil moisture falls below 50%.
   - A notification is sent via Blynk when moisture is critically low.

2. **Remote Mode**:
   - Toggle the pump control switch in the Blynk app to enable manual override.
   - Adjust the pump speed using the slider.

---

## 📊 Data Flow

| Virtual Pin | Widget       | Purpose                      |
|-------------|--------------|------------------------------|
| V2          | Gauge        | Raw sensor data             |
| V3          | Gauge        | Soil moisture percentage    |
| V6          | Switch       | Enable/Disable remote mode  |
| V5          | Slider       | Adjust pump speed           |

---

## ⚠️ Safety Notes

- Ensure proper insulation of electronic components near water.
- Use a relay for high-voltage pumps to avoid damaging the ESP8266.
- Test the circuit in a controlled environment before deploying it.

---

## 🤝 Contributions

Feel free to fork this repository, open issues, or submit pull requests to improve the project. Let's make agriculture smarter together! 🌾

---

### 🌟 Happy Farming with Technology! 🌟

