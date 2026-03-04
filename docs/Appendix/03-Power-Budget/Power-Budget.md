---
title: Appendix - Power Budget
---

## Overview
This section will porvide an estimate for power consumption between each major component of the sound subsystem.

The Power budget spreadsheet will consist of:

* All major components
* each components part number
* each components supply voltage range
* each components absolute maximum current
* Connections between components and power rails + external power source.



![budget1](Power%20Budget.xlsx%20-%20Power%20Budget_page-0001.jpg){style width:"350" height:"300;"}

![budget2](Power%20Budget.xlsx%20-%20Power%20Budget_page-0002.jpg){style width:"350" height:"300;"}

## Conclusions

From the prepared Power Budget, the major function of the subsystem can be achieved with roughtly 500mA of current as the PIC18F47Q10 and the Inductive to Digital Converter are low-current components.

The power budget was used to cordinate which component is compatable with certain voltage ranges and whether the connected components on the power rail has enough current to power the components. In the case of this subsystem, all the components are able to be powered on a +3.3V rail with ample excess current.

## Resouces

The power budget as a PDF download is available [*here*](Power_Budget.pdf), and a Microsoft Excel Sheet [*here*](Power_Budget.xlsx).