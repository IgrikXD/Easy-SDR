# Assembly guide for Balun (SMD, ENCLOSURE) module

## PCB requirements
In the manufacture of the device, use the material of the FR-4 printed circuit board with a thickness of 1.6 mm and copper weight equal to 1 oz (this is not the best material for RF equipment, but it is the most popular and affordable). This is necessary to comply with the wave impedance of the RF line equal to 50 Ohms. If this requirement is not observed, the wave impedance of the RF line will be different from 50 Ohms, which may make additional losses to the useful signal when the device is running. Wave resistance calculations were performed for a material with Er = 4.6 (FR-4) using [Saturn PCB Design V7.08](http://www.saturnpcb.com/pcb_toolkit/) toolkit.

## Components installing 
Due to the use of SMD components and relatively tight mounting, this module has some recommendations on the soldering order of components, this is necessary to facilitate soldering (no hard-to-reach areas for the soldering iron will be formed).

Soldering order of components:

- U1 -> D1 -> J2 -> J1

After assembly, clean the PCB to remove any flux residues and prepare an aluminum enclosure with dimensions of 50 x 50 x 25 mm for installing the PCB. Disassemble the metal case and cut holes in the side covers so that the SMA connector and terminal block pass through them freely.

Install the PCB in one of the parts of the case by placing it on the appropriate chassis. Screw the side covers of the case to the part of the case where the PCB is installed and tighten the nuts on the SMA connector, this will allow you to align and fix the PCB inside the case.

Screw the top cover of the aluminum enclosure. Now the device is ready to work.

## Installation recommendations
Connect the balanced antenna feed line (e.g. dipole, loop) to the terminal block of the balun module, and connect the SMA output to the SDR receiver using a 50 Ohm coaxial cable. Make sure to select the appropriate transformer ratio depending on the impedance of your antenna (refer to the impedance ratio table in the [module description](../README.md)).

Since the balun module may be installed outdoors in close proximity to the receiving antenna, there is a possibility that it may be forced to work in conditions of high humidity (rain, snow). In this case, before installing the module, **it is recommended to perform a preliminary sealing of all connected parts between enclosure, SMA connector and terminal block with silicone sealant**. This will prevent the ingress of water into the device and its failure.