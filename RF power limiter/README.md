# RF power limiter

An easy and quick building of "RF power limiter" module based on [SMD components](./SMD/EasyEDA) for weakening too strong signals during receiving process. The module includes a [schematic](./SMD/Schematics) and [PCB GERBER files](./SMD/Gerbers) with SMA connectors. Based on the submitted files, you can order PCB manufacturing at the factory ([PCBWay], [JLCPCB]). In turn, I developed PCB for the independently manufacturing based on the existing circuit. As a result, the self-made manufacture of the "PI Attenuator" module is cheaper than buying a ready-made device.

## Current development progress:
[![Progress](https://img.shields.io/badge/RF%20power%20limiter%20%28SMD%29-tested-green.svg)](https://easyeda.com/IgrikXD/bias-tee-lna-smd-enclosure_copy) [![Progress](https://img.shields.io/badge/version-1.0.EE-blue.svg)](./SMD/EasyEDA)  

## Current available implementations at EasyEDA platform:
- [RF power limiter (SMD, ENCLOSURE)] ([Components list](./SMD/Components%20list.md), [Assembly guide](./SMD/Assembly%20guide.md))

## How does it work?
The power limiter reduces the output signal from the receiving antenna when the limiting range input power is reached without distorting its waveform. As a result, at the output we get a signal with a similar shape to the input, but lower in level, which will not allow us to overload the receiver input with too strong signals (which do not meet the maximum input power requirement) and in some cases will save your receiver from physical damage. To correctly select the correct power limiter, you need to know the maximum allowable input power of your SDR receiver. For example, **RTL-SDR.COM V.3 and Airspy R2 receivers have a maximum allowable input signal level of +10 dBm**.

## Basic characteristics of the PI Attenuator module:

- **Frequency range:** 30 MHz - 3 GHz (according to the datasheet on RLM-33+, upper frequency may be unattainable with FR-4 PCB material), 3 MHz - 750 MHz (according to the datasheet on RLM-751-2WL+)  
- **Linear range insertion loss:** 0.23 dB (RLM-33+), 0.2 dB (RLM-751-2WL+)  
- **Linear range max input power:** 5 dBm (RLM-33+), -10 dBm (RLM-751-2WL+)  
- **Limiting range output power:** +11.5 dBm (RLM-33+), +8.0 dBm (RLM-751-2WL+)  
- **Limiting range input power:** +12 - +30 dBm (RLM-33+), +5 - +33 dBm (RLM-751-2WL+)  
- **RF connector:** SMA  
- **Feed line:** 50 Ohm coaxial cable  
- **Used PCB Material:** FR-4  
- **PCB thickness:** 1.6 mm  
- **PCB copper weight:** 1 oz  

[PCBWay]: <https://www.pcbway.com/>
[JLCPCB]: <https://jlcpcb.com/>
[RF power limiter (SMD, ENCLOSURE)]: <https://easyeda.com/IgrikXD/bias-tee-lna-smd-enclosure_copy>