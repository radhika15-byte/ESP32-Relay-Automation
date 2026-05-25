# ESP32-Relay-Automation
ESP32 + MQTT based smart relay automation system using Adafruit IO for real-time relay monitoring and control.

# Features
1.4-channel relay control using ESP32
2.Physical push-button switching
3.Real-time cloud synchronization
4.MQTT-based communication using Adafruit IO
5.Remote relay monitoring and control
6.Wi-Fi enabled automation system
7.Bidirectional relay status updates

# Hardware Requirements
 ESP32 Development Board
 4-Channel Relay Module
 Push Buttons / Switches
 Jumper Wires
 Breadboard
 Power Supply

# Software Requirements
 Arduino IDE
 ESP32 Board Package
 Adafruit IO Arduino Library
 WiFi Library
 
# Circuit Connections
 Relay   | ESP32 GPIO 
---------|------------
 Relay 1 | GPIO 2 
 Relay 2 | GPIO 5 
 Relay 3 | GPIO 14 
 Relay 4 | GPIO 15 

 Button   | ESP32 GPIO 
----------|-----------
 Button 1 | GPIO 32 
 Button 2 | GPIO 33 
 Button 3 | GPIO 34 
 Button 4 | GPIO 35 

# Working Principle

The ESP32 connects to the Adafruit IO cloud platform through Wi-Fi using MQTT protocol.
Each push button controls a corresponding relay locally.
Relay status is updated to the cloud dashboard in real time.
Cloud commands from Adafruit IO can also control relays remotely.
The system maintains bidirectional synchronization between hardware and cloud interface.

# MQTT Architecture
ESP32 → MQTT Client
Adafruit IO → MQTT Broker
Relay Feeds → MQTT Topics

# MQTT Operations
save() → Publish relay status
               onMessage() → Subscribe to cloud updates

# The dashboard displays:
Relay ON/OFF status
Real-time device synchronization
Remote control interface

# Applications
Home Automation
Smart Switching Systems
Remote Electrical Control
IoT-based Appliance Management
Industrial Automation Prototypes

