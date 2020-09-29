# How to order from PCBWay

## Why PCBWay?
When developing this project, I also use [PCBWay] service for some objective reasons. This company currently provides a large number of multi-colored solder masks for your PCBs without increasing the final price (price for 10 printed circuit boards up to 100x100 mm. in size is $ 5), it is possible to use PCB material other than FR-4 (also available: Aluminum, Rogers, HDI, Cooper Base) and the number of layers up to 14. An undoubted plus is the possibility of international delivery (DHL, FedEx, EMS, China Post, E-Packet) and its low cost (about $ 8 when using China Post with delivery to Belarus).

## Ordering from PCBWay
First, you need to go to the [PCBWay] site itself.  
![Mainpage](../Resources/PCBWay%20order/PCBWay-1-Mainpage.png)  

Then log in to your existing account or create a new one.  
![Login reg](../Resources/PCBWay%20order/PCBWay-2-Login-Reg.png)  

Click the "[PCB Instant Quote](https://www.pcbway.com/orderonline.aspx)" button to go to the PCB manufacturing order form.  
![Add gerber](../Resources/PCBWay%20order/PCBWay-3-Add-gerber.png)  

Click "[Quick-order PCB ⇒(only 1 min)](https://www.pcbway.com/QuickOrderOnline.aspx)" and select the previously generated and downloaded Gerber file ([How to export Gerber file from EasyEDA](./How%20to%20export%20Gerber%20file%20from%20EasyEDA.md)). After that, the Gerber file will automatically upload. After the automatic upload of the Gerber file, you will be able to preview your PCB using the "Online Gerber Viewer", change the production parameters (amount, mask color, thickness, etc.). If the size of the printed circuit board is up to 100x100 mm., amount of layers is not more than 2, then the order price for up to 10 PCBs will not exceed $ 5 (excluding delivery).  
![Add result](../Resources/PCBWay%20order/PCBWay-4-Add-result.png)   

After checking all the parameters, we press the "Add to Cart" button to save the current order. At this stage, you can add several more PCBs to the order. The actions for adding a new PCB are similar to those described earlier. If you added all the necessary PCBs, proceed to the next step - processing, and payment of the order. To do this, click the "Proceed to checkout" button.  
![Cart](../Resources/PCBWay%20order/PCBWay-5-Cart.png)  

At this step, add your mailing address, choose the most convenient method of delivery and the preferred method of payment. After adding all the necessary data, click the "Confirm & Pay" button.  
![Place order](../Resources/PCBWay%20order/PCBWay-6-Place-order.png)  

After payment of the order, we can look at the information on the placed order. For each PCB there will be a separate number in the order, according to which we can view the current production status.  
![Order history](../Resources/PCBWay%20order/PCBWay-7-Order-history.png)  

To view the production status, click the "Production Tracking" button for the specific PCB.  
![Order status](../Resources/PCBWay%20order/PCBWay-8-Order-status.png)  

## Soldering-ready PCBs

Example of PCBs from PCBWay service:  
![PCBs](../Resources/PCBWay%20order/PCBWay-9-PCB-HF-Upconverter.jpg)  
![PCBs](../Resources/PCBWay%20order/PCBWay-10-PCB-Coax-power-supply.jpg)  
![PCBs](../Resources/PCBWay%20order/PCBWay-11-PCB-SPDT-Antenna-switch.jpg)  
![PCBs](../Resources/PCBWay%20order/PCBWay-12-PCB-LNA-Bias-Tee-powered-1.jpg)  
![PCBs](../Resources/PCBWay%20order/PCBWay-13-PCB-LNA-Bias-Tee-powered-2.jpg)  
![PCBs](../Resources/PCBWay%20order/PCBWay-14-PCB-LNA-Bias-Tee-powered+filtering-1.jpg)  
![PCBs](../Resources/PCBWay%20order/PCBWay-15-PCB-LNA-Bias-Tee-powered+filtering-2.jpg)  
![PCBs](../Resources/PCBWay%20order/PCBWay-16-PCB-HF-Upconverter-ready-made.jpg)  
![PCBs](../Resources/PCBWay%20order/PCBWay-17-PCB-SPDT-Antenna-switch-ready-made-1.jpg)  
![PCBs](../Resources/PCBWay%20order/PCBWay-18-PCB-SPDT-Antenna-switch-ready-made-2.jpg)  

PCBs of high enough quality, I currently have no claims on workmanship. Earlier, about a two year ago, I encountered a problem with the poor quality of the solder mask in PCBWay boards (peeling during heating), but now no problems have been found. PCBWay very often provides good discounts and supports the Open Source / Open Hardware community, which is why I decided to use PCBWay services as the main supplier of printed circuit boards for my project. 

Other articles:  
[How to export Gerber file from EasyEDA](./How%20to%20export%20Gerber%20file%20from%20EasyEDA.md)  
[How to order from JLCPCB](./How%20to%20order%20from%20JLCPCB.md)  
[How to order from LCSC](./How%20to%20order%20from%20LCSC.md)  
[How to work with RTL-SDR receivers on Linux](./How%20to%20work%20with%20SDR%20receivers%20on%20Linux.md)  


[PCBWay]: <https://www.pcbway.com/>
