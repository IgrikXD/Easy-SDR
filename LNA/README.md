# LNA

An easy and quick building of LNA module at the [SMD component group](./SMD/EasyEDA). The module includes a schematic and PCB files (EasyEDA) with differences in power circuit (PCB with/without reverse polarity protection circuit, PCB with/without TCBT-14+ Bias Tee module). Based on the submitted files, you can independently manufacture a PCB or order its manufacturing at the factory. In turn, I developed PCB for the independently manufacturing based on the existing circuit. As a result, the self-made manufacture of the antenna is cheaper than buying a ready-made module.

## Current development progress:
[![Progress](https://img.shields.io/badge/LNA%28SMD%29-not%20tested-yellow.svg)](https://easyeda.com/IgrikXD/LNA-SMD) [![Progress](https://img.shields.io/badge/version-1.1.EE-blue.svg)](./SMD/EasyEDA)  

## Current available implementations at EasyEDA platform:
- [LNA (SMD)] ([Components list](./SMD/Components%20list.md), [Assembly guide](./SMD/Assembly%20guide.md))

## How does it work?
A **[Low-noise amplifier] (LNA)** is an electronic amplifier that amplifies a very low-power signal without significantly degrading its signal-to-noise ratio. An amplifier increases the power of both the signal and the noise present at its input. LNAs are designed to minimize additional noise. 

When working with SDR equipment, due to low power or large transmitter removal, it is often necessary to **amplify weak signals without significantly increasing the noise level** (working with weather satellites, weather balloons, etc.), otherwise it may be difficult to receive some signals (errors during reception, loss of communication) or impossible at all (the signal is not available or has an excessively low level). In such cases, LNA used and connected between the antenna and the receiver. **Please note that using LNA is only rational if you have an antenna tuned to a specific operating range**. If you are using an antenna not designed to work at a given frequency, the first thing you need to do is to replace your antenna with a suitable one and check the signal level.

## Basic characteristics of the LNA:

- **Input voltage:** DC 6.2 - 15 V (external source) / DC 3.3 - 5.0 V (powered via Bias Tee)
- **Maximum DC current:** 70 mA
- **Frequency range:** 50 MHz - 4 GHz (according to the datasheet on PSA4-5043+)
- **Gain:** 25.4 dB, 50 MHz / 22.1 dB, 500 MHz / 18.4 dB, 1 GHz / 13.3 dB, 2 GHz / 10.2 dB, 3 GHz / 8.0 dB, 4 GHz
- **Noise Figure:** 0.73 dB, 50 MHz / 0.65 dB, 500 MHz / 0.75 dB, 1 GHz / 0.98 dB, 2 GHz / 1.1 dB, 3 GHz / 1.44 dB, 4 GHz
- **RF connector:** SMA
- **Feed line:** 50 Ohm coaxial cable

Detailed data on the characteristics of PSA4-5043+ at different frequencies: [Typical Performance Data](./SMD/Datasheets/Amplifiers/PSA4-5043+-Typical-Performance-Data.pdf), [Typical Performance Graph](./SMD/Datasheets/Amplifiers/PSA4-5043+-Typical-Performance-Graph.pdf)

## What was used in the development?
| Source | Description |
| ------ | ------ |
| [LNA for all] | An excellent example of a ready-made LNA module based on the PSA4-5043+ IC. |
| [Low-noise amplifier] | Wikipedia article describing the principle of LNA works, main parameters and application. |
| [Mini-Circuits PSA4-5043 preamp EDN] | Review of the ready solution of the amplifier from the company Mini-Circuits (TB-653+), based on the PSA4-5043+ IC. |
| [Mini-Circuits PSA4-5043+] | Used technical documentation on the recommended PCB layout and the recommended use of components. |

[LNA (SMD)]: <https://easyeda.com/IgrikXD/LNA-SMD>
[LNA for all]: <http://lna4all.blogspot.com/2013/04/lna-for-all-low-noise-amplifier-for.html>
[Low-noise amplifier]: <https://en.wikipedia.org/wiki/Low-noise_amplifier>
[Mini-Circuits PSA4-5043 preamp EDN]: <https://www.edn.com/electronics-blogs/emc-emi-rfi-esd/4397653/Mini-Circuits-PSA4-5043-preamp>
[Mini-Circuits PSA4-5043+]: <https://www.minicircuits.com/WebStore/dashboard.html?model=PSA4-5043%2B>