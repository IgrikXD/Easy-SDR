# How to order from LCSC

## Why LCSC?
The main reason for choosing [LCSC] was that this distributor is connected with the service of PCBs developing [EasyEDA]. This allows us, when correctly describing the BOM file, to place the order of all necessary components in just a few simple steps. Supporting worldwide shipping. All components come in individual anti-static packaging with a protection against damage (cardboard box + bubble wrap).  
However, you may not find all the necessary components for the assembly, in this case I'm using [Ebay]. To make it easier to find the necessary components for the assembly of the module, you can find the corresponding file with a list of all the necessary components with links to [LCSC] and [Ebay], and also, with references to datasheets on the following path:  
**Easy-SDR repository / Module name / Component group / Components list**.

## Ordering from LCSC
First, go to the page of the module you are interested in on the EasyEDA website.  
![Module page](../Resources/LCSC%20order/LCSC-1-Module-page.png)  

Press the "BOM" button and go up a little higher, click the "Open in Editor" button. At this step you can view the contents of the BOM file, but you can not do anything.  
![BOM select](../Resources/LCSC%20order/LCSC-2-BOM-select.png)  

Click this button, whereby you will be taken to the EasyEDA editor.  
![Editor](../Resources/LCSC%20order/LCSC-3-Editor.png)  

Now we can make exporting the BOM file or use "One-click Purchasing at LCSC". To do this, you need to on the right, in the top panel of the editor, click the "Export BOM" button.  
![BOM export](../Resources/LCSC%20order/LCSC-4-BOM-export.png)  

Next, small window appearing where you can see a BOM list details for choosen module. At this step, you can either just **save the BOM file, by pushing "Export BOM" button**, or making **"One-click Purchasing at LCSC"** with push corresponding button.  
![BOM preview](../Resources/LCSC%20order/LCSC-5-BOM-preview.png)  

If you chose to save the BOM file, this file can be uploaded to the LCSC service yourself using the [BOM Tool](https://lcsc.com/user/bom).  
![BOM tool](../Resources/LCSC%20order/LCSC-6-BOM-tool.png)  

Select the previously downloaded BOM file and drag it to the download area, or select the BOM file yourself from your file system.  
![BOM upload](../Resources/LCSC%20order/LCSC-7-BOM-upload.png)  

In the case of automatic redirection through "One-click Purchasing at LCSC" or in case of self-loading the BOM file, you will see the generated pre-order based on the received data from the BOM file. However, at this stage, there are three possible options for the availability of the necessary components:  

Сomponent in stock. In this case, no action is required, the necessary component is present in the warehouse and will be included in our order.  ![Component in stock](../Resources/LCSC%20order/LCSC-8-Component-in-stock.png)  

Component not found. In this case, the required component was not found, you can try to search for the necessary component yourself using a different search query. However, most likely you will not find anything, in this case, you can try to order this component for example at [Ebay].  
![Component not found](../Resources/LCSC%20order/LCSC-9-Component-not-found.png)  

Or component out of stock. In this case there are two ways to solve the problem. You can choose the mode "Backorder" where within 48 hours the request to the supplier for specification of cost and quantity of necessary components will be executed or to find analog of necessary component and independently to update the order. Personally, I recommend using the second method if you do not order any specific components (IC, transistors, etc.).  
![Component out of stock](../Resources/LCSC%20order/LCSC-10-Component-out-of-stock.png)  

Now, go to the product page that is out of stock. In this case it will be a resistor. And copy the resistor's nominal resistance (1k) and its form factor (0805) and paste this data into the search bar at the top of the site.  
![Component update](../Resources/LCSC%20order/LCSC-11-Component-update.png)  

After performing the search, you will be presented with a list of suitable components.  
![Component search](../Resources/LCSC%20order/LCSC-12-Component-search.png)  

Select the required component and go to the characteristics view page to make sure that you have chosen exactly what you need. After checking the characteristics, add the product you are interested in to your order.  
![New component](../Resources/LCSC%20order/LCSC-13-New-component.png)  

After resolving all conflicts with missing components, go back to our downloaded BOM file and add all the components we are interested in to the current order. At this stage, we add only those components that have the status **"In stock"**. To add a component to the order, click the "BUY" button. If you specify the number of components, lower than the minimum for the order, the system displays a warning message about the minimum order quantity.  
![Add to cart](../Resources/LCSC%20order/LCSC-14-Add-to-cart.png)  

Add all the components listed in the BOM file.  
![All component added](../Resources/LCSC%20order/LCSC-15-All-component-added.png)  

After adding all the components, go to your shopping cart for the current order by pressing the "GO TO CART & CHECK OUT" button. At this step you can make the last adjustments to your order.  
![Shopping cart](../Resources/LCSC%20order/LCSC-16-Shopping-cart.png)  

After checking the basket of your order, proceed to the next step - processing and payment of the order. To do this, press the "SECURE CHECKOUT" button. At this step, add your mailing address, choose the most convenient method of delivery and the preferred method of payment. After adding all the necessary data, click the "Confirm" button.  
![Checkout](../Resources/LCSC%20order/LCSC-17-Checkout.png)  

After payment of the order you can go to the "YOUR ORDERS" section and see a list of all the orders you have made.  
![Order history](../Resources/LCSC%20order/LCSC-18-Order-history.png)  

When choosing a specific order, you can see information about the address and method of delivery, find the number to track the parcel. When you click on the track number, you will be automatically redirected to the [4PX] website to track your parcel.  
![Order details](../Resources/LCSC%20order/LCSC-19-Order-details.png)  

Other articles:  
[How to export Gerber file from EasyEDA](./How%20to%20export%20Gerber%20file%20from%20EasyEDA.md)  
[How to order from JLCPCB](./How%20to%20order%20from%20JLCPCB.md)  
[How to make a PCB (LUT technology)](./How%20to%20make%20a%20PCB%20(LUT%20technology).md)  
[How to make a PCB (Photoresist method)](./How%20to%20make%20a%20PCB%20(Photoresist%20method).md)  
[How to use solder mask](./How%20to%20use%20solder%20mask.md)  
[How to work with SDR receivers on Linux](./How%20to%20work%20with%20SDR%20receivers%20on%20Linux.md)


[LCSC]: <https://lcsc.com/>
[EasyEDA]: <https://easyeda.com/>
[Ebay]: <https://www.ebay.com/>
[4PX]: <http://track.4px.com/>