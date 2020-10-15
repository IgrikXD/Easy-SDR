# LNA, Bias Tee powered

An easy and quick building of "LNA, Bias Tee powered" module based on [SMD components](./SMD/EasyEDA) and used for amplify weak radio signals without significantly increasing the noise level and compensation for loss of useful signal when passing through a coaxial cable. The module includes a [schematic](./SMD/Schematics) and [PCB GERBER files](./SMD/Gerbers) prepared for setting up into aluminum enclosure with dimensions 50 x 25 x 25 mm with N-Type connectors. Based on the submitted files, you can order PCB manufacturing at the factory ([PCBWay], [JLCPCB]). In turn, I developed PCB for the independently manufacturing based on the existing circuit. As a result, the self-made manufacture of the "LNA, Bias Tee powered" module is cheaper than buying a ready-made device.

## Current development progress:
[![Progress](https://img.shields.io/badge/LNA,%20Bias%20Tee%20powered%20%28SMD,%20ENCLOSURE%29-tested-green.svg)](https://easyeda.com/IgrikXD/bias-tee-lna-smd-enclosure) [![Progress](https://img.shields.io/badge/version-1.0.EE-blue.svg)](./SMD/EasyEDA)  

## Current available implementations at EasyEDA platform:
- [LNA, Bias Tee powered (SMD, ENCLOSURE)] ([Components list](./SMD/Components%20list.md), [Assembly guide](./SMD/Assembly%20guide.md))

## How does it work?
A **[Low-noise amplifier] (LNA)** is an electronic amplifier that amplifies a very low-power signal without significantly degrading its signal-to-noise ratio. An amplifier increases the power of both the signal and the noise present at its input. LNAs are designed to minimize additional noise. 

When working with SDR equipment, due to low power, large transmitter removal or a sufficiently long coaxial cable, which introduces additional attenuation of the useful signal, it is often necessary to **amplify weak signals without significantly increasing the noise level** (working with weather satellites, weather balloons, etc.), otherwise it may be difficult to receive some signals (errors during reception, loss of communication) or impossible at all (the signal is not available or has an excessively low level). In such cases, LNA used and connected between the antenna and the receiver. **Please note that using LNA is only rational if you have an antenna tuned to a specific operating range.** If you are using an antenna not designed to work at a given frequency, the first thing you need to do is to replace your antenna with a suitable one and check the signal level.

## Basic characteristics of the LNA, Bias Tee powered module:
- **Input voltage:** DC 3.3 - 5.0 V (powered via Bias Tee)  
- **Maximum DC current:** 76 mA (PSA4-5043+), 200 mA (PGA-103+)  
- **Frequency range:** 50 MHz - 4 GHz (according to the datasheet on [PSA4-5043+](./SMD/Datasheets/Amplifiers/PSA4-5043+-Amplifier-Datasheet.pdf) and [PGA-103+](./SMD/Datasheets/Amplifiers/PGA-103+-Amplifier-Datasheet.pdf), upper frequency may be unattainable with FR-4 PCB material)  
- **Gain characteristics table (+5 V supply voltage):**  

| Frequency         | PSA4-5043+ | PGA-103+ |
| ----------------- | ---------- | -------- |
| 50 MHz            | 25.4 dB    | 26.5 dB  |
| 400 MHz           | 22.1 dB    | 22.1 dB  |
| 1 GHz             | 18.4 dB    | 16.2 dB  |
| 2 GHz             | 13.3 dB    | 11.0 dB  |
| 3 GHz             | 10.2 dB    | 8.1 dB   |
| 4 GHz             | 8.0 dB     | 6.2 dB   |

- **Noise Figure characteristics table (+5 V supply voltage):**  

| Frequency         | PSA4-5043+ | PGA-103+ |
| ----------------- | ---------- | -------- |
| 50 MHz            | 0.73 dB    | 0.5 dB   |
| 400 MHz           | 0.65 dB    | 0.5 dB   |
| 1 GHz             | 0.75 dB    | 0.6 dB   |
| 2 GHz             | 0.98 dB    | 0.9 dB   |
| 3 GHz             | 1.1 dB     | 1.2 dB   |
| 4 GHz             | 1.44 dB    | 1.5 dB   |

- **Output IP3 characteristics table (+5 V supply voltage):**  

| Frequency         | PSA4-5043+ | PGA-103+ |
| ----------------- | ---------- | -------- |
| 50 MHz            | 31 dBm     | 36.7 dBm |
| 400 MHz           | 32.1 dBm   | 39 dBm   |
| 1 GHz             | 33.5 dBm   | 41.9 dBm |
| 2 GHz             | 32.7 dBm   | 44.6 dBm |
| 3 GHz             | 33.6 dBm   | 44.3 dBm |
| 4 GHz             | 32.6 dBm   | 45.4 dBm |

- **RF connector:** N-Type  
- **Feed line:** 50 Ohm coaxial cable  
- **Used PCB Material:** FR-4  
- **PCB thickness:** 1.6 mm  
- **PCB copper weight:** 1 oz  

Detailed data on the characteristics of PSA4-5043+ at different frequencies: [Typical Performance Data](./SMD/Datasheets/Amplifiers/PSA4-5043+-Typical-Performance-Data.pdf), [Typical Performance Graph](./SMD/Datasheets/Amplifiers/PSA4-5043+-Typical-Performance-Graph.pdf)  
Detailed data on the characteristics of PGA-103+ at different frequencies: [Typical Performance Data](./SMD/Datasheets/Amplifiers/PGA-103+-Typical-Performance-Data.pdf), [Typical Performance Graph](./SMD/Datasheets/Amplifiers/PGA-103+-Typical-Performance-Graph.pdf)

## What was used in the development?
| Source | Description |
| ------ | ------ |
| [LNA for all] | An excellent example of a ready-made LNA module based on the PSA4-5043+ IC. |
| [Low-noise amplifier] | Wikipedia article describing the principle of LNA works, main parameters and application. |
| [Mini-Circuits PSA4-5043 preamp EDN] | Review of the ready solution of the amplifier from the company Mini-Circuits (TB-653+), based on the PSA4-5043+ IC. |
| [Mini-Circuits PSA4-5043+] | Used technical documentation on the recommended PCB layout and the recommended use of components. |
| [Mini-Circuits PGA-103+] | Used technical documentation on the recommended PCB layout and the recommended use of components. |

## Similar projects:
| Project | Description |
| ------ | ------ |
| [LNA for ABS-B] | RF amplifier and / or filter design in metal case with N-Type connectors to work with ADS-B. The amplifier is built on the basis of a ready-made PSA4-5043 microcircuit, and a TA1090EC filter. The author assembles and pre-tests the finished device before publishing. |
| [LNA for RF receiver] | RF amplifier and / or filter design in metal case with N-Type connectors with Bias Tee powering supply or built-in LM1117 voltage regulator. The amplifiers are based on the off-the-shelf PSA4-5043 / PMA3-83LNW microcircuits, and have a huge variation of the applied filters. The author assembles and pre-tests the finished device before publishing. |

## Who helped improve this project?
- [eismeer89](eismeer89@gmail.com) - Proposal to use a metal enclosure in the end device and replace SMA connectors with N-Type. Consultation on technical aspects of the implementation of amplifiers and RF transmission lines.

[PCBWay]: <https://www.pcbway.com/>
[JLCPCB]: <https://jlcpcb.com/>
[LNA, Bias Tee powered (SMD, ENCLOSURE)]: <https://easyeda.com/IgrikXD/bias-tee-lna-smd-enclosure>
[LNA for all]: <http://lna4all.blogspot.com/2013/04/lna-for-all-low-noise-amplifier-for.html>
[Low-noise amplifier]: <https://en.wikipedia.org/wiki/Low-noise_amplifier>
[Mini-Circuits PSA4-5043 preamp EDN]: <https://www.edn.com/electronics-blogs/emc-emi-rfi-esd/4397653/Mini-Circuits-PSA4-5043-preamp>
[Mini-Circuits PSA4-5043+]: <https://www.minicircuits.com/WebStore/dashboard.html?model=PSA4-5043%2B>
[Mini-Circuits PGA-103+]: <https://www.minicircuits.com/WebStore/dashboard.html?model=PGA-103%2B>
[LNA for ABS-B]: <https://easyeda.com/Eismeer/lna-for-rf-receiver_copy_copy>
[LNA for RF receiver]: <https://easyeda.com/Eismeer/lna-for-rf-receiver>
