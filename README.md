# Measuring-Water-Level-using-ESP32-and-Display-Real-Time-Data-in-Firebase

This project monitors the water level in a tank using an ultrasonic sensor connected to an ESP32. It calculates the water level in real time and uploads the data to **Firebase Realtime Database**, allowing for remote monitoring.

## 🔧 Features

* Measures distance using an ultrasonic sensor (HC-SR04)
* Calculates water level based on tank height
* Sends real-time data to Firebase Realtime Database
* Wi-Fi-enabled data transmission using ESP32
* Error handling for invalid sensor readings

## 🛠 Tech Stack

* **ESP32** microcontroller
* **HC-SR04** ultrasonic distance sensor
* **Firebase Realtime Database**
* **Arduino IDE**
* **C++**

## 📦 Hardware Required

* ESP32 Dev Board
* HC-SR04 Ultrasonic Sensor
* Jumper Wires
* Breadboard
* USB cable for programming

## 📁 Circuit Connections

| HC-SR04 Pin | ESP32 Pin |
| ----------- | --------- |
| VCC         | 5V        |
| GND         | GND       |
| TRIG        | GPIO 4    |
| ECHO        | GPIO 18   |

## 🔑 Configuration

Edit these fields in the source code:

```cpp
#define WIFI_SSID "your_wifi_ssid"
#define WIFI_PASSWORD "your_wifi_password"

#define API_KEY "your_firebase_api_key"
#define DATABASE_URL "your_firebase_database_url"
```

## 🧠 How It Works

1. The ultrasonic sensor measures the distance from the top of the tank to the water surface.
2. This distance is subtracted from the total tank height to calculate the current water level.
3. The ESP32 sends the water level to Firebase every 5 seconds.
4. Data can be monitored in real-time via the Firebase console or a connected app.

## 🔒 Security Note

Avoid hardcoding sensitive information (like API keys or passwords) in public repositories. Use environment variables or encrypted config files for production.


## 📃 License

This project is open-source and available under the [MIT License](https://opensource.org/licenses/MIT).

---

Let me know if you want a version tailored for GitHub, including images, badges, or a live demo section.
