# Smart Irrigation / Ultrasonic Water Control System

An Arduino-based project demonstrating ultrasonic distance measurement and digital output control.

## Project Overview

This project uses an ultrasonic sensor to measure distance and controls a digital output on Arduino pin 7 according to a 20 cm threshold.

The provided source code does not directly read soil moisture. The exact purpose of the output—such as controlling a relay or pump—depends on the connected hardware.

## Components

* Arduino-compatible board
* Ultrasonic distance sensor
* Connecting wires
* Output device connected to digital pin 7, if used in the hardware setup

## Pin Connections

| Component       | Arduino pin |
| --------------- | ----------- |
| Ultrasonic TRIG | D10         |
| Ultrasonic ECHO | D11         |
| Digital output  | D7          |

## How It Works

1. The ultrasonic sensor sends a trigger pulse.
2. The Arduino measures the returning echo duration.
3. The distance is calculated in centimetres.
4. If the measured distance is below 20 cm, pin 7 is set LOW.
5. If the distance is above 20 cm, pin 7 is set HIGH.
6. The distance is displayed in the Serial Monitor at 9600 baud.

At exactly 20 cm, neither condition changes the output, so the previous output state is retained.

## Software Requirements

* Arduino IDE
* Arduino-compatible board support

## Setup Instructions

1. Connect the ultrasonic sensor to pins D10 and D11.
2. Connect the intended digital output circuit to D7.
3. Open the `.ino` file in Arduino IDE.
4. Select the correct board and port.
5. Upload the sketch.
6. Open Serial Monitor at 9600 baud.
7. Test the distance readings and output behavior.

## Project Status
* Source Code:[Smart Irrigation system Code.txt](https://github.com/user-attachments/files/33292277/Smart.Irrigation.system.Code.txt)//EAZYTRONIC.COM
* Circuit diagram: <img width="2728" height="1536" alt="Smart Irrigation system Diagram" src="https://github.com/user-attachments/assets/6aa2f6b2-7885-4ec4-8bbf-81812531fa20" />

* Hardware testing Student Video: https://github.com/user-attachments/assets/b89dd4a4-60bc-4944-b187-8ac09ce69bff










  
## Safety Note

If pin 7 controls a pump or relay, verify the circuit and electrical ratings before powering the load. Do not connect a high-current pump directly to an Arduino GPIO pin.

## Author

**Imran Khan**

* GitHub: https://github.com/Imran-khan009
* Portfolio: https://sengrimrankhan.netlify.app
