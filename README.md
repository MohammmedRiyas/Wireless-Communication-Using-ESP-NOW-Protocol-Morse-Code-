# ESP-NOW Wireless Morse Code Communication

## Overview
This project enables wireless Morse code communication between two ESP32 devices using the ESP-NOW protocol. The sender translates button presses into Morse code, transmits them wirelessly, and the receiver decodes the Morse code and displays the corresponding character on a 128x64 OLED screen.

## Features
- Wireless Morse code transmission using ESP-NOW
- Button-based Morse code input
- Automatic Morse code encoding and decoding
- 128x64 OLED display output for received characters
- Clears display after 5 seconds of inactivity

## Hardware Requirements
- 2x ESP32 development boards
- 2x 128x64 OLED displays (I2C)
- Push button
- Connecting wires

## Software Requirements
- Arduino IDE with ESP32 board support
- Adafruit GFX Library
- Adafruit SSD1306 Library

## Wiring
### Transmitter & Receiver ESP32
| Component  | ESP32 Pin |
|------------|----------|
| OLED SDA   | GPIO 21  |
| OLED SCL   | GPIO 22  |
| Button     | GPIO 15  |

## Installation & Usage
1. Install the required libraries in Arduino IDE:
   - Adafruit GFX
   - Adafruit SSD1306
2. Configure the receiver MAC address in the code:
   ```cpp
   uint8_t receiverMAC[] = {MAC}; // Replace with the correct MAC
   ```
3. Upload the code to both ESP32 boards.
4. Power up the devices and start transmitting Morse code by pressing the button.
5. The received Morse code will be displayed on the OLED screen.

## Morse Code Encoding Rules
- Short press (<500ms) = Dot (`.`)
- Long press (≥500ms) = Dash (`-`)
- After releasing the button for 500ms, the code is transmitted

## Expected Output
### Sender
```
Message sent successfully: .-
```
### Receiver
```
Received Morse Code: .-
Decoded Character: A
```
The OLED display will show:
```
A
```

## Enhancements
- Implement bidirectional communication
- Improve Morse code timing accuracy
- Add support for additional special characters


## Author
Mohammed Riyas N

Harish Karthic 

