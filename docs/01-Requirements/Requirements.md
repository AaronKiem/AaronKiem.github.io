---
title: Module's Requirements
---

## Module Requirements
The table below outlines the metal detecting sensor subsystem of the CropScout exploration device by listing module requirements for processing and relaying that data to the user.


## Soil pH Sensor Subsystem
| **Requirement Description** | **Measure of<br> Threshold** | **Target<br>Measure** |**Stretch<br>Requirement<br>(Y-N)**|
|-----------------------------| ----------------- | ----------------- | :-----: |
| Surface mounted, 3.3V switching power regulator | 3.2 Volts | 3.3 Volts | No |
| Surface mounted microcontroller | 1 PIC or ESP | 8-bit PIC | No |
| Wireless Communication | Able to send or receive a Wi-Fi data | Send and receive Wi-Fi Data to MQTT | Yes |
| LDC1101DRCR (metal detecting sensor) | Able to detect metal 6 inches away | Able to produce a signal from detecting metal that is 6 inches under soil | No |

