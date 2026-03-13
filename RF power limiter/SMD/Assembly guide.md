# Assembly guide for RF power limiter (SMD, ENCLOSURE) module

## PCB requirements
In the manufacture of the device, use the material of the FR-4 printed circuit board with a thickness of 1.6 mm and copper weight equal to 1 oz (this is not the best material for RF equipment, but it is the most popular and affordable). This is necessary to comply with the wave impedance of the RF line equal to 50 Ohms. If this requirement is not observed, the wave impedance of the RF line will be different from 50 Ohms, which may make additional losses to the useful signal when the device is running. Wave resistance calculations were performed for a material with Er = 4.6 (FR-4) using [Saturn PCB Design V7.08](http://www.saturnpcb.com/pcb_toolkit/) toolkit.

## Components installing 
Due to the use of SMD components and relatively tight mounting, this module has some recommendations on the soldering order of components, this is necessary to facilitate soldering (no hard-to-reach areas for the soldering iron will be formed).

Soldering order of components:

- U1 -> SMA con.

After assembly, clean the PCB to remove any flux residues and prepare an aluminum enclosure with dimensions of 50 x 50 x 25 mm for installing the PCB. Disassemble the metal case and cut holes in the side covers so that the SMA connectors pass through them freely.

Install the PCB in one of the parts of the case by placing it on the appropriate chassis. Screw the side covers of the case to the part of the case where the PCB is installed and tighten the nuts on the SMA connectors, this will allow you to align and fix the PCB inside the case.

Screw the top cover of the aluminum enclosure. Now the device is ready to work.

## Installation recommendations
Connect the RF power limiter between the antenna and the SDR receiver. Or, in the case of using an upconverter - between the antenna and the upconverter, this solution will also protect the upconverter's input from too strong signals.

If you use RF power limiter, you will lose the ability to use software selectable Bias Tee (if this is offered by your SDR receiver). Therefore, **if you use an active antenna (for example, [Mini-Whip](https://easyeda.com/IgrikXD/Antenna_Mini_Whip_SMD-74e9e6740b814f6c901a811855125754)) or [Bias Tee powered LNA](https://easyeda.com/IgrikXD/bias-tee-lna-smd-enclosure), you will definitely need to use a separate Power Feed Unit that is connected between the antenna and the power limiter.**