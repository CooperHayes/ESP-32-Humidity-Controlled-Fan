# Humidity Controlled Fan

An ESP32-based humidity control system that automatically activates a fan when humidity exceeds a predefined threshold while continously displaying data from a DHT22 sensor on a .96 SSD1306 OLED display.

## Project Overview

This system continuously monitors local humidity using a humidity sensor connected to an ESP32. When the measured humidity rises above a set level, the the ESP32 sends a signal to the MOSFET gate which then allows for current to flow through the 5V fan. Once humidity falls below the threshold, the fan is switched off automatically.

The goal of the project is to provide a simple, low-cost environmental control that operates without manual intervention.

## Features

* Real-time humidity monitoring
* Automatic fan activation
* Digital presentation of temperature and humidity
* Low-cost components
* Easy to expand with displays, alarms, or data logging

## Hardware Used

| Component                      | Quantity |
| ------------------------------ | -------- |
| ESP32 Controlller              | 1        |
| .96 SSD1306 OLED Display       | 1        |
| DHT11 or DHT22 Humidity Sensor | 1        |
| Bare Wire 5V Fan               | 1        |
| MOSFET or Transistor Driver    | 1        |
| 220 Ω Resistor                 | 1        |
| 10 kΩ Resistor                 | 1        |
| Power Supply                   | 1        |
| Jumper Wires                   | Various  |
| Breadboard (prototype stage)   | 1        |

## Wiring

A complete wiring diagram is provided in the repository documentation. Refer to the diagrams folder for detailed circuit schematics, pin assignments, and component connections.

The wiring diagram illustrates:

* Humidity sensor connections
* Fan driver (MOSFET) circuitry
* Resistor placement
* OLED display connections
* Arduino pin assignments


## How It Works

1. The humidity sensor measures the surrounding air humidity.
2. The ESP32 reads the sensor value.
3. If humidity exceeds the configured threshold:
   * Fan turns ON.
4. If humidity drops below the threshold:
   * Fan turns OFF.
5. The cycle repeats continuously.


## Software

The project is programmed using the Arduino IDE.

Required libraries:

* DHT Sensor Library
* Adafruit Unified Sensor Library
* Adafruit GFX Library
* Wire Library

## Installation

1. Clone this repository.
2. Open the `.ino` file in Arduino IDE.
3. Install required libraries.
4. Connect the hardware according to the wiring diagram.
5. Upload the sketch to the ESP32 board.

## Results

The system successfully controlled a fan based on humidity readings, demonstrating automated environmental regulation with minimal hardware and allowed for safe power consumption through the use of a MOSFET.

## Future Improvements

* Data logging to SD card
* Adjustable threshold via buttons
* Mobile app integration
* Pulse Width Modulation for accurate control

## Lessons Learned

Through this project I learned:

* Reading environmental sensors with ESP32
* Controlling higher-current devices using MOSFETs
* Implementing threshold-based automation
* Hardware troubleshooting and circuit design
