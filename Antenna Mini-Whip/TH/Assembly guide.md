# Assembly guide for Antenna Mini-Whip (TH) module

## Components installing 
This module does not have any specific recommendations for assembly. All passive components can be mounted in any convenient order for you.  
However, it is strongly recommended that you **use an antistatic wrist strap and do not use soldering irons that are powered directly from the 220V / 110V network**, which can damage the J310 field-effect transistor when soldering.

Recommendations for assembling components:

- Soldering all passive components in any order.
- Soldering the power connector.
- Soldering SMA connectors.
- Soldering the diode 1N5819.
- Soldering of the transistor 2N5109.
- Soldering the field effect transistor J310.

## Additional instructions
A useful step can also be to check the output voltage level with a multimeter. To prevent damage to your receiver, connect PFU to the power supply, and perform voltage measurement on the SMA connector (PFU-to-receiver connector). The value of the output voltage must be zero. After that, you can make further connections and work with the antenna.

## Installation recommendations
Immediately before installation, you can place the antenna in a plastic housing, this will additionally protect your antenna from precipitation. The installation of the antenna in the plastic housing does not interfere with the normal reception.

To install the Mini-Whip antenna, you can choose a grounded metal or dielectric mast.

**In the case of selecting a metal mast, it is necessary to place the antenna above the top of the mast, and the mast itself must have a good grounding (the cable shield is also grounded)**. Qualitative grounding is necessary for the correct operation of the antenna, since its principle is based on the principle of measuring the potential between the metal plate of the antenna itself and the ground (earthed mast), after which the transmitted signal is transmitted to the receiver.
![Metal mast installation](../Resources/Antenna%20Mini-Whip/Metal-mast-installation.png)

**In case of using a mast made of dielectric material, you also need to perform high-quality grounding of the shield of the coaxial cable used.** Since in this case the potential difference is measured between the antenna plate and the shield of the coaxial cable.
![Dielectric mast installation](../Resources/Antenna%20Mini-Whip/Dielectric-mast-installation.png)

An additional advantage will also be the location of the antenna at the highest available point of installation.