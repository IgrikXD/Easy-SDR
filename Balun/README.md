# Balun

An easy and quick building of "Balun" module based on [SMD components](./SMD/EasyEDA) used to convert a balanced signal to a unbalanced and match the impedances. The module includes a [schematic](./SMD/Schematics) and [PCB GERBER files](./SMD/Gerbers) prepared for setting up into aluminum enclosure with dimensions 50 x 50 x 25 mm with SMA connector. Based on the submitted files, you can order PCB manufacturing at the factory ([PCBWay], [JLCPCB]). In turn, I developed PCB for the independently manufacturing based on the existing circuit. As a result, the self-made manufacture of the "Balun" module is cheaper than buying a ready-made device.

## Current development progress:
[![Progress](https://img.shields.io/badge/Balun%20%28SMD,%20ENCLOSURE%29-tested-green.svg)](https://oshwlab.com/IgrikXD/bias-tee-lna-smd-enclosure_copy_copy) [![Progress](https://img.shields.io/badge/version-1.0.EE-blue.svg)](./SMD/EasyEDA)  

## Current available implementations at EasyEDA platform:
- [Balun (SMD, ENCLOSURE)] ([Components list](./SMD/Components%20list.md), [Assembly guide](./SMD/Assembly%20guide.md))

## How does it work?
A **Balun** (from **bal**anced to **un**balanced) is a passive electronic device that converts a balanced (differential) signal to an unbalanced (single-ended) signal and vice versa. In addition to signal conversion, a balun can also perform **impedance matching** between two parts of a circuit that have different impedance values.

**Why is this needed when working with SDR?** Many antennas, such as dipoles and loops, are **balanced** by design - both conductors carry signals of equal amplitude but opposite phase relative to ground. However, most SDR receivers and coaxial cables are **unbalanced** systems where the signal is carried on one conductor relative to ground (shield). Connecting a balanced antenna directly to an unbalanced feed line without a balun causes several problems: part of the signal begins to flow along the outer surface of the coaxial cable shield (**common-mode current**), which leads to increased noise pick-up, distortion of the antenna radiation pattern and degraded reception quality.

By installing a balun between the antenna and the coaxial feed line, common-mode currents are suppressed and the antenna operates as designed. In this module, the balun is built around a **Mini-Circuits RF transformer**, which allows you to select the appropriate impedance ratio (from 1:1 to 1:16) depending on the antenna impedance and the required frequency range. For example, a classic **half-wave dipole** has an impedance of approximately **72-75 Ohm**, and a transformer with a 1:1 ratio can be used to connect it to a **50 Ohm** coaxial cable with minimal mismatch, while a **full-wave loop** antenna with an impedance of approximately **100-200 Ohm** may require a transformer with a 2:1 or 4:1 ratio to match it to the same **50 Ohm** feed line.

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