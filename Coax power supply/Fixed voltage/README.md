# Coax power supply

An easy and quick building of Coax power supply module at the [SMD component group](./SMD/EasyEDA). The module includes a schematic and PCB files (EasyEDA) prepared for setting up into aluminum case 80 mm. x 50 mm. x 20 mm.. Based on the submitted files, you can independently manufacture a PCB or order its manufacturing at the factory. In turn, I developed PCB for the independently manufacturing based on the existing circuit. As a result, the self-made manufacture of the Coax power supply module is cheaper than buying a ready-made module.

## Current development progress:
[![Progress](https://img.shields.io/badge/Coax%20power%20supply%20(SMD)-not%20tested-yellow.svg)](https://easyeda.com/IgrikXD/antenna-power-supply-smd) [![Progress](https://img.shields.io/badge/version-1.0.EE-blue.svg)](./SMD/EasyEDA)  

## Current available implementations at EasyEDA platform:
- [Coax power supply (SMD)] ([Components list](./SMD/Components%20list.md), [Assembly guide](./SMD/Assembly%20guide.md))

## How does it work?
Coax power supply module is built on the principle of using Bias Tee. Bias Tees are the components, that are used to supply DC currents or voltages to bias RF circuits. Bias tee is a three-port device. A signal that consists of RF + DC is incident at port 1 of the Bias Tee. The capacitor blocks all DC signals from getting through to port 2 and only allows the RF signals to pass through. Whereas, the inductor in the circuit blocks all RF signals from getting through to Port 3 and allows all DC signals to get through.

![Bias Tee schematic](../../Resources/Coax%20power%20supply/Bias-Tee-schematic.png)  

A feature of this module is the stabilization of the active antennas or LNA supply voltage, which will allow to set a fixed value (DC +3.3 V) of the output voltage and avoid a situation where the antenna or LNA characteristics may change due to the instability of the supply voltage (battery discharge). This decision will positively affect the quality of the work of active antennas or LNA.

## What are the differences from the [HF Antenna power supply (SMD)] module?
The main difference between this module and "[HF Antenna power supply (SMD)] module" is that now a wideband Bias-Tee module from Mini-Circuit - [TCBT-14+] is used to supply power via a coaxial cable. This allows to increase the maximum operating frequency of this module, **which allows it to be used in radio channels with frequencies above 30 MHz** to power almost any LNA or active receiving antennas with a power supply voltage of +3.3 V without significantly affecting the useful signal and RF line. This module also has the ability to power from the built-in Li-pol battery, which allows to use it for some time without connecting an external power source (this function can be disabled by installing a resistor R0 (DNI) **instead** of soldering the battery charge controller). The last significant difference is the ability to install the PCB into an aluminum case with dimensions of 80 mm. x 50mm. x 20mm (you can purchase it on [eBay](https://www.ebay.com/sch/i.html?_from=R40&_trksid=m570.l1313&_nkw=aluminium+enclosure+80&_sacat=0)).

## Basic characteristics of the HF Antenna power supply module:

- **Frequency range:** 10 MHz - 10 GHz (according to the [datasheet on TCBT-14+](./Datasheets/Bias%20Tees/TCBT-14+-Bias-Tee-Datasheet), may not be possible with FR-4 PCB material)  
- **Power:** USB type B, DC 5 V / built-in Li-pol battery  
- **Output voltage:** DC +3.3 V  
- **Maximum output current:** 200 mA  
- **RF connector:** SMA  
- **Feed line:** 50 Ohm coaxial cable  
- **Used PCB Material:** FR-4  
- **PCB thickness:** 1.6 mm  

## What was used in the development?
| Source | Description |
| ------ | ----------- |
| [What is a Bias Tee?] | A simple definition of the concept of Bias Tee. |
| [Bias tee] | Wikipedia article describing the idea of Bias Tee in more detail. |
| [#284: Basics of RF Bias Tees including applications and examples] | A video on YouTube telling basic things about the concept of Bias Tee, there are examples of design and using of different Bias Tees. |

[TCBT-14+]: <https://www.minicircuits.com/WebStore/dashboard.html?model=TCBT-14%2B>
[HF Antenna power supply (SMD)]: <../HF%20Antenna%20power%20supply/README.md>
[Coax power supply (SMD)]: <https://easyeda.com/IgrikXD/antenna-power-supply-smd>
[What is a Bias Tee?]: <https://www.everythingrf.com/community/what-is-a-bias-tee>
[Bias tee]: <https://en.wikipedia.org/wiki/Bias_tee>
[#284: Basics of RF Bias Tees including applications and examples]: <https://www.youtube.com/watch?v=lxgpm-UXTNY>
