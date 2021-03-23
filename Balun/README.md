# Balun

An easy and quick building of "Balun" module based on [SMD components](./SMD/EasyEDA) used to convert a balanced signal to a unbalanced and match the impedances. The module includes a [schematic](./SMD/Schematics) and [PCB GERBER files](./SMD/Gerbers) prepared for setting up into aluminum enclosure with dimensions 50 x 50 x 25 mm with SMA connector. Based on the submitted files, you can order PCB manufacturing at the factory ([PCBWay], [JLCPCB]). In turn, I developed PCB for the independently manufacturing based on the existing circuit. As a result, the self-made manufacture of the "Balun" module is cheaper than buying a ready-made device.

## Current development progress:
[![Progress](https://img.shields.io/badge/Balun%20%28SMD,%20ENCLOSURE%29-tested-green.svg)](https://easyeda.com/IgrikXD/bias-tee-lna-smd-enclosure_copy) [![Progress](https://img.shields.io/badge/version-1.0.EE-blue.svg)](./SMD/EasyEDA)  

## Current available implementations at EasyEDA platform:
- [Balun (SMD, ENCLOSURE)] ([Components list](./SMD/Components%20list.md), [Assembly guide](./SMD/Assembly%20guide.md))

## How does it work?


## Basic characteristics of the Balun module:

- **Frequency range table:**

| Transformer:      | TC1-6+         | TC2-1T+     | TC4-1T+       | TC8-1+      | TC9-1+      | TC16-161T+    |
| ----------------- | -------------- | ----------- | ------------- | ----------- | ------------| ------------- |
| Frequency range:  | 0.15 - 350 MHz | 3 - 300 MHz | 0.5 - 300 MHz | 2 - 500 MHz | 2 - 200 MHz | 0.6 - 160 MHz |
- **Impedance ratio table:**

| Transformer:      | TC1-6+ | TC2-1T+ | TC4-1T+ | TC8-1+ | TC9-1+ | TC16-161T+ |
| ----------------- | ------ | ------- | ------- | ------ | ------ | ---------- |
| Impedance ratio:  | 1      | 2       | 4       | 8      | 9      | 16         |
- **Maximum RF power:** 0.25 W  
- **RF connector:** SMA  
- **Feed line:** 50 Ohm coaxial cable  
- **Used PCB Material:** FR-4  
- **PCB thickness:** 1.6 mm  
- **PCB copper weight:** 1 oz  

[PCBWay]: <https://www.pcbway.com/>
[JLCPCB]: <https://jlcpcb.com/>
[Balun (SMD, ENCLOSURE)]: <https://easyeda.com/IgrikXD/bias-tee-lna-smd-enclosure_copy_copy>