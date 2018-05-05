# Assembly guide for HF Upconverter (SMD) module

## Components installing 
Due to the use of SMD components and relatively tight mounting, this module has some recommendations on the order of soldering components, this is necessary to facilitate soldering (no hard-to-reach areas for the soldering iron will be formed).
Also, it is strongly recommended that you **use an antistatic wrist strap and do not use soldering irons that are powered directly from the 220V / 110V network**, which can damage the some sensitive components when soldering.

Soldering order of components:

- TPS version: C14 -> L4 -> C16 -> L5 -> C18 -> L6 -> C13 -> C15 -> C17 -> C19 -> C21 -> L8 -> C23 -> L10 -> C25 -> L12 -> C20 -> L7 -> C22 -> L9 -> C24 -> L11 -> C26 -> L13 -> C27 -> R13 -> R14 -> C4 -> C6 -> DNI(R7) -> DNI(R6) -> C7 -> C8 -> C9 -> R10 -> R11 -> R12 -> L2 -> C11 -> L1 -> MX1 -> DNI(L3) -> DNI(C12) -> U2 -> C5 -> BLUE LED -> R5 -> RED LED -> R8 -> GREEN LED -> R9 -> D3 -> SW1 -> U3 -> C10 -> USB1 -> SMA con.

For building this version, you will need a multimeter for measurements the output voltage of the LM317. If you do not have a multimeter, you can use the SMD resistor R3(OR), 480 Ohm **instead** resistor R3.  

- TPS + LM version: C14 -> L4 -> C16 -> L5 -> C18 -> L6 -> C13 -> C15 -> C17 -> C19 -> C21 -> L8 -> C23 -> L10 -> C25 -> L12 -> C20 -> L7 -> C22 -> L9 -> C24 -> L11 -> C26 -> L13 -> C27 -> R13 -> R5 -> R14 -> C4 -> C6 -> DNI(R7) -> C7 -> C2 -> R2 -> C1 -> R1 -> C3 -> C8 -> R11 -> R12 -> L2 -> C11 -> L1 -> C10 -> MX1 -> DNI(L3) -> DNI(C12) -> U2 -> C5 -> DNI(R6) -> BLUE LED -> YELLOW LED -> R4 -> RED LED -> R8 -> GREEN LED -> R9 -> D2 -> Q1 -> D1 -> Q2 -> U1 -> D3 -> R3/R3(OR) -> DC1 -> USB1 -> (**Only when using resistor R3**. Connect the power to the DC connector, measure the voltage between the middle switch contact (SW1) and GND. **The value obtained should be between 3.25-3.35 V**. If the voltage does not correspond within the specified range - adjust voltage using resistor R3.) -> SW1 -> U3 -> C9 -> R10 -> SMA con. 

## Installation recommendations
If you use HF Upconverter, you will lose the ability to use software selectable Bias Tee (if this is offered by your SDR receiver). Therefore, if you use an active antenna (for example, Mini-Whip), you will definitely need to use a separate Power Feed Unit that is connected between the antenna and the converter.

Also, because of using of a 125 MHz value crystal oscillator, the frequency will be shifted to 125 MHz up (the frequency shift of our received radio station will look like this: 4.625 MHz + 125 MHz = 129.625 MHz). For convenience, you will need to set the value of the backward bias of -125 MHz in the receiving program (Gqrx, SDRSharp, etc.), but this action is not mandatory.

In the event of a large number of interference at reception, you can independently manufacture a metal case for the upconverter. To do this, you can use any metal box of suitable size. The box is connected to the shield of a coaxial cable (connects to the external part of the SMA connector) or wire can be used, one end of which is soldered to the box and the other to a special "SHIELD" contact on the converter board.

## Power supply recommendations
When powering the HF Upconverter, **do not use power banks or other power supplies with impulse converters**. These devices create a sufficiently large amount of interference, which can adversely affect the reception quality. When working from a laptop it is possible to use power from a free USB connector, or use a battery with a voltage of 5 V (or 7 - 20 V, LM317 version). In addition, a good solution will be the use of ferrite filters on power cables.