# Assembly guide for LNA (SMD) module

## Components installing 
Due to the use of SMD components and relatively tight mounting, this module has some recommendations on the soldering order of components, this is necessary to facilitate soldering (no hard-to-reach areas for the soldering iron will be formed).
Also, it is strongly recommended that you **use an antistatic wrist strap and do not use soldering irons that are powered directly from the 220V / 110V network**, which can damage some sensitive components when soldering.

Soldering order of components:

- Version with RPP, TCBT-14+: U2 -> L1 -> C5 -> C4 -> C1 -> C2 -> C3 -> C6 -> LED1 -> R2 -> Q1 -> D1 -> R1 -> D2 -> U1 -> U3 -> DC1 -> SW1 -> SMA con. (Resistor **R0(DNI)** can be soldered to disable the function of protection against polarity reversal)
- Version with RPP: C(BT) -> L(BT) -> L1 -> C5 -> C4 -> C1 -> C2 -> C3 -> C6 -> LED1 -> R2 -> Q1 -> D1 -> R1 -> D2 -> U1 -> U3 -> DC1 -> SW1 -> SMA con. (Resistor **R0(DNI)** can be soldered to disable the function of protection against polarity reversal)
- Version without RPP, TCBT-14+: U2 -> L1 -> C4 -> C5 -> C1 -> C2 -> C3 -> C6 -> R2 -> LED1 -> D2 -> U1 -> U3 -> DC1 -> SW1 -> SMA con.
- Version without RPP: C(BT) -> L(BT) -> L1 -> C4 -> C5 -> C1 -> C2 -> C3 -> C6 -> R2 -> LED1 -> D2 -> U1 -> U3 -> DC1 -> SW1 -> SMA con.
- Version BT only, TCBT-14+: L1 -> C4 -> C5 -> U2 -> C6 -> D2 -> U3 -> SMA con.
- Version BT only: C5 -> C4 -> C(BT) -> L(BT) -> L1 -> C6 -> D2 -> U3 -> SMA con.
- Version simplified: C(BT) -> L(BT) -> L1 -> **R0(BT)/R0(EXT)** -> C5 -> C4 -> C1 -> C2 -> C3 -> C6 -> D2 -> U1 -> U3 -> SMA con.
- Version simplified, DC connector: C(BT) -> L(BT) -> L1 -> **R0(BT)/R0(EXT)** -> C5 -> C4 -> C1 -> C2 -> C3 -> C6 -> D2 -> U1 -> U3 -> DC1 -> SMA con.

When soldering a simplified LNA, a resistor **R0(BT/EXT)** is used, select:
**R0(BT)** - when powering LNA through Bias Tee;
**R0(EXT)** - when using an external power source with conversion via LM1117;

**Simultaneous soldering of both resistors is not allowed!**

## Additional instructions
To prevent damage to your receiver perform voltage measurement on the SMA RF OUT connector. The value of the output voltage must be around zero. After that, you can connect the cables to the receiver and the antenna and continue your work.  

**Remember that when using the version without protection against polarity reversal, you must take care of the correct polarity of the power supply**. In the case of supplying voltage with incorrect polarity, you can destroy the LM1117 voltage regulator.

## Installation recommendations
In the event of a large amount of interference at reception, you can independently manufacture a metal case for the LNA module. To do this, you can use any metal box of suitable size. The box is connected to the shield of a coaxial cable (connects to the external part of the SMA connector) or wire can be used, one end of which is soldered to the box and the other to a special "SHIELD" contact on the PCB.

## Power supply recommendations
**It is recommended to use directly connected batteries** (for example, a 18650 battery pack) to power this module and not to use any intermediate transducers, either pulsed or linear (there is simply no need, voltage stabilization is performed using an LM1117 chip).