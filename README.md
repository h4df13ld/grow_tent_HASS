# Home Tent System
This repo contains information about a (somewhat) automated grow tent I am in the process of building. The system is setup so I can controll all the hardware that regulates the tent, and also to pull in environmental data so the conditons can be monitored. Included are diagrams of the system, and at a later date I will upload the code used in the systems. The system runs off an RPi + ESP Microcontrollers, which run and control various sensors and hardware.

# Home Assistant
The system works using Home Assistant (HASS) which is installed on a Raspberry Pi 4. This software can be found at this link. 

[https://www.home-assistant.io/installation/](https://www.home-assistant.io/installation/)

HASS is used for general home automation, and it allows you to control a wide variety of IOT devices from a centralised point - in this case, a Pi. I can control HASS from my PC or phone, and the dashboard is customisable to allow me to fine tune what information is displayed to me. I am using HASS to program ESP microcontrollers: the ESP32 and NodeMCU (ESP8266). HASS has an add on which makes this process very simple, ESPHome.

# ESP Home
ESP Home is an add on to HASS which is used to write code which can be uploaded to an ESP based microcontroller. This code brings the core functionality required for the microcontroller to communicate with the Raspberry Pi over WiFi, which includes communication, over the air updates and more. This allows me to focus on writing the code specific to the task. In this system, relays are controlled to turn hardware in the tent system on and off, including fans, LEDs, lights and heaters. Sensors are situated in the tent which measure air temperature, humdity and pressure alongside light level. ESP Home has pre-built sensor and hardware libraries, making it very simple to write code quickly. ESP Home is found at this link.

# Additional Functions
Alongside the above described caoabilities, the system has some other functions.
<ul>
    <li>PIR Sensor detects movement in attic to switch on loft lights</li>
    <li>WiFi switches are used to control two mains circ fans in the tent</li>
</ul>


[https://esphome.io/index.html](https://esphome.io/index.html)

## Example of HASS Dashboard
An example of the dashboard I setup is shown below.
![Example HASS Dashboard](https://github.com/h4df13ld/home_tent/blob/main/HASS%20Dashboard.png)

## Diagram of System
The overall system wiring and setup as shown below.
![System Diagram](https://github.com/h4df13ld/home_tent/blob/main/Control%20System%20Diagram.png)

## Pins Breakout of Microcontrolers
The pins used for the various microcontrollers are shown below.
![Pins Breakout](https://github.com/h4df13ld/home_tent/blob/main/Pins%20Used%20In%20Control%20System.png)

## Sensors Used
<ul>
    <li>Humidity & Temperature -> BMP280</li>
    <li>Temperature -> DS18B20</li>
    <li>Light Level -> BH1750</li>
</ul>