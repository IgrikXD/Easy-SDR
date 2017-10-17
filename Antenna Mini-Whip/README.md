# Project for easy and quick build active pa0rdt Mini-Whip antenna.

Project include schematic and PCB (EasyEDA, Sprint layout). Based on the submitted files, you can independently manufacture a PCB or order its production at the factory. The project was based on the idea of an active receiving antenna pa0rdt Mini-Whip. The antenna consists of the antenna itself and power feed unit. In turn, I developed PCB for the independently manufacturing based on the existing circuit. As a result, the self-made manufacture of the antenna is cheaper than buying a ready-made module.

- Original schematic: [PA0RDT Mini Whip];
- Example of working an SDR receiver on antenna Mini-Whip: [Wide-band WebSDR in Enschede, the Netherlands];

## Basic characteristics of the antenna:

- **Frequency range:** 10 kHz - 30 MHz;
- **Power:** DC 12 - 15 V, 50 mA;
- **Second order output intercept point:** > + 70 dBm;
- **Third order output intercept point:** > + 30 dBm;
- **Maximum output power:** in excess of – 15 dBm;
- **RF connector:** SMA;
- **Feed line:** 50 - 100 Ohm coaxial cable;
Do not forget about the impedance matching with the receiver.

## For the manufacture of the device you will need to purchase the following components

