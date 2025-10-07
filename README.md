# 🌐 Automatic Streetlight Controller using Internet of Things (IoT)

An Android-based IoT application designed to **automatically control streetlights** based on ambient light levels, using real-time sensor data. This smart system significantly reduces manual intervention, improves reliability, and enhances **energy efficiency**.

## 🧠 Project Overview

This project connects a remote **LDR (Light Dependent Resistor)** sensor to the [ThingSpeak](https://thingspeak.com/) IoT platform, which sends live ambient light readings. An Android app fetches this data every 5 seconds and displays:

- 📉 **LDR Sensor Value**
- 💡 **Streetlight Status** (ON/OFF)

By monitoring the light levels, the system can automatically determine whether the streetlights should be turned ON or OFF.

## ✨ Features

- 📶 Real-time IoT data retrieval from ThingSpeak
- 🔄 Automatic status updates every 5 seconds
- 📱 Clean Android interface displaying live sensor data
- ⚡ Improves energy efficiency by avoiding unnecessary streetlight usage
- ☁️ Works with any sensor-based ThingSpeak setup

## 🛠️ Technologies Used

- Java (Android SDK)
- ThingSpeak REST API
- LDR sensor (hardware side)
- HTTP Networking
- JSON Parsing

## 📲 Screenshots

> *(Include actual app UI screenshots here if possible)*  
> Example:  
> ![App Screenshot](screenshots/streetlight_status.png)

## 🚀 How It Works

1. An LDR sensor monitors ambient light.
2. The sensor sends readings to ThingSpeak via a microcontroller (e.g., ESP8266, Arduino).
3. The Android app fetches the latest data from ThingSpeak’s API.
4. Based on the LDR value, the streetlight status (ON/OFF) is displayed in the app.

## 🧪 ThingSpeak JSON Response Sample

```json
{
  "created_at": "2025-10-07T15:00:00Z",
  "entry_id": 151,
  "field1": "365",
  "field2": "ON"
}
field1: LDR value

field2: Light status

⚙️ Setup Instructions
✅ Prerequisites
Android Studio

ThingSpeak channel with two fields:

Field 1: LDR value

Field 2: Light status (ON/OFF)

Internet connection

🔧 Configuration Steps
Clone this repository:

bash
Copy code
git clone https://github.com/your-username/streetlight-controller-iot.git
Open the project in Android Studio.

Open MainActivity.java and update your ThingSpeak credentials:

java
Copy code
private static final String CHANNEL_ID = "YOUR_CHANNEL_ID";
private static final String READ_API_KEY = "YOUR_READ_API_KEY";
Run the app on an Android device or emulator.

📅 Data Refresh Rate
The app fetches data every 5 seconds.

You can change the refresh rate in startRepeatingFetch() in MainActivity.java.

💡 Real-World Applications
Smart city infrastructure

Automated streetlight systems

Remote environmental monitoring

Energy conservation systems

🛡 License
This project is licensed under the MIT License. See LICENSE for more information.

🙌 Acknowledgements
ThingSpeak API

Android Developers documentation

Open-source community contributions

🌍 "Making cities smarter, one light at a time."

yaml
Copy code

---

### ✅ Next Steps
- Save this content as `README.md` in the root of your GitHub repo.
- Add your screenshots to a `/screenshots/` folder (optional but recommended).
- Add a `LICENSE` file if you want to open-source it (MIT is a good default).

Let me know if you want help customizing this for an academic submission, adding circuit diagrams, or explaining the hardware setup.
