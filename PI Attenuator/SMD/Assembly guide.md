# Assembly guide for PI Attenuator (SMD) module

## PCB requirements
In the manufacture of the device, use the material of the FR-4 printed circuit board with a thickness of 1.6 mm and copper weight equal to 1 oz (this is not the best material for RF equipment, but it is the most popular and affordable). This is necessary to comply with the wave impedance of the RF line equal to 50 Ohms. If this requirement is not observed, the wave impedance of the RF line will be different from 50 Ohms, which may make additional losses to the useful signal when the device is running. Wave resistance calculations were performed for a material with Er = 4.6 (FR-4) using [Saturn PCB Design V7.08](http://www.saturnpcb.com/pcb_toolkit/) toolkit.

## Components installing 
Due to the use of SMD components and relatively tight mounting, this module has some recommendations on the soldering order of components, this is necessary to facilitate soldering (no hard-to-reach areas for the soldering iron will be formed).

Soldering order of components:

- Rz -> Rx -> Ry -> SMA con.

## Installation recommendations
Connect the attenuator between the antenna and the SDR receiver. Or, in the case of using an upconverter - between the antenna and the upconverter, this solution will also avoid overloading the upconverter's input.

If desired, the finished device can be packed in shrink wrap. This will protect the device from moisture and dust.

If you use PI Attenuator, you will lose the ability to use software selectable Bias Tee (if this is offered by your SDR receiver). Therefore, **if you use an active antenna (for example, [Mini-Whip](https://easyeda.com/IgrikXD/Antenna_Mini_Whip_SMD-74e9e6740b814f6c901a811855125754)) or [Bias Tee powered LNA](https://easyeda.com/IgrikXD/bias-tee-lna-smd-enclosure), you will definitely need to use a separate Power Feed Unit that is connected between the antenna and the attenuator.**
