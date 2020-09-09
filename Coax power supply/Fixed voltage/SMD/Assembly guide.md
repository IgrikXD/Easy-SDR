# Assembly guide for Coax power supply, fixed voltage (SMD, ENCLOSURE) module

## PCB requirements
In the manufacture of the device, use the material of the FR-4 printed circuit board with a thickness of 1.6 mm and copper weight equal to 1 oz (this is not the best material for RF equipment, but it is the most popular and affordable). This is necessary to comply with the wave impedance of the RF line equal to 50 Ohms. If this requirement is not observed, the wave impedance of the RF line will be different from 50 Ohms, which may make additional losses to the useful signal when the device is running. Wave resistance calculations were performed for a material with Er = 4.6 (FR-4) using [Saturn PCB Design V7.08](http://www.saturnpcb.com/pcb_toolkit/) toolkit.

## Components installing 
Due to the use of SMD components and relatively tight mounting, this module has some recommendations on the soldering order of components, this is necessary to facilitate soldering (no hard-to-reach areas for the soldering iron will be formed).
Also, it is strongly recommended that you **use an antistatic wrist strap and do not use soldering irons that are powered directly from the 220V / 110V network**, this can damage some sensitive components when soldering.

### Assembling sequence:

**Coax power supply, fixed voltage (SMD, ENCLOSURE): Main module (TCBT-14+):** R1 -> F1 -> R3 -> C5 -> L1 -> U1 -> C1 -> C2 -> U2 -> C3 -> C4 -> R2 -> LED1.  
**Coax power supply, fixed voltage (SMD, ENCLOSURE): Main module:** R1 -> F1 -> R3 -> C5 -> L1 -> U1 -> C1 -> C2 -> C(BT) -> L(BT) -> C3 -> C4 -> R2 -> LED1.  

Take a small piece of shrink tubing, with a diameter that allows you to put it on the outer side of the USB-B connector. Put the shrink tube on the USB-B connector and briefly heat the shrink tube to compress it to the outer side of the USB-B connector. **This solution allows you to isolate the external part of the USB-B connector and the USB cable braid from the GND polygon on the PCB.**  

**Soldering sequence:** USB1 -> SMA con.  

![USB-B heat shrink tube](../../Resources/Coax%20power%20supply/Enclosure-USB-B-heat-shrink.png)  

The next step is to prepare an aluminum enclosure, with dimensions of 80 x 50 x 20mm, for setting up PCB inside. Cut holes in the side covers of the case so that the USB-B and SMA connectors pass through them freely.

![Cutting holes in side covers](../../Resources/Coax%20power%20supply/Enclosure-Cutting-holes-in-side-covers.png)  

Install the PCB in one of the parts of the case by placing it on the appropriate chassis. Screw the side covers of the case to the part of the case where the PCB is installed, **so you will fix the PCB and can mark the places for the hole cutting for the toggle switch SW1 and LED1**. Take the SW1 toggle switch and place it in the mounting place on the PCB. **The place where the toggle switch touches the side face of the enclosure is the point where milling is necessary in order for the toggle switch to be placed and soldered to the PCB.**

![Toggle switch installation](../../Resources/Coax%20power%20supply/Enclosure-Toggle-switch-installation.png)  

Mark the same point on the top of the aluminum housing cover. 

![Toggle switch installation, top cover](../../Resources/Coax%20power%20supply/Enclosure-Toggle-switch-installation-top-cover.png)  

Unscrew the side covers of the case, remove the PCB and use a drill to mill the hole for SW1 toggle switch to the desired depth. Also, drill a hole for the LED1. After milling, re-insert the PCB into the appropriate chassis and check how freely the toggle switch fits into the milled hole. If you can't set the toggle switch, repeat the above steps to achieve optimal results.  

![Milled hole for toggle switch](../../Resources/Coax%20power%20supply/Enclosure-Milled-hole-for-toggle-switch.png) 

The next step, again take a small piece of shrink tube, the diameter of which allows you to put it on the outer, round part of the toggle switch SW1. Heat the shrink tube to compress it to the outer, round part of the switch SW1. **This solution allow isolate SW1 toggle switch from the aluminum enclosure of the device.**  

![Toggle switch heat shrink tube](../../Resources/Coax%20power%20supply/Enclosure-Toggle-switch-heat-shrink.png)  

Insert the PCB back into the chassis, screw the side covers aluminum enclosure, tighten the nuts on the SMA connector, this will allow you to align and fix the PCB inside the case. After the above operations, solder the SW1 toggle switch after installing it in mounting place on PCB.  

**Soldering sequence:** SW1.  

![Soldering the toggle switch](../../Resources/Coax%20power%20supply/Enclosure-Soldering-the-toggle-switch.png)  

Screw the top cover of the aluminum enclosure. Now the device is ready to work.

![Ready-made device](../../Resources/Coax%20power%20supply/Enclosure-Ready-made-device.png)  

## Additional instructions
If you want to use an output voltage other than +3.3 V, you can replace the LP5907MFX-3.3 linear voltage regulator with any other linear regulators in the SOT-23-5 case, with the same pinout and capable of operating at +5 V (standard USB port voltage).

To prevent damage to your receiver perform voltage measurement on the SMA RF OUT connector. The value of the output voltage must be equal to zero. After that, you can connect the cables to the receiver and continue your work.  
