# Home Tent System
This repo contais various files asscociated with a automated grow tent I am in the process of building. The system is setup so I can controll all the hardware that regulates the tent, and also to pull in environmental data so the conditons can be monitored. Included are diagrams of the system, and at a later date I will upload the code used in the systems. Microcontrollers are used to control the hardware of the system, and these microcontrollers are themselves controlled by open source software. 

# Home Assistant
The system works using Home Assistant (HASS) which is installed on a Raspberry Pi 4. This software can be found at this link. 

[https://www.home-assistant.io/installation/](https://www.home-assistant.io/installation/)

HASS is used for general home automation, and it allows you to control a wide variety of IOT devices from a centralised point - in this case, a Pi. I can controll HASS from my PC or phone, and the dashboard is customisable to allow me to fine tune what information is displayed to me. I am using HASS to program ESP microcontrollers: the ESP32 and NodeMCU (ESP8266). HASS has an add on which makes this process very simple, ESPHome.

# ESP Home
ESP Home is an add on to HASS which is used to produce code which can be uploaded to an ESP based microcontroller. This code brings the core functionality required for the microcontroller to communicate with the Raspberry Pi over WiFi, which includes communication, over the air updates and more. This allows the user, me, to focus on writing the code specific to the task. In this case, that is controlling relays and reading sensor data. In this system, relays are controlled to turn hardware in the tent system on and off, including fans, LEDs, lights and heaters. Sensors are situated in the tent which measure air temperature, humdity and pressure alongsside light level. ESP Home has pre-built sensor and hardware libraries, making it very simple to setup. ESP Home is found at this link.

[https://esphome.io/index.html](https://esphome.io/index.html)

## Example of HASS Dashboard
An example of the dashboard I setup is shown below.
![Example HASS Dashboard](https://github.com/h4df13ld/home_tent/blob/main/HASS%20Dashboard.png)

## Diagram of System
The system is setup as shown below.
![System Diagram](https://github.com/h4df13ld/home_tent/blob/main/Control%20System%20Diagram.png)

## Pins Breakout of Microcontrolers
The pins used for the microcontrollers are shown below.
![Pins Breakout](https://github.com/h4df13ld/home_tent/blob/main/Pins%20Used%20In%20Control%20System.png)
