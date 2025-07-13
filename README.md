# 📚 RFID-Based Access Control System using ESP8266

A secure and IoT-enabled RFID access control system that uses the **ESP8266 microcontroller**, **RC522 RFID reader**, and **Google Sheets API** to log access entries (name, date, time) in real time. Designed for libraries but easily scalable for offices, hostels, labs, and smart campuses.

![RFID Setup](assets/rfid-setup.png) <!-- Optional image -->

---

## 🚀 Features

- ✅ Secure user authentication using RFID (RC522)
- 📟 Real-time feedback on 16x2 LCD
- 🔊 Buzzer alerts for granted or denied access
- 🌐 Wi-Fi-enabled logging using ESP8266
- ☁️ Data automatically logged to Google Sheets (cloud-based)
- 📈 Logs name, date, and time of each access attempt
- 🔒 Works only for pre-authorized users

---

## 🛠️ Tech Stack

- **Microcontroller:** ESP8266 (NodeMCU)
- **Sensors:** RC522 RFID reader, buzzer, 16x2 I2C LCD
- **Programming:** C/C++ (Arduino IDE)
- **Cloud Integration:** Google Sheets API (via Apps Script)
- **Libraries Used:**
  - `MFRC522.h` – RFID reader
  - `ESP8266WiFi.h` – Wi-Fi connection
  - `WiFiClientSecure.h` – HTTPS for Google Sheets
  - `LiquidCrystal_I2C.h` – LCD display

---

## 🖼️ System Architecture

```text
[RFID Card] --> [RC522 Reader] --> [ESP8266]
                                         |
                               [Authorization Check]
                                         |
                             +-----------+-----------+
                             |                       |
                      [Access Granted]        [Access Denied]
                             |                       |
              [Display on LCD + Buzzer]      [Display on LCD + Buzzer]
                             |
                [Log to Google Sheet via Wi-Fi]