### Capacitors:
* [100 nF, nonpolar](https://www.ebay.com/sch/i.html?_from=R40&_trksid=p2050601.m570.l1313.TR10.TRC2.A0.H0.X100nf.TRS2&_nkw=100nf&_sacat=0) - **4 pcs.**
### Connectors:
* [SMA Female](https://www.ebay.com/sch/i.html?_from=R40&_sacat=0&_nkw=sma+female&_blrs=spell_check) - **3 pcs.**
* [SMA Male](https://www.ebay.com/sch/i.html?_from=R40&_trksid=p2050601.m570.l1313.TR0.TRC0.A0.H0.Xsma+male.TRS5&_nkw=sma+male&_sacat=0) - **4 pcs.**
* [DC-003](https://www.ebay.com/sch/i.html?_from=R40&_trksid=p2050601.m570.l1313.TR0.TRC0.H0.Xdc-003.TRS0&_nkw=dc-003&_sacat=0)/[DC-005](https://www.ebay.com/sch/i.html?_from=R40&_trksid=p2050601.m570.l1313.TR10.TRC2.A0.H0.Xdc-005.TRS2&_nkw=dc-005&_sacat=0)/[KF301-5.0-3P](https://www.ebay.com/sch/i.html?_from=R40&_trksid=p2050601.m570.l1313.TR1.TRC0.A0.H0.XKF301-3P.TRS0&_nkw=KF301-3P&_sacat=0) - **1 pcs.** The choice of a connector depends on the selection of the PFU module from the Sprint Layout file.
### Fuse:
* [Self repaiting fuse 100mA](https://www.ebay.com/sch/i.html?_from=R40&_trksid=p2050601.m570.l1313.TR0.TRC0.A0.H0.Xmf-r+100mA.TRS5&_nkw=mf-r+100mA&_sacat=0) - **1 pcs.** Not necessarily, it can be replaced by a jumper.
### Diodes:
* [Schottky 1A](https://www.ebay.com/sch/i.html?_from=R40&_trksid=p2050601.m570.l1313.TR0.TRC0.H0.XSchottky+1A.TRS0&_nkw=Schottky+1A&_sacat=0) - **1 pcs.**
### Inductors:
* [470 uH](https://www.ebay.com/sch/i.html?_from=R40&_trksid=p2050601.m570.l1313.TR0.TRC0.H0.X470uh.TRS0&_nkw=470uh&_sacat=0) - **2 pcs.**
### Resistors:
* [47R, 0.125](https://www.ebay.com/sch/i.html?_from=R40&_trksid=p2050601.m570.l1313.TR1.TRC0.A0.H0.X47ohm.TRS0&_nkw=47ohm&_sacat=0) - **1 pcs.**
* [220R, 0.125W](https://www.ebay.com/sch/i.html?_from=R40&_trksid=p2050601.m570.l1313.TR3.TRC1.A0.H0.X220ohm.TRS0&_nkw=220ohm&_sacat=0) - **1 pcs.**
* [680R, 0.125W](https://www.ebay.com/sch/i.html?_from=R40&_trksid=p2050601.m570.l1313.TR1.TRC0.A0.H0.X680ohm.TRS0&_nkw=680ohm&_sacat=0) - **1 pcs.**
* [2K2, 0.125W](https://www.ebay.com/sch/i.html?_from=R40&_trksid=p2050601.m570.l1313.TR0.TRC0.A0.H0.X2.2k+ohm.TRS5&_nkw=2.2k+ohm&_sacat=0) - **1 pcs.**
* [10K, 0.125W](https://www.ebay.com/sch/i.html?_from=R40&_trksid=p2050601.m570.l1313.TR11.TRC1.A0.H0.X10k+ohm.TRS0&_nkw=10k+ohm&_sacat=0) - **1 pcs.**
* [1M, 0.125W](https://www.ebay.com/sch/i.html?_from=R40&_trksid=p2050601.m570.l1313.TR2.TRC0.A0.H0.X1m+ohm.TRS0&_nkw=1m+ohm&_sacat=0) - **3 pcs.**
### Transistors:
* [BJT: 2N5109](https://www.ebay.com/sch/i.html?_from=R40&_trksid=p2050601.m570.l1313.TR11.TRC2.A0.H0.X2n5109.TRS1&_nkw=2n5109&_sacat=0) - **1 pcs.**
* [FET: J310](https://www.ebay.com/sch/i.html?_from=R40&_trksid=p2050601.m570.l1313.TR12.TRC2.A0.H0.Xj310.TRS0&_nkw=j310&_sacat=0) - **1 pcs.**
### Coaxial cable:
* [RG-58](https://www.ebay.com/sch/i.html?_from=R40&_trksid=p2050601.m570.l1313.TR11.TRC2.A0.H0.Xrg58.TRS1&_nkw=rg58&_sacat=0)/[RG-213](https://www.ebay.com/sch/i.html?_from=R40&_trksid=p2050601.m570.l1313.TR9.TRC1.A0.H0.Xrg213.TRS0&_nkw=rg213&_sacat=0) - 6 meters. Or some other coaxial cable with wave impedance - 50 Ohm. You can choose any other convenient length.
### Copper Clad Boards (it is not necessary if you ordering finished PCB):
* [100x33 mm.](https://www.ebay.com/sch/i.html?_from=R40&_trksid=p2050601.m570.l1313.TR0.TRC0.H0.XCopper+Clad.TRS0&_nkw=Copper+Clad&_sacat=0) - Antenna module.
* [45x33 mm.](https://www.ebay.com/sch/i.html?_from=R40&_trksid=p2050601.m570.l1313.TR0.TRC0.H0.XCopper+Clad.TRS0&_nkw=Copper+Clad&_sacat=0) - Power Feed Unit.

[How to import EasyEDA .json files] into your project;

PCB's can be ordered from the following links:

| PCB Manufacturer | Information |
| ----- | ----- |
| [JLCPCB] | International shipping. The minimum order is 5 pieces.|
| [Seeed Studio] | International shipping. The minimum order is 5 pieces.|
| [ITEAD] | International shipping. The minimum order is 5 pieces.|
| [OSH Park] | International shipping. |
| [Belplata] | Manufacturer of PCB from Belarus. Delivery by mail in Belarus, self-delivery.|
| [Nanotech] | Manufacturer of PCB from Belarus. Delivery by mail in Belarus, self-delivery. |
| [PS Electro] | The manufacturer of PCB from Russia. Delivery by mail in Russia, self-delivery. The minimum order is 1 pieces.|
| [Rezonit] |  The manufacturer of PCB from Russia. Delivery by mail in Russia, self-delivery. The minimum order is 1 pieces. |
| [MERKAR] | The manufacturer of PCB from Poland. Delivery method: mail, self-delivery, courier. The minimum order is 1 pieces. |
| [SATLAND PROTOTYPE] | The manufacturer of PCB from Poland. Delivery method: mail, self-delivery. |
| [Margol Electronics] | The manufacturer of PCB from Poland. Delivery method: mail, self-delivery. The minimum order is 1 pieces. |



[PA0RDT Mini Whip]: <http://dl1dbc.net/SAQ/miniwhip.html>
[How to import EasyEDA .json files]: <https://easyeda.com/dillon/Backup_Your_EasyEDA_Project_Locally-JrecamWv5>
[JLCPCB]: <https://jlcpcb.com/quote>
[Seeed Studio]: <https://www.seeedstudio.com/fusion_pcb.html>
[ITEAD]: <https://www.itead.cc/open-pcb.html>
[OSH Park]: <https://oshpark.com/uploads/new>
[Belplata]: <http://www.belplata.by/on-line-order>
[PS Electro]: <http://www.pselectro.ru/zakaz_pechatnyh_plat/>
[Rezonit]: <http://www.rezonit.ru/service/calc/>
[Nanotech]: <http://www.pcb.by/index.php/clients/orderform>
[MERKAR]: <http://www.merkar.pl/cennik.html>
[SATLAND PROTOTYPE]: <http://prototypy.com/t/51,Plytki_PCB>
[Margol Electronics]: <http://www.fabrykapcb.pl/jakzamowic.html>
[Wide-band WebSDR in Enschede, the Netherlands]: <http://websdr.ewi.utwente.nl:8901/>