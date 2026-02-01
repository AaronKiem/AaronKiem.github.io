---
title: Module's Requirements
---

## Module Requirements
The table below outlines the soil pH sensor subsystem of the CropScout exploration device by listing module requirements for measuring pH data and relaying that data to the user.


## Soil pH Sensor Subsystem
| **Requirement Description** | **Measure of<br> Threshold** | **Target<br>Measure** |**Stretch<br>Requirement<br>(Y-N)**|
|-----------------------------| ----------------- | ----------------- | :-----: |
| Surface mounted, 3.3V switching power regulator | 3.2 Volts | 3.3 Volts | No |
| Surface mounted microcontroller | 1 PIC or ESP | 8-bit PIC | No |
| Wireless Communication | Able to send or receive a Wi-Fi data | Send and receive Wi-Fi Data to MQTT | Yes |
| pH electrode probe (sensor) | Able to accurately detect H+ ion concentration to microcontroller to nearest whole number | Sends pH data to microcontroller to relay to user to nearest tenth digit | NO |
| Probe connector (Signal conversion board) | ±1°C measurement accuracy | ±0.25°C measurement accuracy| NO |

