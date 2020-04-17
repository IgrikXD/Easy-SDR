# Coax power supply, fixed voltage

An easy and quick building of "Coax power supply, fixed voltage" module at the [SMD component group](./SMD/EasyEDA) for power active antennas and amplifiers through a coaxial cable. The module includes a schematic and PCB files ([GERBER](./SMD/Gerbers)) prepared for setting up into aluminum enclosure with dimensions 80 mm. x 50 mm. x 20 mm. with SMA connectors. Based on the submitted files, you can order PCB manufacturing at the factory. In turn, I developed PCB for the independently manufacturing based on the existing circuit. As a result, the self-made manufacture of the "Coax power supply, fixed voltage" module is cheaper than buying a ready-made module.

## Current development progress:
[![Progress](https://img.shields.io/badge/Coax%20power%20supply,%20fixed%20voltage%20(SMD,%20ENCLOSURE)-not%20tested-yellow.svg)](https://easyeda.com/IgrikXD/coax-power-supply-smd-enclosure) [![Progress](https://img.shields.io/badge/version-1.0.EE-blue.svg)](./SMD/EasyEDA)  

## Current available implementations at EasyEDA platform:
- [Coax power supply, fixed voltage (SMD, ENCLOSURE)] ([Components list](./SMD/Components%20list.md), [Assembly guide](./SMD/Assembly%20guide.md))

## How does it work?
Coax power supply module is built on the principle of using Bias Tee. Bias Tees are the components, that are used to supply DC currents or voltages to bias RF circuits. Bias tee is a three-port device. A signal that consists of RF + DC is incident at port 1 of the Bias Tee. The capacitor blocks all DC signals from getting through to port 2 and only allows the RF signals to pass through. Whereas, the inductor in the circuit blocks all RF signals from getting through to Port 3 and allows all DC signals to get through.

![Bias Tee schematic](../../Resources/Coax%20power%20supply/Bias-Tee-schematic.png)  

A feature of this module is the stabilization of the active antennas or LNA supply voltage, which will allow to set a fixed value of the output voltage and avoid a situation where the antenna or LNA characteristics may change due to the instability of the supply voltage (for example, battery discharge). This decision will positively affect the quality of the work of active antennas or LNA achievinh consistent performance throughout the entire operating time.

## What are the differences from the [HF Antenna power supply (SMD)] module?
The main difference between this module and "[HF Antenna power supply (SMD)] module" is that now a wideband Bias-Tee module from Mini-Circuit - [TCBT-14+] is used to supply end devices (active antenna, LNA) through a coaxial cable. This allows to increase the maximum operating frequency of this module, which allows it to be used in radio channels with frequencies up to 10 GHz (may be unattainable with FR-4 PCB material) to power large amount of LNA or active receiving antennas without significantly affecting the useful signal and RF line. Next difference is the ability to install the PCB into an aluminum case with dimensions of 80 mm. x 50mm. x 20mm (you can purchase it on [eBay](https://www.ebay.com/sch/i.html?_from=R40&_trksid=m570.l1313&_nkw=aluminium+enclosure+80&_sacat=0)).

## Basic characteristics of the Coax power supply, fixed voltage module:

- **Input voltage:** USB type B, DC 5 V  
- **Frequency range:** 10 MHz - 10 GHz (according to the [datasheet on TCBT-14+](./Datasheets/Bias%20Tees/TCBT-14+-Bias-Tee-Datasheet), upper frequency may be unattainable with FR-4 PCB material)  
- **Output voltage:** DC +3.3 V (can be changed by replacing the linear regulator LP5907MFX-3.3)  
- **Maximum output current:** 200 mA  
- **RF connector:** SMA  
- **Feed line:** 50 Ohm coaxial cable  
- **Used PCB Material:** FR-4  
- **PCB thickness:** 1.6 mm  
- **PCB copper weight:** 1 oz  

## What was used in the development?
| Source | Description |
| ------ | ----------- |
| [What is a Bias Tee?] | A simple definition of the concept of Bias Tee. |
| [Bias tee] | Wikipedia article describing the idea of Bias Tee in more detail. |
| [#284: Basics of RF Bias Tees including applications and examples] | A video on YouTube telling basic things about the concept of Bias Tee, there are examples of design and using of different Bias Tees. |

[TCBT-14+]: <https://www.minicircuits.com/WebStore/dashboard.html?model=TCBT-14%2B>
[HF Antenna power supply (SMD)]: <../HF%20Antenna%20power%20supply/README.md>
[Coax power supply, fixed voltage (SMD, ENCLOSURE)]: <https://easyeda.com/IgrikXD/coax-power-supply-smd-enclosure>
[What is a Bias Tee?]: <https://www.everythingrf.com/community/what-is-a-bias-tee>
[Bias tee]: <https://en.wikipedia.org/wiki/Bias_tee>
[#284: Basics of RF Bias Tees including applications and examples]: <https://www.youtube.com/watch?v=lxgpm-UXTNY>