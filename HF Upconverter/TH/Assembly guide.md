# Assembly guide for HF Upconverter (TH) module

## PCB requirements
In the manufacture of the device, use the material of the FR-4 printed circuit board with a thickness of 1.6 mm (this is not the best material for RF equipment, but it is the most popular and affordable). This is necessary to comply with the wave impedance of the RF line equal to 50 Ohms. If this requirement is not observed, the wave impedance of the RF line will be different from 50 Ohms, which may lead to incorrect operation of the device. Wave resistance calculations were performed for a material with Er = 4.6 (FR-4) using [Saturn PCB Design V7.08](http://www.saturnpcb.com/pcb_toolkit/).

## Manufacture of inductors
In the process of manufacturing this module, you will have to manufacture the inductors yourself for the used highpass / lowpass filters. Coils are made by winding an enameled copper wire of a certain diameter to a round workpiece of a certain diameter (it is convenient to use drills). Before winding the coil, clean one end of the wire from the insulation (use an aggressive solvent or insulation heating, approximately
3-5 mm.). When you start winding the coil, try to make the windings as close as possible to each other. After finishing the winding of the coil, remove the protective insulation from the other end of the coil and make tinning both ends. After doing this, your coil will be ready for installation on the PCB.

A small example of manufacturing an inductor: [Making a Simple Air Core Inductor (Induction Coil): 5 Steps]

Characteristics of coils for manufacturing:  
- **39 nH** - wire Ø0.5mm., coil Ø2.5mm., windings 4 - **3 pcs.**;  
- **330 nH** - wire Ø0.25mm., coil Ø2.5mm., windings 14 - **1 pcs.**;  
- **390 nH** - wire Ø0.25mm., coil Ø2.5mm., windings 16 - **1 pcs**;  

## Components installing 
In the beginning, it is recommended to install self-made inductors, since soldering and manufacturing of these elements can cause difficulties if you doing this for the first time. Other passive components can be mounted in any convenient order for you.  
However, it is strongly recommended that you **use an antistatic wrist strap and do not use soldering irons that are powered directly from the 220V / 110V network**, which can damage the crystal oscillator and mixer when soldering.

Recommendations for assembling components:

- Soldering self-made inductors.
- Soldering other passive components in any order.
- Soldering the diodes 1N4148 and LED.
- Soldering of the mixer.
- Soldering the crystal oscillator.
- Soldering the power connector and the switch.
- Soldering SMA connectors.

## Installation recommendations
If you use HF Upconverter, you will lose the ability to use software selectable Bias Tee (if this is offered by your SDR receiver). Therefore, if you use an active antenna (for example, Mini-Whip), you will definitely need to use a separate Power Feed Unit that is connected between the antenna and the converter.

Also, because of using of a 125 MHz value crystal oscillator, the frequency will be shifted to 125 MHz up (the frequency shift of our received radio station will look like this: 4.625 MHz + 125 MHz = 129.625 MHz). For convenience, you will need to set the value of the backward bias of -125 MHz in the receiving program (Gqrx, SDRSharp, etc.), but this action is not mandatory.

In the event of a large amount of interference at reception, you can independently manufacture a metal case for the upconverter. To do this, you can use any metal box of suitable size. The box is connected to the shield of a coaxial cable (connects to the external part of the SMA connector) or wire can be used, one end of which is soldered to the box and the other to a special "SHIELD" contact on the upconverter PCB.

## Power supply recommendations
When powering the HF Upconverter, **do not use power banks or other power supplies with impulse converters**. These devices create a sufficiently large amount of interference, which can adversely affect reception quality. When working from a laptop it is possible to use power from a free USB connector, or use a battery with a voltage of 5 V. In addition, a good solution will be the use of ferrite filters on power cables.

[Making a Simple Air Core Inductor (Induction Coil): 5 Steps]: <http://www.instructables.com/id/Making-a-Simple-Induction-Coil/>
