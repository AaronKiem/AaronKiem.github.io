---
title: Appendix - Module's Major Components Selection Process
---

## Module's Major Components Selection Process

### Power Management

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------
|
| ![](TPSM84209RKHR.jpg)<br>Option 1.<br> TPSM84209RKHR<br>$5/each<br>[link to product](https://www.digikey.com/en/products/detail/texas-instruments/TPSM84209RKHR/10273205?s=N4IgTCBcDaICoAUDKBZAHAFjABgJwCUBpACXxAF0BfIA)                 | \* Input 4.5-28V <br>\* Fixed 3.3/5V output <br>\* 2A output <br>\*  |<br>\* Requires 2-3 external capcitors |
![](MAX20457ATIF.webp)<br>Option 2. <br> MAX20457ATIF<br> $6/each<br>[Link to product](https://www.digikey.com/en/products/detail/analog-devices-inc-maxim-integrated/MAX20457ATIF-VY/11484961) | \* Smaller component <br>\* Only one IC <br> \* Input 3.5-36V output 3.3/5V | \* Needs external inductors and capacitors <br>\* More succeptible to overheating    | 
![](volt.Regulator.png)<br>Option 3.<br> LM7805<br>$0.50/each <br> [Link to product](https://www.digikey.com/en/products/detail/stmicroelectronics/L7805CV/585964) | \* Components are readily available <br>\* Able to switch from load and no load <br>|  \* Requires multiple parts <br>\* Takes up greater space <br>\* Components are susceptible to heating    |

**Choice:** Option 3: LDC1101DRCR

**Rationale:** Despite being more complicated than the JDC1614RGHR, both would require a custom coil design and a PCB layout to apply which would require research to use either parts. But the LDC1101DRCR has higher processing abilities and an available datasheet.




### Sensor
| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------
|
| ![](JDC1614RGHR.jpg)<br>Option 1.<br> JDC1614RGHR<br>$5/each<br>[link to product](https://www.digikey.com/en/products/detail/texas-instruments/LDC1614RGHR/5481860)                 | \* 3.3V power consumption<br>\* Immune to environmental contaminants<br>\* Contactless sensing   |<br>\* Requires I2C configuration <br>\* Sensor coil must be designed |
![](LJ12A3-4-Z.jpg)<br>Option 2. <br> LJ12A3-4-Z<br> $10/each<br>[Link to product](https://www.amazon.com/LJ12A3-4-Z-Inductive-Proximity-Printer-Leveling/dp/B07XGFTV2F) | \* 3 wire connection <br>\* *detects conductors, liquids, and powders | <br> \* Requires 5V\* No datasheet <br>\* From Amazon   | 
![](LDC1101DRCR.webp)<br>Option 3.<br> LDC1101DRCR<br>$4/each <br> [Link to product](https://https://www.digikey.com/en/products/detail/texas-instruments/LDC1101DRCR/8347716) | \* Measures both inductance and proximity profiling path <br>\* Higher speeds and resolution than the JDC1614 <br>|  \* Sensor coil must be designed <br>\* SPI programming required <br>\* More complex to implement    |

**Choice:** Option 3: LDC1101DRCR

**Rationale:** Despite being more complicated than the JDC1614RGHR, both would require a custom coil design and a PCB layout to apply which would require research to use either parts. But the LDC1101DRCR has higher processing abilities and an available datasheet.
