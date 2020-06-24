# SPDT Antenna switch

An easy and quick building of "SPDT Antenna switch" module based on [SMD components](./SMD/EasyEDA) and used for switching receiving antennas. The module includes a [schematic](./SMD/Schematics) and [PCB](./SMD/Gerbers) prepared for setting up into aluminum enclosure with dimensions 80 x 50 x 20 mm with SMA connectors. Based on the submitted files, you can order PCB manufacturing at the factory ([PCBWay], [JLCPCB]). In turn, I developed PCB for the independently manufacturing based on the existing circuit. As a result, the self-made manufacture of the "SPDT Antenna switch" module is cheaper than buying a ready-made device.

## Current development progress:
[![Progress](https://img.shields.io/badge/SPDT%20Antenna%20switch%20(SMD,%20ENCLOSURE)-not%20tested-yellow.svg)](https://easyeda.com/IgrikXD/hf-upconverter-smd-enclosure) [![Progress](https://img.shields.io/badge/version-1.0.EE-blue.svg)](./SMD/EasyEDA)  

## Current available implementations at EasyEDA platform:
- [SPDT Antenna switch (SMD, ENCLOSURE)] ([Components list](./SMD/Components%20list.md), [Assembly guide](./SMD/Assembly%20guide.md))

## How does it work?
This device works on the principle of simple switching the desired antenna input (RF IN 1 / RF IN 2) and connecting it to the device output (RF OUT). This works in much the same way as if you had two independent antennas and alternately connected them to your SDR receiver as needed, disconnected one of them and connected the other. Only in the case of using this module, such switching will be carried out by means of a special chip - SPDT switch AS169-73LF. 

![SPDT switch diagram](../Resources/SPDT%20Antenna%20switch/SPDT-Switch-diagram.png) 

This allows you to switch the receiving antennas at a much higher speed and can really come in handy when you want to check how much a particular antenna works better while you are receiving a weak, short-time radio signal. Also, this saves time spent physically disconnecting the antenna from the coaxial input of the SDR receiver and connecting a new receiveng antenna.

## Basic characteristics of the SPDT Antenna switch module:

- **Input voltage:** USB type B, DC 5 V  
- **Frequency range:** 300 kHz - 2.5 GHz (according to the [datasheet on AS169-73LF](./SMD/Datasheets/Switches/AS169-73LF-Switch-Datasheet.pdf))  
- **Insertion loss:** 0.3 dB (300 kHz - 1 GHz), 0.4 dB (1 - 2.5 GHz)  
- **Isolation:** 25 dB (300 kHz - 1 GHz), 24 dB (1 - 2.5 GHz) 
- **RF connector:** SMA  
- **Feed line:** 50 Ohm coaxial cable  
- **Used PCB Material:** FR-4  
- **PCB thickness:** 1.6 mm  
- **PCB copper weight:** 1 oz  

**Used only for switching receiving antennas! Using the unit in a transmitting radio channel may damage the AS169-73LF.**

## What was used in the development?
| Source | Description |
| ------ | ------ |
| [Upconverter1v3] | Analysis of a section of the circuit used to implement the pass-through mode for the radio signals. |

[PCBWay]: <https://www.pcbway.com/>
[JLCPCB]: <https://jlcpcb.com/>
[SPDT Antenna switch (SMD, ENCLOSURE)]: <https://easyeda.com/IgrikXD/spdt-antenna-switch-smd-enclosure>
[Upconverter1v3]: <https://github.com/opendous/Upconverter1v3>
