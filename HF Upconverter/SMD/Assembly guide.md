# Assembly guide for HF Upconverter (SMD, ENCLOSURE) module

## PCB requirements
In the manufacture of the device, use the material of the FR-4 printed circuit board with a thickness of 1.6 mm and copper weight equal to 1 oz (this is not the best material for RF equipment, but it is the most popular and affordable). This is necessary to comply with the wave impedance of the RF line equal to 50 Ohms. If this requirement is not observed, the wave impedance of the RF line will be different from 50 Ohms, which may make additional losses to the useful signal when the device is running. Wave resistance calculations were performed for a material with Er = 4.6 (FR-4) using [Saturn PCB Design V7.08](http://www.saturnpcb.com/pcb_toolkit/) toolkit.

## Components installing 
Due to the use of SMD components and relatively tight mounting, this module has some recommendations on the soldering order of components, this is necessary to facilitate soldering (no hard-to-reach areas for the soldering iron will be formed).
Also, it is strongly recommended that you **use an antistatic wrist strap and do not use soldering irons that are powered directly from the 220V / 110V network**, this can damage some sensitive components when soldering.

### Assembling sequence:

**HF Upconverter (SMD, ENCLOSURE): Main module:** R1 -> F1 -> R8 -> C27 -> L1 -> R2 -> LED1 -> U1 -> U2 -> C2 -> C1 -> C3 -> C5 -> C4 -> U3 -> R3 (required if the OE or ST function is used by a crystal oscillator) -> C6 -> C7 -> U4 -> R4 -> R5 -> C9 -> L3 -> R6 -> R7 -> C8 -> L2 -> C10 -> C11 -> D1 -> L4 -> C13 -> C15 -> L5 -> C12 -> C14 -> C16 -> L6 -> C17 -> C18 -> C20 -> L8 -> C26 -> C19 -> L7 -> C23 -> L11 -> L10 -> C22 -> C24 -> L12 -> C21 -> L9 -> C25 -> L13 -> MX1.  

Take a small piece of shrink tubing, with a diameter that allows you to put it on the outer side of the USB-B connector. Put the shrink tube on the USB-B connector and briefly heat the shrink tube to compress it to the outer side of the USB-B connector. **This solution allows you to isolate the external part of the USB-B connector and the USB cable braid from the GND polygon on the PCB.**  

**Soldering sequence:** USB1 -> SMA con.  

![USB-B heat shrink tube](../../Resources/HF%20Upconverter/Enclosure-USB-B-heat-shrink.png)  

The next step is to prepare an aluminum enclosure, with dimensions of 80 x 50 x 20mm, for setting up PCB inside. Cut holes in the side covers of the case so that the USB-B and SMA connectors pass through them freely.

![Cutting holes in side covers](../../Resources/HF%20Upconverter/Enclosure-Cutting-holes-in-side-covers.png)  

Install the PCB in one of the parts of the case by placing it on the appropriate chassis. Screw the side covers of the case to the part of the case where the PCB is installed, **so you will fix the PCB and can mark the places for the hole cutting for the toggle switch SW1 and LED1**. Take the SW1 toggle switch and place it in the mounting place on the PCB. **The place where the toggle switch touches the side face of the enclosure is the point where milling is necessary in order for the toggle switch to be placed and soldered to the PCB.**

![Toggle switch installation](../../Resources/HF%20Upconverter/Enclosure-Toggle-switch-installation.png)  

Mark the same point on the top of the aluminum housing cover. 

![Toggle switch installation, top cover](../../Resources/HF%20Upconverter/Enclosure-Toggle-switch-installation-top-cover.png)  

Unscrew the side covers of the case, remove the PCB and use a drill to mill the hole for SW1 toggle switch to the desired depth. Also, drill a hole for the LED1. After milling, re-insert the PCB into the appropriate chassis and check how freely the toggle switch fits into the milled hole. If you can't set the toggle switch, repeat the above steps to achieve optimal results.  

![Milled hole for toggle switch](../../Resources/HF%20Upconverter/Enclosure-Milled-hole-for-toggle-switch.png) 

The next step, again take a small piece of shrink tube, the diameter of which allows you to put it on the outer, round part of the toggle switch SW1. Heat the shrink tube to compress it to the outer, round part of the switch SW1. **This solution allow isolate SW1 toggle switch from the aluminum enclosure of the device.**  

![Toggle switch heat shrink tube](../../Resources/HF%20Upconverter/Enclosure-Toggle-switch-heat-shrink.png)  

Insert the PCB back into the chassis, screw the side covers aluminum enclosure, tighten the nuts on the SMA connector, this will allow you to align and fix the PCB inside the case. After the above operations, solder the SW1 toggle switch after installing it in mounting place on PCB.  

**Soldering sequence:** SW1.  

![Soldering the toggle switch](../../Resources/HF%20Upconverter/Enclosure-Soldering-the-toggle-switch.png)  

Screw the top cover of the aluminum enclosure. Now the device is ready to work.

![Ready-made device](../../Resources/HF%20Upconverter/Enclosure-Ready-made-device.png)  

## Installation recommendations
If you use HF Upconverter, you will lose the ability to use software selectable Bias Tee (if this is offered by your SDR receiver). Therefore, if you use an active antenna (for example, Mini-Whip), you will definitely need to use a separate Power Feed Unit that is connected between the antenna and the converter.

Also, because of using of a 125 MHz value crystal oscillator, the frequency will be shifted to 125 MHz up (the frequency shift of our received radio station will look like this: 4.625 MHz + 125 MHz = 129.625 MHz). For convenience, you will need to set the value of the backward bias of -125 MHz in the receiving program (Gqrx, SDRSharp, etc.), but this action is not mandatory.

## Power supply recommendations
When powering the HF Upconverter, **do not use power banks or other power supplies with impulse converters**. These devices create a sufficiently large amount of interference, which can adversely affect reception quality. When working from a laptop it is possible to use power from a free USB connector, or use a battery with a voltage of 5 V. In addition, a good solution will be the use of ferrite filters on power cables.
