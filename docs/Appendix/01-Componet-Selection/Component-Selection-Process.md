---
title: Appendix - Module's Major Components Selection Process
---

## Module's Major Components Selection Process

### Power Management

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------
|
| ![](TPSM84209RKHR.jpg)<br>Option 1.<br> TPSM84209RKHR<br>$5/each<br>[link to product](https://www.digikey.com/en/products/detail/texas-instruments/TPSM84209RKHR/10273205?s=N4IgTCBcDaICoAUDKBZAHAFjABgJwCUBpACXxAF0BfIA)                 | \* Input 4.5-28V <br>\* Fixed 3.3/5V output <br>\* 2A output <br>\*  |<br>\* Requires 2-3 external capcitors |
![](AP63203WU.jpg)<br>Option 2. <br> AP63203WU-7<br> $1/each<br>[Link to product](AP63203WU-7) | \* Smaller component <br>\* Low Cost <br> \* Input 4-32V output 3.3V | \* Requires multiple parts <br>\* Single output    | 
![](LM2575D2T.webp)<br>Option 3.<br> LM2575D2T<br>$2.50/each <br> [Link to product](https://www.digikey.com/en/products/detail/onsemi/LM2575D2T-3-3R4G/1476688) | \* Robust <br>\* Simple design <br>|  \* Requires multiple parts <br>\* Takes up greater space  |

**Choice:** Option 2: AP63203WU-7

**Rationale:** The AP63203WU-7 is cheaper and is just as complex as the LM2575D2T, but with a much more balenced layout making it much easier to hand solder.




### Sensor
| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------
|
| ![](JDC1614RGHR.jpg)<br>Option 1.<br> JDC1614RGHR<br>$5/each<br>[link to product](https://www.digikey.com/en/products/detail/texas-instruments/LDC1614RGHR/5481860)                 | \* 3.3V power consumption<br>\* Immune to environmental contaminants<br>\* Contactless sensing   |\* Requires I2C configuration <br>\* Sensor coil must be designed |
![](LJ12A3-4-Z.jpg)<br>Option 2. <br> LJ12A3-4-Z<br> $10/each<br>[Link to product](https://www.amazon.com/LJ12A3-4-Z-Inductive-Proximity-Printer-Leveling/dp/B07XGFTV2F) | \* 3 wire connection <br>\* *detects conductors, liquids, and powders | <br> \* Requires 5V\* No datasheet <br>\* From Amazon <br>\* Not solder mount  | 
![](LDC1101DRCR.webp)<br>Option 3.<br> LDC1101DRCR<br>$4/each <br> [Link to product](https://https://www.digikey.com/en/products/detail/texas-instruments/LDC1101DRCR/8347716) | \* Measures both inductance and proximity profiling path <br>\* Higher speeds and resolution than the JDC1614 <br>|  \* Sensor coil must be designed <br>\* SPI programming required <br>\* More complex to implement    |

**Choice:** Option 3: LDC1101DRCR

**Rationale:** Despite being more complicated than the JDC1614RGHR, both would require a custom coil design and a PCB layout to apply which would require research to use either parts. But the LDC1101DRCR has higher processing abilities and an available datasheet.
