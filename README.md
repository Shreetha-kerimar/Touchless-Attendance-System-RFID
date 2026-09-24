# Touchless Attendance System Using RFID

An automated, touchless attendance logging system built with Arduino Uno, RFID RC522 module, and PLX-DAQ for real-time Excel data logging.

---

## 📌 Features
- **Touchless RFID Identification**: Scans card UIDs and maps them to registered users.
- **Visual & Audio Indicators**: Uses Red/Green LEDs and a Buzzer to confirm scanning status.
- **Real-Time Data Logging**: Logs user entries, dates, and IN/OUT timestamps directly to Microsoft Excel via PLX-DAQ.

---

## 🛠️ Components Required
- **Microcontroller**: Arduino Uno
- **RFID Module**: MFRC522 RFID Reader & RFID Tags
- **Indicators**: Red LED, Green LED, Buzzer
- **Display**: LCD Display (I2C module)
- **Miscellaneous**: Jumper Wires, USB Cable
- **Software**: Arduino IDE, Microsoft Excel with PLX-DAQ v2.11

---

## 🔌 Circuit Pin Connections

| Arduino UNO Pin | Module / Component | Pin Name |
| :--- | :--- | :--- |
| **5** | Green LED | Positive (+) |
| **6** | Red LED | Positive (+) |
| **8** | Buzzer | Positive (+) |
| **9** | RFID RC522 | RST |
| **10** | RFID RC522 | SDA (SS) |
| **11** | RFID RC522 | MOSI |
| **12** | RFID RC522 | MISO |
| **13** | RFID RC522 | SCK |
| **A4** | LCD (I2C) | SDA |
| **A5** | LCD (I2C) | SCL |
| **3.3V** | RFID RC522 | 3.3V |
| **5V** | LCD (I2C) | VCC |
| **GND** | All | GND (Common Ground) |

---

## 🚀 Setup Instructions

1. **Hardware Assembly**: Wire the components according to the circuit table above.
2. **Arduino Setup**:
   - Open Arduino IDE and install required libraries (`MFRC522`, `TimeLib`, `SPI`).
   - Upload `Touchless_Attendance_System.ino` to your Arduino board.
3. **Data Logging Setup**:
   - Download and install [PLX-DAQ Data Acquisition Software](https://www.parallax.com/package/plx-daq/).
   - Close the Arduino Serial Monitor before opening Excel.
   - Open the PLX-DAQ Excel sheet, select the correct **COM Port** and baud rate (`9600`), and click **Connect**.
   - Scan RFID cards to watch attendance populate in real-time.