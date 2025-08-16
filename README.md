

# Garbage Monitoring and Collection Assistance

## Project Overview

This project provides a smart solution for monitoring garbage bins and assisting in efficient waste collection. It uses a NodeMCU microcontroller, ultrasonic sensor, and GPS module to measure the fill level and location of bins. Data is sent to ThingSpeak for real-time monitoring, and notifications are triggered via IFTTT when bins are nearly full. The Blynk app displays bin location and status.

---


- **source_code.ino**  
  Main firmware for NodeMCU. Handles sensor readings, GPS data, WiFi connection, ThingSpeak updates, and Blynk integration.
- **circuit.png**  
  Circuit diagram showing how to connect the NodeMCU, ultrasonic sensor, and GPS module.
- **connections.png**  
  Detailed wiring connections for hardware setup.
- **README.md**  
  Project documentation and setup instructions.
- **aditya 126.docx** & **all 3.docx**  
  Project reports or documentation (not required for setup).

---


- NodeMCU (ESP8266) 
- Ultrasonic Sensor (HC-SR04) 
- GPS Module 
- Jumper wires, breadboard, power supply

---

## Setup Instructions


### 1. Hardware Assembly <img src="https://img.icons8.com/color/24/000000/maintenance.png"/>

- Refer to circuit.png and connections.png for wiring.
- Connect the ultrasonic sensor to NodeMCU pins D4 (TRIGGER) and D5 (ECHO).
- Connect the GPS module to NodeMCU pins D2 (TX) and D1 (RX).


### 2. Firmware Upload <img src="https://img.icons8.com/color/24/000000/upload.png"/>

- Open source_code.ino in Arduino IDE.
- Install required libraries:
  - TinyGPS++
  - Blynk
  - ESP8266WiFi
- Update WiFi credentials, Blynk auth token, and ThingSpeak API key in the code.
- Upload the code to NodeMCU.


### 3. ThingSpeak Setup <img src="https://img.icons8.com/color/24/000000/cloud.png"/>

- Create a ThingSpeak channel.
- Copy the API key and paste it into source_code.ino.
- Configure fields to receive bin fill percentage.


### 4. IFTTT Integration <img src="https://img.icons8.com/color/24/000000/phone.png"/>

- Use ThingHTTP and React services to connect ThingSpeak to IFTTT.
- Create a webhook in IFTTT to trigger a call/SMS when bin fill percentage exceeds 80%.


### 5. Blynk App Setup <img src="https://img.icons8.com/color/24/000000/smartphone-tablet.png"/>

- Install the Blynk app on your phone.
- Create a new project and add a Map widget (V0) and Value Display widgets (V1-V5).
- Use the auth token from Blynk in your code.

---


## How It Works <img src="https://img.icons8.com/color/24/000000/idea.png"/>

- The ultrasonic sensor measures the distance from the top of the bin to the trash.
- The percentage filled is calculated and sent to ThingSpeak.
- GPS module provides bin location, displayed in the Blynk app.
- When the bin is 80% full, IFTTT triggers a notification to your phone.

---


## Usage <img src="https://img.icons8.com/color/24/000000/play.png"/>

1. Power up the NodeMCU with all modules connected.
2. Monitor bin status and location on ThingSpeak and Blynk app.
3. Receive notifications when bins need to be emptied.

---


## Team <img src="https://img.icons8.com/color/24/000000/conference-call.png"/>

- Hardware & Firmware: [Your Name]
- Cloud & Notification Services: [Teammate’s Name]

---


## License <img src="https://img.icons8.com/color/24/000000/copyright.png"/>

For educational and demonstration purposes.

---

Let me know if you want to add more details or personalize the team section!