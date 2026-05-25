# ESP32-Relay-Automation
ESP32 + MQTT based smart relay automation system using Adafruit IO for real-time relay monitoring and control.

# Features
1. 4-channel relay control using ESP32 <br>
2. Physical push-button switching <br>
3. Real-time cloud synchronization <br>
4. MQTT-based communication using Adafruit IO <br>
5. Remote relay monitoring and control <br>
6. Wi-Fi enabled automation system <br>
7. Bidirectional relay status updates <br>

# Hardware Requirements
 ESP32 Development Board <br>
 4-Channel Relay Module <br>
 Push Buttons / Switches <br>
 Jumper Wires <br>
 Breadboard <br>
 Power Supply <br>

# Software Requirements
 Arduino IDE <br>
 ESP32 Board Package <br>
 Adafruit IO Arduino Library <br>
 WiFi Library <br>
 
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

# Hardware Prototype
<img width="1600" height="1200" alt="image" src="https://github.com/user-attachments/assets/dd794c9a-e2b6-4c35-be34-acabfe188ab4" />

# Dashboard Interface
<img width="1580" height="804" alt="image" src="https://github.com/user-attachments/assets/a2954243-bb8e-4119-84fe-85803bbbd545" />


# Working Principle
The ESP32 connects to the Adafruit IO cloud platform through Wi-Fi using MQTT protocol. <br>
Each push button controls a corresponding relay locally. <br>
Relay status is updated to the cloud dashboard in real time. <br>
Cloud commands from Adafruit IO can also control relays remotely. <br>
The system maintains bidirectional synchronization between hardware and cloud interface. <br>

# MQTT Architecture
ESP32 → MQTT Client <br>
Adafruit IO → MQTT Broker <br>
Relay Feeds → MQTT Topics <br>

# MQTT Operations
save() → Publish relay status <br>
onMessage() → Subscribe to cloud updates <br>

# The dashboard displays:
Relay ON/OFF status <br>
Real-time device synchronization <br>
Remote control interface <br>

# Applications
Home Automation <br> 
Smart Switching Systems <br>
Remote Electrical Control <br>
IoT-based Appliance Management <br>
Industrial Automation Prototypes <br>

