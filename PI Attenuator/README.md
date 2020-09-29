# PI Attenuator

An easy and quick building of "PI Attenuator" module based on [SMD components](./SMD/EasyEDA) for weakening too strong signals during receiving process. The module includes a [schematic](./SMD/Schematics) and [PCB GERBER files](./SMD/Gerbers) with SMA connectors. Based on the submitted files, you can order PCB manufacturing at the factory ([PCBWay], [JLCPCB]). In turn, I developed PCB for the independently manufacturing based on the existing circuit. As a result, the self-made manufacture of the "PI Attenuator" module is cheaper than buying a ready-made device.

## Current development progress:
[![Progress](https://img.shields.io/badge/PI%20Attenuator%20%28SMD%29-tested-green.svg)](https://easyeda.com/IgrikXD/PI-Attenuator-SMD) [![Progress](https://img.shields.io/badge/version-4.0.EE-blue.svg)](./SMD/EasyEDA)  

## Current available implementations at EasyEDA platform:
- [PI Attenuator (SMD)] ([Components list](./SMD/Components%20list.md), [Assembly guide](./SMD/Assembly%20guide.md))

## How does it work?
An attenuator is an electronic device that reduces the power of a signal without appreciably distorting its waveform.

**What is an attenuator for?**
Fixed attenuators in circuits are used to lower voltage, dissipate power, and to improve impedance matching. In measuring signals, attenuator pads or adapters are used to lower the amplitude of the signal a known amount to enable measurements, or to protect the measuring device from signal levels that might damage it. Attenuators are also used to "match" impedance by lowering apparent SWR.

An example of using an attenuator can be the situation when in the immediate vicinity of you there is a powerful transmitting radio station. If the transmitter power is high, the signal will cause a strong overload of the receiver and make its normal operation impossible. When using an attenuator, you can smoothly reduce the amplitude of the received signal without distorting the signal itself and perform its further processing. Unlike the software-implemented attenuator, the hardware implemented attenuator will not allow you to overload the input of your SDR receiver. Since in the case of hardware overload, further software processing of the signal will be practically impossible.

## Basic characteristics of the PI Attenuator module:

- **Maximum power dissipation:** 300 mW / 24.77 dBm
- **Attenuation range:** 1 - 50 dB (see list of parameters in schematic file or [Components list](./SMD/Components%20list.md))
- **RF connector:** SMA
- **Feed line:** 50 Ohm coaxial cable
- **Used PCB Material:** FR-4
- **PCB thickness:** 1.6 mm
- **PCB copper weight:** 1 oz

## List of changes:
Version **4.0.EE**: removed old versions of PCBs due to the bulkiness of the end device in the case of their use. In this case, it would be much more optimal to use ready-made SMA attenuators.  
Version **3.0.EE**: added versions of PCBs with the possibility of installation in an aluminum enclosure with dimensions of 50 x 25 x 25 mm.  
Version **2.0.EE**: the RF line width has been recalculated using [Saturn PCB Design V7.08](http://www.saturnpcb.com/pcb_toolkit/). At the moment, the resistance of the RF line is close to 50 Ohms.

## What was used in the development?
| Source | Description |
| ------ | ----------- |
| [Attenuator] | Wikipedia article describing the principle of attenuators works. Describes the existing schemes of attenuators, explains the basic working characteristics. |
| [Аттенюатор] | Translation of the above article into Russian. |
| [PI Attenuator Calculator] | Online calculator for calculating the parameters of the PI Attenuator. |

[PCBWay]: <https://www.pcbway.com/>
[JLCPCB]: <https://jlcpcb.com/>
[PI Attenuator (SMD)]: <https://easyeda.com/IgrikXD/PI-Attenuator-SMD>
[Attenuator]: <https://en.wikipedia.org/wiki/Attenuator_(electronics)>
[Аттенюатор]: <https://ru.wikipedia.org/wiki/%D0%90%D1%82%D1%82%D0%B5%D0%BD%D1%8E%D0%B0%D1%82%D0%BE%D1%80>
[PI Attenuator Calculator]: <http://www.leleivre.com/rf_pipad.html>
