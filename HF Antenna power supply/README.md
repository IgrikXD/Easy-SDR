# HF Antenna power supply

An easy and quick building of HF Antenna power supply module at the [SMD component group](./SMD/EasyEDA). The module includes a schematic and PCB files (EasyEDA) with differences in power circuit (PCB with/without reverse polarity protection circuit). Based on the submitted files, you can independently manufacture a PCB or order its manufacturing at the factory. In turn, I developed PCB for the independently manufacturing based on the existing circuit. As a result, the self-made manufacture of the HF Antenna power supply module is cheaper than buying a ready-made module.

## Current development progress:
[![Progress](https://img.shields.io/badge/HF%20Antenna%20power%20supply%20%28SMD%29-tested-green.svg)](https://easyeda.com/IgrikXD/Antenna-power-supply-SMD) [![Progress](https://img.shields.io/badge/version-2.1.EE-blue.svg)](./SMD/EasyEDA)  

## Current available implementations at EasyEDA platform:
- [HF Antenna power supply (SMD)] ([Components list](./SMD/Components%20list.md), [Assembly guide](./SMD/Assembly%20guide.md))

## How does it work?
HF Antenna power supply module is built on the principle of using Bias Tee. Bias Tees are the components, that are used to supply DC currents or voltages to bias RF circuits. Bias tee is a three-port device. A signal that consists of RF + DC is incident at port 1 of the Bias Tee. The capacitor blocks all DC signals from getting through to port 2 and only allows the RF signals to pass through. Whereas, the inductor in the circuit blocks all RF signals from getting through to Port 3 and allows all DC signals to get through.

![Bias Tee schematic](../Resources/HF%20Antenna%20power%20supply/Bias-Tee-schematic.png)  

A feature of this module is the stabilization of the antenna supply voltage, which will allow to set a fixed value of the output voltage and avoid a situation where the antenna characteristics may change due to the instability of the supply voltage (battery discharge). This decision will positively affect the quality of the work of active antennas.

## Basic characteristics of the HF Antenna power supply module:

- **Input voltage:** DC 7.5 - 36 V  
- **Maximum operating frequency:** 30 MHz  
- **Output voltage (adjustable):** DC 4.79 - 15.21 V  
- **Maximum output current:** 300 mA  
- **RF connector:** SMA  
- **Feed line:** 50 Ohm coaxial cable  
- **Used PCB Material:** FR-4  
- **PCB thickness:** 1.6 mm  

## List of changes:
Version **2.1.EE**: changes of the toggle switch (SW1) on the printed circuit board, now the contacts of the case are soldered to the GND area.  
Version **2.0.EE**: the RF line width has been recalculated using [Saturn PCB Design V7.08](http://www.saturnpcb.com/pcb_toolkit/). At the moment, the resistance of the RF line is close to 50 Ohms.

## What was used in the development?
| Source | Description |
| ------ | ----------- |
| [What is a Bias Tee?] | A simple definition of the concept of Bias Tee. |
| [Bias tee] | Wikipedia article describing the idea of Bias Tee in more detail. |
| [#284: Basics of RF Bias Tees including applications and examples] | A video on YouTube telling basic things about the concept of Bias Tee, there are examples of design and using of different Bias Tees. |
| [PA0RDT Mini-Whip] | A part of the antenna PFU circuit is used. The original solution has been modified. |


[HF Antenna power supply (SMD)]: <https://easyeda.com/IgrikXD/Antenna-power-supply-SMD>
[What is a Bias Tee?]: <https://www.everythingrf.com/community/what-is-a-bias-tee>
[Bias tee]: <https://en.wikipedia.org/wiki/Bias_tee>
[#284: Basics of RF Bias Tees including applications and examples]: <https://www.youtube.com/watch?v=lxgpm-UXTNY>
[PA0RDT Mini-Whip]: <http://dl1dbc.net/SAQ/Mwhip/pa0rdt-Mini-Whip.pdf>
