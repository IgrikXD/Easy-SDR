# Assembly guide for PI Attenuator (SMD) module

## Components installing 
Due to the use of SMD components and relatively tight mounting, this module has some recommendations on the soldering order of components, this is necessary to facilitate soldering (no hard-to-reach areas for the soldering iron will be formed).

Soldering order of components:

- Rz -> Rx -> Ry -> SMA con.

## Installation recommendations
Connect the attenuator between the antenna and the SDR receiver. Or, in the case of using a upconverter - between the antenna and the upconverter, this solution will also avoid overloading the upconverter's input.

If you use PI Attenuator, you will lose the ability to use software selectable Bias Tee (if this is offered by your SDR receiver). Therefore, **if you use an active antenna (for example, Mini-Whip), you will definitely need to use a separate Power Feed Unit that is connected between the antenna and the PI Attenuator.**

In the event of a large number of interference at reception, you can independently manufacture a metal case for the attenuator. To do this, you can use any metal box of suitable size. The box is connected to the shield of a coaxial cable (connects to the external part of the SMA connector) or wire can be used, one end of which is soldered to the box and the other to a special "SHIELD" contact on the attenuator board.