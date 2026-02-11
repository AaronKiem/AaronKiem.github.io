---
title: Module's Selected Major Components
---

## Module's Selected Major Components

The following sections are the selected major components necessary for  .....

>**For each of the following sections, use <ins>one of the two styles</ins> given near the end. *REMOVE THIS NOTE***

### Power Management

(**remove this note/placeholder**: this is where your 3.3 volt switching regulator, any other needed power regulator, and power source {if applicable} **THAT WERE SELECTED**)

For more details, review the ["Appendix - Component Selection Process - Power Mangement"](https://embedded-systems-design.github.io/EGR314DataSheetTemplate/Appendix/01-Componet-Selection/Component-Selection-Process/#power-management) selection.


### Sensor

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------
|
![](LDC1101DRCR.webp)<br>Option 3.<br> LDC1101DRCR<br>$4/each <br> [Link to product](https://https://www.digikey.com/en/products/detail/texas-instruments/LDC1101DRCR/8347716) | \* Measures both inductance and proximity profiling path <br>\* Higher speeds and resolution than the JDC1614 <br>|  \* Sensor coil must be designed <br>\* SPI programming required <br>\* More complex to implement    |

For more details, review the ["Appendix - Component Selection Process - Sensor"](https://embedded-systems-design.github.io/EGR314DataSheetTemplate/Appendix/01-Componet-Selection/Component-Selection-Process/#sensor) selection.


## Microcontroller 

| **Microcontroller**                                                                                                                                                                                      | **SPI, UART, I2C**                                                                                                                                    | **Pins count**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------
|
![](PIC18F47Q10.webp)<br>Option 1.<br> PIC18F47Q10<br>$3/each <br> [Link to product](https://www.digikey.com/en/products/detail/microchip-technology/PIC18F47Q10-I-P/10187785) | \* 4-wire SPI <br>\* (CSB, SCLK, SDI, SDO) <br>|  \* 11 Pins, 3.3V system |

My subsystem is of a metal detector system for the CropScout rover design. I am responsible for detecting earth metals underground and will provide an LED actuator. The system will be able to run on 3.3V