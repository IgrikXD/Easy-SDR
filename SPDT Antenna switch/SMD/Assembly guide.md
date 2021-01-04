# Assembly guide for SPDT Antenna switch (SMD, ENCLOSURE) module

## PCB requirements
In the manufacture of the device, use the material of the FR-4 printed circuit board with a thickness of 1.6 mm and copper weight equal to 1 oz (this is not the best material for RF equipment, but it is the most popular and affordable). This is necessary to comply with the wave impedance of the RF line equal to 50 Ohms. If this requirement is not observed, the wave impedance of the RF line will be different from 50 Ohms, which may make additional losses to the useful signal when the device is running. Wave resistance calculations were performed for a material with Er = 4.6 (FR-4) using [Saturn PCB Design V7.08](http://www.saturnpcb.com/pcb_toolkit/) toolkit.

## Components installing 
Due to the use of SMD components and relatively tight mounting, this module has some recommendations on the soldering order of components, this is necessary to facilitate soldering (no hard-to-reach areas for the soldering iron will be formed).
Also, it is strongly recommended that you **use an antistatic wrist strap and do not use soldering irons that are powered directly from the 220V / 110V network**, this can damage some sensitive components when soldering.

### Assembling sequence:

**SPDT Antenna switch (SMD, ENCLOSURE): Main module:** R1 -> F1 -> R4 -> C13 -> L1 -> C2 -> R3 -> LED1 -> U1 -> C1 -> C3 -> U2 -> R2 -> C4 -> C5 -> C6 -> C7 -> U3 -> C8 -> C9 -> C10 -> C11 -> D1 -> D2 -> C12.

> **Optional**  
> Take a small piece of shrink tubing, with a diameter that allows you to put it on the outer side of the USB-B connector. Put the shrink tube on the USB-B connector and briefly heat the shrink tube to compress it to the outer side of the USB-B connector. **This solution allows you to isolate the external part of the USB-B connector and the USB cable braid from the GND polygon on the PCB.**  

**Soldering sequence:** USB1 -> SMA con.  

The next step is to prepare an aluminum enclosure, with dimensions of 80 x 50 x 20mm, for setting up PCB inside. Cut holes in the side covers of the case so that the USB-B and SMA connectors pass through them freely.
> I do not give specific recommendations for preparing a metal case for a finished device, since there are many ways to manufacture it, both at home and using industrial equipment (laser cutting, CNC milling machine). I will only provide [AutoCAD](./Enclosure%20model%20files/) drawings for the manufacture of side covers in any way convenient for you. For self-production of cases, I use a drill with metal cutters and the necessary drills. I carry out the transfer of the drawing from AutoCAD to the covers of the metal case 80 x 50 x 20 mm, after which I perform the necessary processing using a drill and file files.

![Cutting holes in side covers](../../Resources/SPDT%20Antenna%20switch/Enclosure-Cutting-holes-in-side-covers.jpg)  

Install the PCB in one of the parts of the case by placing it on the appropriate chassis. Screw the side covers of the case to the part of the case where the PCB is installed and tighten the nuts on the SMA connector, **so you will fix the PCB and can mark the places for the hole cutting for the toggle switches SW1, SW2 and LED1**. Take the SW1 toggle switch and place it in the mounting place on the PCB. **The place where the toggle switch touches the side face of the enclosure is the point where milling is necessary in order for the toggle switch to be placed and soldered to the PCB.** Perform the same operation with the toggle switch SW2.

![Toggle switch installation](../../Resources/SPDT%20Antenna%20switch/Enclosure-Toggle-switch-installation.jpg)  

Mark the same point on the top of the aluminum housing cover. 

![Toggle switch installation, top cover](../../Resources/SPDT%20Antenna%20switch/Enclosure-Toggle-switch-installation-top-cover.jpg)  

Unscrew the side covers of the case, remove the PCB and use a drill to mill the holes for SW1 and SW2 toggle switches to the desired depth. Also, drill a hole for the LED1. After milling, re-insert the PCB into the appropriate chassis and check how freely the toggle switch fits into the milled hole. If you can't set the toggle switch, repeat the above steps to achieve optimal results.  

![Milled hole for toggle switch](../../Resources/SPDT%20Antenna%20switch/Enclosure-Milled-hole-for-toggle-switch.jpg) 

> **Optional** 
> The next step, again take a small piece of shrink tube, the diameter of which allows you to put it on the outer, round part of the toggle switch SW1 and SW2. Heat the shrink tube to compress it to the outer, round part of the switches. **This solution allow isolate toggle switches from the aluminum enclosure of the device.**   

Insert the PCB back into the chassis, screw the side covers aluminum enclosure, tighten the nuts on the SMA connector, this will allow you to align and fix the PCB inside the case. After the above operations, solder the SW1 and SW2 toggle switches after installing it in mounting place on PCB.  

**Soldering sequence:** SW1 -> SW2.  

![Soldering the toggle switch](../../Resources/SPDT%20Antenna%20switch/Enclosure-Soldering-the-toggle-switch.jpg)  

After soldering clean the PCB to remove any flux residues.

![Cleaning the PCB](../../Resources/HF%20Upconverter/Cleaning-the-PCB.jpg)

Screw the top cover of the aluminum enclosure. Now the device is ready to work.

![Ready-made device](../../Resources/SPDT%20Antenna%20switch/Enclosure-Ready-made-device.jpg)  

## Installation recommendations
If you use SPDT Antenna switch module, you will lose the ability to use software selectable Bias Tee (if this is offered by your SDR receiver). Therefore, **if you use an active antenna (for example, [Mini-Whip](https://easyeda.com/IgrikXD/Antenna_Mini_Whip_SMD-74e9e6740b814f6c901a811855125754)) or [Bias Tee powered LNA](https://easyeda.com/IgrikXD/bias-tee-lna-smd-enclosure), you will definitely need to use a separate Power Feed Unit that is connected between the antenna and the antenna switch.**

## Power supply recommendations
When powering the SPDT Antenna switch module, **do not use power banks or other power supplies with impulse converters**. These devices create a sufficiently large amount of interference, which can adversely affect reception quality. When working from a laptop it is possible to use power from a free USB connector, or use a battery with a voltage of 5 V. In addition, a good solution will be the use of ferrite filters on power cables.
