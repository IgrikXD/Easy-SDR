# Assembly guide for LNA, Bias Tee powered + filtering (SMD, ENCLOSURE) module

## PCB requirements
In the manufacture of the device, use the material of the FR-4 printed circuit board with a thickness of 1.6 mm and copper weight equal to 1 oz (this is not the best material for RF equipment, but it is the most popular and affordable). This is necessary to comply with the wave impedance of the RF line equal to 50 Ohms. If this requirement is not observed, the wave impedance of the RF line will be different from 50 Ohms, which may make additional losses to the useful signal when the device is running. Wave resistance calculations were performed for a material with Er = 4.6 (FR-4) using [Saturn PCB Design V7.08](http://www.saturnpcb.com/pcb_toolkit/) toolkit.

## Components installing 
Due to the use of SMD components and relatively tight mounting, this module has some recommendations on the soldering order of components, this is necessary to facilitate soldering (no hard-to-reach areas for the soldering iron will be formed).
Also, it is strongly recommended that you **use an antistatic wrist strap and do not use soldering irons that are powered directly from the 220V / 110V network**, this can damage some sensitive components when soldering.

### Assembling sequence:

**LNA, Bias Tee powered + filtering (SMD, ENCLOSURE): Main module:** C1 -> D1 -> U2 -> U1.

At this stage, it is necessary to prepare an aluminum enclosure with dimensions of 50 x 25 x 25 mm for installing the PCB of the finished amplifier. Disassemble the metal case, discard the side covers - they are no longer needed, in their place will be performed installation of coaxial N-Type connectors.

![Disassembled enclosure](../../Resources/LNA/Bias%20Tee%20powered/Disassembled-enclosure.png)  

Take the two N-Type coaxial connectors and screw them onto one of the body parts using 2 screws on each side.

![N-Type mounting](../../Resources/LNA/Bias%20Tee%20powered/N-Type-mounting.png)  

The next step is to solder the PCB to the installed connectors in the aluminum enclosure. To do this, you can take advantage of small pieces of wire or paper that fit under the PCB and pushing it to the pins of the N-Type connectors. After the PCB is fixed and correctly placed, solder the necessary connections.  

![PCB mounting](../../Resources/LNA/Bias%20Tee%20powered/PCB-mounting.png)  

After the PCB has been soldered to the pins of the N-Type coaxial connector, remove the piece of paper or wire that was used to support the PCB and screw the top cover of the device.

![Top cover mounting](../../Resources/LNA/Bias%20Tee%20powered/Top-cover-mounting.png)  

Now you need to unscrew the bottom cover and solder the PCB on the other side. You do not need to worry that the PCB will fall out of the case - it is held by a soldered connection to the N-Type connectors, which in turn remain screwed to another part of the enclosure.

![Bottom side soldering](../../Resources/LNA/Bias%20Tee%20powered/Bottom-side-soldering.png)  

After soldering the bottom side of the PCB, screw the bottom cover of the device back on. Now your device is assembled and ready to go.

![Ready-made device](../../Resources/LNA/Bias%20Tee%20powered/Enclosure-Ready-made-device.png)  

## Installation recommendations
Since it is recommended that the LNA be located in close proximity to the receiving antenna, there is a possibility that you may encounter a problem when the LNA will be forced to work in conditions of high humidity (rain, snow). In this case, before installing the LNA, **it is recommended to perform a preliminary sealing of all connected parts between enclosure and N-Type connectors with silicone sealant**. This will prevent the ingress of water into the device and its failure.

## Power supply recommendations
When powering the LNA using the "Bias Tee" function in your SDR receiver, you must carefully monitor the maximum current consumption of the LNA. **Before applying power to the LNA, make sure that your SDR receiver is capable of providing at least 15% higher maximum current than that required by the amplifier**. Otherwise, your receiver's Bias Tee unit may be damaged and require replacement.
