# Assembly guide for PI Attenuator (SMD) module

## PCB requirements
In the manufacture of the device, use the material of the FR-4 printed circuit board with a thickness of 1.6 mm (this is not the best material for RF equipment, but it is the most popular and affordable). This is necessary to comply with the wave impedance of the RF line equal to 50 Ohms. If this requirement is not observed, the wave impedance of the RF line will be different from 50 Ohms, which may lead to incorrect operation of the device. Wave resistance calculations were performed for a material with Er = 4.6 (FR-4) using [Saturn PCB Design V7.08](http://www.saturnpcb.com/pcb_toolkit/).

## Components installing 
Due to the use of SMD components and relatively tight mounting, this module has some recommendations on the soldering order of components, this is necessary to facilitate soldering (no hard-to-reach areas for the soldering iron will be formed).

Soldering order of components:

- Rz -> Rx -> Ry -> SMA con.

## Installation recommendations
Connect the attenuator between the antenna and the SDR receiver. Or, in the case of using an upconverter - between the antenna and the upconverter, this solution will also avoid overloading the upconverter's input.

If you use PI Attenuator, you will lose the ability to use software selectable Bias Tee (if this is offered by your SDR receiver). Therefore, **if you use an active antenna (for example, Mini-Whip), you will definitely need to use a separate Power Feed Unit that is connected between the antenna and the PI Attenuator.**

In the event of a large amount of interference at reception, you can independently manufacture a metal case for the attenuator. To do this, you can use any metal box of suitable size. The box is connected to the shield of a coaxial cable (connects to the external part of the SMA connector) or wire can be used, one end of which is soldered to the box and the other to a special "SHIELD" contact on the attenuator PCB.
