# Humidity Controlled Fan

An Arduino-based humidity control system that automatically activates a fan when humidity exceeds a predefined threshold. The project was designed to improve ventilation and reduce moisture buildup in enclosed spaces such as bathrooms, grow tents, storage areas, or small rooms.

## Project Overview

This system continuously monitors ambient humidity using a humidity sensor connected to an Arduino. When the measured humidity rises above a set level, the Arduino activates a fan through a transistor or MOSFET driver. Once humidity falls below the threshold, the fan is switched off automatically.

The goal of the project is to provide a simple, low-cost environmental control solution that operates without manual intervention.

## Features

* Real-time humidity monitoring
* Automatic fan activation
* Adjustable humidity threshold
* Low-cost components
* Easy to expand with displays, alarms, or data logging

## Hardware Used

| Component                      | Quantity |
| ------------------------------ | -------- |
| Arduino Uno/Nano               | 1        |
| DHT11 or DHT22 Humidity Sensor | 1        |
| DC Fan                         | 1        |
| MOSFET or Transistor Driver    | 1        |
| Power Supply                   | 1        |
| Jumper Wires                   | Various  |
| Breadboard (prototype stage)   | 1        |

## How It Works

1. The humidity sensor measures the surrounding air humidity.
2. The Arduino reads the sensor value.
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
5. Upload the sketch to the Arduino board.

## Results

The system successfully controlled a fan based on humidity readings, demonstrating automated environmental regulation with minimal hardware and power consumption.

## Future Improvements

* OLED/LCD display for live readings
* Data logging to SD card
* Wi-Fi monitoring using ESP32
* Adjustable threshold via buttons
* Mobile app integration

## Lessons Learned

Through this project I learned:

* Reading environmental sensors with Arduino
* Controlling higher-current devices using transistors/MOSFETs
* Implementing threshold-based automation
* Hardware troubleshooting and circuit design
* Creating embedded systems that solve real-world problems
