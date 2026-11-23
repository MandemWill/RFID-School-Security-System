# Development of a School Security System Using RFID Technology

An Arduino-based school security system designed to monitor student departures using Radio Frequency Identification (RFID) technology. The system records the departure time of students and sends SMS notifications to their parents or guardians, helping improve student safety and communication between schools and parents.

## 📌 Project Overview

Student safety is an important concern for educational institutions. Traditional methods of monitoring student movement can make it difficult for parents and school administrators to know exactly when students leave school premises.

This project presents an RFID-based school security system that automates student departure tracking. Each student is assigned an RFID card which is scanned using an RFID reader when leaving the school premises.

The system identifies the student, retrieves the current date and time using a Real-Time Clock (RTC) module, displays relevant information on an LCD screen, and sends an SMS notification to the registered parent or guardian through a GSM module.

## 🎯 Project Objectives

The main objectives of this project are to:

- Develop an RFID-based student identification system.
- Automatically record student departure times.
- Provide accurate timestamps using a Real-Time Clock module.
- Send SMS notifications to parents or guardians when students depart.
- Improve communication between schools and parents.
- Provide a simple and reliable school security monitoring solution.

## ⚙️ System Features

- **RFID Identification:** Identifies students using their registered RFID cards.
- **Departure Tracking:** Records the time students leave the school premises.
- **Real-Time Clock:** Uses the DS3231 RTC module to maintain accurate date and time.
- **SMS Notifications:** Sends departure notifications to registered parents or guardians through GSM communication.
- **LCD Display:** Displays system information and student identification details.
- **Portable Power Supply:** Uses rechargeable lithium-ion batteries with voltage regulation.

## 🛠️ Hardware Components

| Component | Description |
|---|---|
| Arduino Uno | Main microcontroller |
| RC522 RFID Reader | Reads student RFID cards |
| RFID Cards/Tags | Unique student identification |
| IOT-GA6-B GSM Module | Sends SMS notifications |
| DS3231 RTC Module | Maintains accurate date and time |
| LCD2004 Display | Displays system information |
| I2C LCD Interface | Simplifies LCD communication |
| 18650 Lithium-ion Batteries | Portable power supply |
| Boost Converter | Regulates battery voltage to 5V |
| Jumper Wires | Hardware connections |

## 💻 Software and Technologies

- Arduino IDE
- Embedded C/C++ (Arduino programming)
- SPI Communication
- I2C Communication
- GSM Communication

### Arduino Libraries

The project uses the following libraries:

- `SPI.h` – SPI communication for the RFID reader.
- `MFRC522.h` – Interface with the RC522 RFID module.
- `Wire.h` – I2C communication.
- `RTClib.h` – Interface with the DS3231 RTC module.
- `LiquidCrystal_I2C.h` – Interface with the I2C LCD display.

## 🔄 How the System Works

1. The system is powered on using its rechargeable battery supply.
2. The Arduino initializes the RFID reader, RTC module, LCD and GSM module.
3. A student presents their registered RFID card to the RC522 reader.
4. The Arduino reads the RFID card's unique identification number.
5. The system identifies the student using the registered card information.
6. The DS3231 RTC module provides the current date and departure time.
7. The LCD displays the relevant student and system information.
8. The GSM module sends an SMS notification to the student's registered parent or guardian.
9. The student's departure event is recorded with its corresponding timestamp.

## 🔌 Communication Protocols

The system uses multiple communication protocols to integrate its hardware components.

| Protocol | Component | Purpose |
|---|---|---|
| SPI | RC522 RFID Reader | RFID card identification |
| I2C | DS3231 RTC | Date and time retrieval |
| I2C | LCD Display | Display communication |
| UART | GSM Module | SMS communication |

## 🔋 Power Supply

The system uses two 18650 rechargeable lithium-ion batteries connected in parallel to provide a 3.7V nominal supply with increased capacity.

Boost converters are used to step up the battery voltage to 5V for the system's power requirements.

## 📷 Project Documentation

Project documentation, circuit diagrams, implementation photographs and additional resources will be made available in this repository.

## 🚀 Future Improvements

Potential improvements include:

- Integration with a centralized student information database.
- Development of a web-based monitoring dashboard.
- Enhanced reporting and historical departure records.
- Remote configuration and management.
- Additional security and authentication mechanisms.

## 🎓 Academic Project

**Project Title:** Development of a School Security System Using RFID Technology (Departure Tracking System)

**Degree:** Bachelor of Engineering (B.Eng.) in Computer Engineering

**Institution:** Covenant University, Nigeria

**Project Type:** Final Year Undergraduate Project

## 👨‍💻 Author

**William Folorunso Popoola**

Computer Engineering | Embedded Systems | IoT

GitHub: https://github.com/MandemWill

---

*This project was developed as an undergraduate final-year engineering project to demonstrate the application of RFID technology, embedded systems and GSM communication in improving school security and student departure monitoring.*
