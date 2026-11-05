# DIGITAL PROTECTION RELAY WITH IoT

## Project Overview

The **Digital Protection Relay with IoT** is an ESP32-based electrical monitoring and protection prototype designed to monitor electrical parameters, identify abnormal operating conditions, and provide system status through a local web dashboard.

The system integrates voltage sensing, current sensing, an OLED display, relay control, LED indicators, and a buzzer. The ESP32 processes sensor inputs and provides local and Wi-Fi-based monitoring.

This project demonstrates the integration of embedded systems, electrical protection concepts, and Internet of Things (IoT) technology.

## Features

* AC voltage monitoring using the ZMPT101B sensor.
* Current sensing using the ACS712 5A sensor.
* ESP32-based processing and control.
* OLED display for local monitoring.
* Relay-based load switching.
* Green, yellow, and red LED status indicators.
* Buzzer for audible alerts.
* Wi-Fi connectivity.
* Web dashboard interface for monitoring.
* Configurable protection thresholds in the dashboard design.
* Fault indication and relay control interface.

## Hardware Components

| Component              | Description          |
| ---------------------- | -------------------- |
| ESP32-DEVKIT-D         | Main microcontroller |
| ZMPT101B               | AC voltage sensor    |
| ACS712 5A              | Current sensor       |
| 1-Channel Relay Module | Load switching       |
| 0.96-inch OLED         | Display module       |
| Green LED              | Normal status        |
| Yellow LED             | Warning status       |
| Red LED                | Fault status         |
| Piezo Buzzer           | Audible alert        |
| 220 Ω Resistors        | LED current limiting |
| 5V 2A Adapter          | Power supply         |

## Pin Configuration

| Component              | ESP32 GPIO |
| ---------------------- | ---------- |
| ZMPT101B Analog Output | GPIO 34    |
| ACS712 Analog Output   | GPIO 35    |
| OLED SDA               | GPIO 21    |
| OLED SCL               | GPIO 22    |
| Relay IN               | GPIO 26    |
| Buzzer                 | GPIO 27    |
| Green LED              | GPIO 18    |
| Yellow LED             | GPIO 19    |
| Red LED                | GPIO 23    |

## Working Principle

1. The ZMPT101B voltage sensor provides an analog signal corresponding to the AC voltage.
2. The ACS712 sensor provides an analog signal corresponding to the current.
3. The ESP32 receives and processes the sensor signals.
4. The OLED displays the measured values and system status.
5. The protection logic compares monitored values with predefined limits.
6. The relay and indicators respond according to the implemented protection logic.
7. Wi-Fi connectivity provides a way to access the web dashboard.

## Software Requirements

* Arduino IDE
* ESP32 Board Package
* ESP32 Arduino Core
* Adafruit GFX Library
* Adafruit SSD1306 Library
* Wi-Fi libraries supported by the ESP32 Arduino Core

## Installation and Setup

### 1. Install Arduino IDE

Download and install the Arduino IDE.

### 2. Configure ESP32

Install the ESP32 board package through the Arduino IDE Boards Manager.

### 3. Install Required Libraries

Install the following libraries through Library Manager:

* Adafruit GFX
* Adafruit SSD1306

### 4. Connect the Hardware

Connect the components according to the pin configuration table.

### 5. Upload the Code

1. Open the project firmware in Arduino IDE.
2. Select the appropriate ESP32 development board.
3. Select the correct COM port.
4. Verify the program.
5. Upload the program to the ESP32.

### 6. Access the Dashboard

Open the dashboard HTML file in a web browser.

**Note:** The current dashboard is a visual prototype using simulated readings. It is not yet connected to the ESP32 for live data communication or actual relay control.

## Applications

* Educational electrical protection prototypes.
* Embedded system development.
* Electrical parameter monitoring demonstrations.
* IoT-based monitoring system development.
* Microcontroller-based relay control experiments.

## Future Enhancements

* Live ESP32-to-dashboard communication.
* Real-time voltage and current monitoring.
* Improved sensor calibration and measurement accuracy.
* Automatic overvoltage and overcurrent protection.
* Cloud-based data logging.
* Mobile notifications for fault conditions.
* Historical measurement graphs.
* Improved protection algorithms.

## Safety Precautions

* This project is an educational prototype and is not a certified electrical protection device.
* Never connect ESP32 ADC pins directly to signals that may exceed 3.3 V.
* Verify sensor output ranges and use suitable signal conditioning.
* Disconnect power immediately if any component overheats.
* Use proper electrical isolation, fuses, enclosures, and insulation when working with AC mains.
* Initial testing should be performed using an appropriate isolated, low-voltage AC source under qualified supervision.

## Project Status

**Development Stage:** Educational Prototype

This project demonstrates electrical fault detection, relay-based protection, and IoT monitoring using ESP32.
