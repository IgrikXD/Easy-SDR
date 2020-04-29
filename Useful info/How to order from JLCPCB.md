# How to order from JLCPCB

## Why JLCPCB?
When developing their projects, in the case of ordering printed circuit boards I use the services of the [JLCPCB] platform. I chose this platform on the basis of the convenience of integration with the [EasyEDA] platform, low prices for orders of PCBs up to 100x100 mm., and the relatively low price of delivery to my country (I live in Belarus).

## What other companies exist to ordering PCBs?
| PCB Manufacturer | Information |
| ----- | ----- |
| [PCBWay] | International delivery. The minimum order is 5 pieces. Sponsorship of non-commercial projects. A bonus system for issuing coupons based on reviews about manufactured PCBs and inviting friends. |
| [Seeed Studio] | International delivery. The minimum order is 5 pieces. |
| [ITEAD] | International delivery. The minimum order is 5 pieces. |
| [OSH Park] | International delivery. |
| [Belplata] | Manufacturer of PCB from Belarus. Delivery by mail in Belarus, self-delivery.|
| [Nanotech] | Manufacturer of PCB from Belarus. Delivery by mail in Belarus, self-delivery. |
| [PS Electro] | The manufacturer of PCB from Russia. Delivery by mail in Russia, self-delivery. The minimum order is 1 piece.|
| [Rezonit] |  The manufacturer of PCB from Russia. Delivery by mail in Russia, self-delivery. The minimum order is 1 piece. |
| [MERKAR] | The manufacturer of PCB from Poland. Delivery method: mail, self-delivery, courier. The minimum order is 1 piece. |
| [SATLAND PROTOTYPE] | The manufacturer of PCB from Poland. Delivery method: mail, self-delivery. |
| [Margol Electronics] | The manufacturer of PCB from Poland. Delivery method: mail, self-delivery. The minimum order is 1 piece. |

## Ordering from JLCPCB
First, you need to go to the [JLCPCB] site itself.  
![Mainpage](../Resources/JLCPCB%20order/JLCPCB-1-Mainpage.png)  

Then log in to your existing account or create a new one.  
![Login reg](../Resources/JLCPCB%20order/JLCPCB-2-Login-Reg.png)  

Click the "[Calculate](https://jlcpcb.com/quote)" button to go to the PCB manufacturing order form.  
![Add gerber](../Resources/JLCPCB%20order/JLCPCB-3-Add-gerber.png)  

Click "Add you Gerber file" and select the previously generated and downloaded Gerber file ([How to export Gerber file from EasyEDA](./How%20to%20export%20Gerber%20file%20from%20EasyEDA.md)). After that, the Gerber file will automatically upload. After the automatic upload of the Gerber file, you will be able to preview your PCB using the "Gerber Viewer" (on the right from the bottom of the PCB preview), change the production parameters (amount, mask color, thickness, etc.).  
![Add result](../Resources/JLCPCB%20order/JLCPCB-4-Add-result.png)  

Setting production parameters. These parameters are set automatically and are considered optimal. If the size of the printed circuit board is up to 100x100 mm., amount of layers is not more than 2 and the green solder mask used (the other parameters are automatically generated), then the order price for up to 10 PCBs will not exceed $ 5 (excluding delivery).  
![PCB property](../Resources/JLCPCB%20order/JLCPCB-5-PCB-Property.png)  

"Gerber Viewer" topside preview  
![Gerber view top](../Resources/JLCPCB%20order/JLCPCB-6-Gerber-view-top.png)  

"Gerber Viewer" analysis result. Do not worry about the warning. Gerber_drill.GTP and Gerber_drill.GBP files are not needed to work with the JLCPCB platform, they will simply be ignored. The minimal trace spacing warning is also ignored because our circuit board has successfully passed a preliminary check for DRC errors.  
![Check result](../Resources/JLCPCB%20order/JLCPCB-7-Check-result.png)  

After checking all the parameters, we press the "SAVE TO CART" button to save the current order. At this stage, you can add several more PCBs to the order. To do this, click the "+ Add new item" button after which you will be taken to the page for adding the Gerber file, the actions for adding a new PCB are similar to those described earlier. If you added all the necessary PCBs, proceed to the next step - processing, and payment of the order. To do this, click the "Checkout securely" button.  
![Cart](../Resources/JLCPCB%20order/JLCPCB-8-Cart.png)  

At this step, add your mailing address, choose the most convenient method of delivery (at the time of 2018, if you make the first order on the JLCPCB platform the delivery is free of charge) and the preferred method of payment. After adding all the necessary data, click the "Pay" button.  
![Place order](../Resources/JLCPCB%20order/JLCPCB-9-Place-order.png)  

After payment of the order, we can look at the information on the placed order. For each PCB there will be a separate number in the order, according to which we can view the current production status.  
![Order history](../Resources/JLCPCB%20order/JLCPCB-10-Order-history.png)  

To view the production status, click the "Order Details" button for the specific PCB. For my order (HF Upconverter (SMD) + Antenna Mini-Whip (SMD)) the manufacture of PCBs was done in about 30 hours.  
![Order status](../Resources/JLCPCB%20order/JLCPCB-11-Order-status.png)  

After the end of the production, your order will be packed and sent to you. The status of your order will change to "Shipped".  
![Order shipped](../Resources/JLCPCB%20order/JLCPCB-12-Order-shipped.png)  

Other articles:  
[How to export Gerber file from EasyEDA](./How%20to%20export%20Gerber%20file%20from%20EasyEDA.md)  
[How to order from LCSC](./How%20to%20order%20from%20LCSC.md)  
[How to order from PCBWay](./How%20to%20order%20from%20PCBWay.md)  
[How to work with RTL-SDR receivers on Linux](./How%20to%20work%20with%20RTL-SDR%20receivers%20on%20Linux.md)


[JLCPCB]: <https://jlcpcb.com/>
[EasyEDA]: <https://easyeda.com/>
[PCBWay]: <https://www.pcbway.com/>
[Seeed Studio]: <https://www.seeedstudio.com/fusion_pcb.html>
[ITEAD]: <https://www.itead.cc/open-pcb/pcb-prototyping.html>
[OSH Park]: <https://oshpark.com/>
[Belplata]: <https://belplata.by/calc>
[Nanotech]: <http://www.pcb.by/index.php/clients/howto>
[PS Electro]: <http://www.pselectro.ru/zakaz_pechatnyh_plat/>
[Rezonit]: <https://service.rezonit.ru/cards/new>
[MERKAR]: <http://www.merkar.pl/cennik.html>
[SATLAND PROTOTYPE]: <http://prototypy.com/sites_pcbplugins/pcborder/58>
[Margol Electronics]: <http://www.fabrykapcb.pl/jakzamowic.html>
