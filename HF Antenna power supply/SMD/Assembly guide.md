# Assembly guide for HF Antenna power supply (SMD) module

## PCB requirements
In the manufacture of the device, use the material of the FR-4 printed circuit board with a thickness of 1.6 mm (this is not the best material for RF equipment, but it is the most popular and affordable). This is necessary to comply with the wave impedance of the RF line equal to 50 Ohms. If this requirement is not observed, the wave impedance of the HF line will be different from 50 Ohms, which may lead to incorrect operation of the device. Wave resistance calculations were performed for a material with Er = 4.6 (FR-4) using [Saturn PCB Design V7.08](http://www.saturnpcb.com/pcb_toolkit/).

## Components installing 
Due to the use of SMD components and relatively tight mounting, this module has some recommendations on the soldering order of components, this is necessary to facilitate soldering (no hard-to-reach areas for the soldering iron will be formed).
Also, it is strongly recommended that you **use an antistatic wrist strap and do not use soldering irons that are powered directly from the 220V / 110V network**, which can damage some sensitive components when soldering.

Soldering order of components:

- Version with RPP: C1 -> C2 -> L1 -> C3 -> R2 -> C4 -> C5 -> R3 -> R4 -> C6 -> R1 -> D1 -> Q1 -> U1 -> DC1 -> SW1 -> SMA con.
- Version without RPP: C1 -> C2 -> L1 -> C3 -> R2 -> C4 -> C5 -> R3 -> R4 -> C6 -> U1 -> DC1 -> SW1 -> SMA con.

## Additional instructions
Now you need to **set the required output voltage level** to power your active antenna (read your active antenna requirements). To do this, connect the power supply and use the **variable resistor R4** to set the required output voltage level by measuring it with help a multimeter.  

To prevent damage to your receiver perform voltage measurement on the SMA Receiver connector. The value of the output voltage must be around zero. After that, you can connect the cables to the receiver and the active antenna and continue your work.  

**Remember that when using the version without protection against polarity reversal, you must take care of the correct polarity of the power supply**. In the case of supplying voltage with incorrect polarity, you can destroy the LM317 voltage regulator.

## Installation recommendations
In the event of a large amount of interference at reception, you can independently manufacture a metal case for the HF Antenna power supply module. To do this, you can use any metal box of suitable size. The box is connected to the shield of a coaxial cable (connects to the external part of the SMA connector) or wire can be used, one end of which is soldered to the box and the other to a special "SHIELD" contact on the PCB.

## Power supply recommendations
**It is recommended to use directly connected batteries** (for example, a 18650 battery pack) to power this module and not to use any intermediate transducers, either pulsed or linear (there is simply no need, voltage stabilization is performed using an LM317 chip).
