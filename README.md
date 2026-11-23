# Development of a School Security System Using RFID Technology

**An RFID-based student departure tracking system using Arduino, GSM communication and real-time clock technology to improve school security and parental awareness.**

## Project Overview

Student safety remains a major concern for educational institutions, particularly when students leave school premises without their parents or guardians having immediate knowledge of their departure.

This project presents the development of a School Security System using Radio Frequency Identification (RFID) technology. The system is designed to identify students as they exit school premises, record their departure date and time, and automatically send SMS notifications to their registered parents or guardians.

The system integrates an Arduino Uno microcontroller with an RFID reader, GSM communication module, Real-Time Clock (RTC), LCD display and other electronic components to provide an automated departure monitoring solution.

Each student is assigned a unique RFID card. When a card is presented to the RFID reader, the system checks its identification number against registered card IDs. Recognised cards trigger an SMS notification containing the student's departure date and time, while unrecognised cards are rejected and trigger an alert.

## Project Objectives

The major objectives of this project are:

1. To develop an RFID-based tracking system capable of monitoring student departures.
2. To integrate GSM technology for automatic SMS notifications to parents and guardians.
3. To implement accurate departure time recording using a Real-Time Clock module.
4. To evaluate the functionality and performance of the developed system.

## Key Features

- **RFID-Based Identification:** Identifies students through unique RFID card identification numbers.
- **Departure Tracking:** Records the date and time when recognised students exit the school premises.
- **Automated SMS Notifications:** Sends departure confirmation messages to registered parent or guardian phone numbers.
- **Real-Time Clock:** Provides date and time information for departure notifications.
- **LCD Interface:** Displays system status, card detection and recognition messages.
- **LED Indicators:** Provides visual feedback for recognised and unrecognised cards.
- **Buzzer Alert:** Provides audible feedback during card validation.
- **Portable Power Supply:** Uses rechargeable lithium-ion batteries and boost converters.

## Hardware Components

| Component | Function |
|---|---|
| Arduino Uno | Main microcontroller |
| RC522 RFID Reader | Reads RFID card identification numbers |
| RFID Cards/Tags | Student identification |
| GSM Module (IOT-GA6-B, as documented in the report) | SMS communication |
| DS3231 RTC Module | Date and time management |
| LCD2004 Display | Displays system messages |
| I2C LCD Interface | LCD communication |
| 18650 Lithium-ion Batteries | Power supply |
| Boost Converters | Voltage regulation |
| LEDs | Visual status indicators |
| Buzzer | Audible alerts |
| Transistor | Electronic switching |
| Resistors | Current limiting and circuit protection |

## Software and Technologies

- Arduino IDE
- C/C++ (Arduino programming)
- SPI Communication
- I2C Communication
- UART / Serial Communication
- GSM AT Commands

### Arduino Libraries

The submitted Arduino sketch uses:

- `SPI.h` – Communication with the RFID reader.
- `MFRC522.h` – RFID card detection and identification.
- `Wire.h` – I2C communication.
- `RTClib.h` – Real-Time Clock interface.
- `LiquidCrystal_I2C.h` – LCD display interface.
- `SoftwareSerial.h` – Serial communication with the GSM module.

## System Operation

The system follows the process below:

1. The Arduino initializes the connected hardware components.
2. The LCD displays the welcome and system initialization messages.
3. The system prompts the user to scan an RFID card.
4. The RC522 reader captures the unique identification number of the presented card.
5. The Arduino compares the captured identification number against registered RFID card IDs.
6. If the card is recognised, the system activates the corresponding indicator and buzzer.
7. The LCD displays the recognition status and confirms that the student may exit.
8. The RTC provides the current date and time.
9. The GSM module sends an SMS notification to the registered parent or guardian.
10. If the card is not recognised, the system denies access, activates the rejection indicator and buzzer, and displays an appropriate warning.

## Communication Protocols

| Protocol | Component | Application |
|---|---|---|
| SPI | RC522 RFID Reader | Reading RFID card data |
| I2C | RTC Module | Retrieving date and time |
| I2C | LCD Display | Displaying system information |
| UART / Serial | GSM Module | Sending SMS notifications |

## Circuit Diagram

The circuit integrates the Arduino Uno with the RFID reader, LCD display, RTC module, GSM module, LEDs, buzzer and battery power supply.

The circuit diagram is included in the `Circuit-Diagrams` directory.

## Power Supply

The system uses two 18650 rechargeable lithium-ion batteries connected in parallel.

The battery configuration provides a nominal 3.7V supply, while boost converters step up the voltage to 5V for the electronic components.

The power design considers the current requirements of the Arduino, RFID reader, LCD, RTC, indicators and GSM module.

## Testing and Results

The developed system was tested to evaluate its ability to identify RFID cards and trigger the appropriate responses.

The documented tests include:

- Recognition of registered RFID cards.
- Rejection of unregistered RFID cards.
- Display of card recognition and rejection messages.
- Activation of LED indicators and buzzer alerts.
- Recording of departure date and time.
- Transmission of SMS departure notifications to parents.

The project report includes implementation photographs, code illustrations, Serial Monitor outputs and SMS notification evidence.

## Project Limitations

The project has certain limitations, including:

- The initial implementation focuses on student departure monitoring.
- Wider deployment requires additional hardware and installation costs.
- Integration with existing school infrastructure may require modifications.
- Further testing and pilot deployment would be necessary for large-scale implementation.

## Future Improvements

Potential enhancements include:

- Integration with a centralized student information database.
- Development of a web-based monitoring dashboard.
- Introduction of a school leave application system.
- Extension of RFID monitoring to classroom attendance.
- Integration of biometric authentication.
- Improved reporting and historical departure records.

## Repository Structure

```text
RFID-School-Security-System/
│
├── README.md
│
├── Project-Report/
│   └── Final-Year-Project.pdf
│
├── Source-Code/
│   └── Arduino_C_code.ino
│
├── Circuit-Diagrams/
│   └── Circuit-Diagram.pdf
│
└── Images/
    ├── Project-Implementation/
    ├── RFID-Card-Recognition/
    └── SMS-Notifications/
```

## Academic Information

**Project Title:** Development of a School Security System Using RFID Technology

**Author:** William Folorunso Popoola

**Degree:** Bachelor of Engineering (B.Eng.) in Computer Engineering

**Institution:** Covenant University, Ota, Ogun State, Nigeria

**Department:** Electrical and Information Engineering

**Year:** 2024

## Author

**William Folorunso Popoola**

Computer Engineering | Embedded Systems | Internet of Things (IoT)

GitHub: https://github.com/MandemWill

---

This project demonstrates the application of RFID technology, embedded systems and GSM communication in developing a student departure tracking solution that promotes school security and improves communication between educational institutions and parents.
