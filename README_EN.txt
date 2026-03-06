# MBUX-Inspired Voice Command System – Arduino & Python

## Project Overview

This project aims to develop a simple MBUX-inspired voice command system using a computer microphone, Python, and Arduino.

The system becomes active when the user says **“Hey Mercedes”** or **“Mercedes”** and provides spoken feedback. It then listens for short voice commands and produces physical outputs through Arduino.

The system can perform the following actions:

- Turn the RGB LED blue, red, or green
- Activate the servo motor
- Turn off both the LED and servo motor with the “Kapat” command
- Provide spoken feedback after the wake word is detected

This project offers a basic but effective experience in voice command recognition, serial communication, and Arduino-based physical output control, combining embedded systems and human-machine interaction.

## Components Used

- Arduino Uno  
- SG90 Servo Motor  
- RGB LED  
- Resistors (220Ω / 330Ω)  
- Jumper wires  
- Breadboard  
- Computer microphone  

## Circuit Connections

- **RGB LED**
  - Red channel → D3
  - Green channel → D5
  - Blue channel → D6
  - A resistor is used in series with each color channel
  - Common pin → GND or 5V depending on LED type

- **SG90 Servo Motor**
  - Brown → GND
  - Red → 5V
  - Orange → D9

## Python Side

On the Python side, the system performs the following tasks:

- Listening to audio from the computer microphone  
- Detecting the wake word “Hey Mercedes” / “Mercedes”  
- Providing spoken feedback to the user  
- Listening for short voice commands  
- Sending commands to Arduino through serial communication  

## Supported Commands

- **Mercedes / Hey Mercedes** → Wakes up the system  
- **Mavi** → RGB LED turns blue  
- **Kırmızı / Kirmizi** → RGB LED turns red  
- **Yeşil / Yesil** → RGB LED turns green  
- **Motor** → Activates the servo motor  
- **Kapat** → Turns off both the RGB LED and servo motor  
- **Ambiyans** → Gives spoken feedback  

## Code Files

- `main_assistant.py` → Main system flow  
- `wake_word.py` → Wake word detection  
- `command_listener.py` → Command listening  
- `test_serial.py` → Serial communication test  
- `mbux_arduino.ino` → Arduino control code  

## Learning Outcomes

- Developing a voice-controlled system with Python  
- Applying wake word logic  
- Establishing serial communication between computer and Arduino  
- Controlling RGB LED and servo motor  
- Converting voice commands into physical outputs  
- Documenting the project on GitHub  
