# How to export Gerber file from EasyEDA

## Why should I export these files?
The answer is simple - if you want to order production of PCBs on a platform other than [EasyEDA]/[JLCPCB], you need to export the files (Gerber) necessary for the production of your printed circuit board. After exporting the files, you will need to upload the received files to the PCB manufacturing service.

## Where can I order PCB manufacture?
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

## Exporting Gerber files
First, go to the page of the module you are interested in on the EasyEDA website.  
![Module page](../Resources/EasyEDA%20Gerber%20export/EasyEDA-1-Module-page.png)

Click the "Documents" button and drop below the "Open in Editor" button.  
![Open editor](../Resources/EasyEDA%20Gerber%20export/EasyEDA-2-Open-editor.png)

Click this button, whereby you will be taken to the EasyEDA editor where you can pre-edit the layout of the PCB before exporting.  
![Editor](../Resources/EasyEDA%20Gerber%20export/EasyEDA-3-Editor.png)

After all the necessary corrections we can make exporting the Gerber file. To do this, you need to on the right, in the top panel of the editor, click the "Generate Gerber" button.  
![Gerber export](../Resources/EasyEDA%20Gerber%20export/EasyEDA-4-Gerber-export.png)

Next, small window appearing where you can see a small image of your PCB and some information needed for placing an order on the JLCPCB (manufacturing parameters, quantity, shipping information and price). At this step, you can either just **save the Gerber file, by pushing "Generate Gerber" button**, preview the Gerber file with "Gerber View", or going to the JLCPCB platform to ordering the PCB.  
![Gerber preview](../Resources/EasyEDA%20Gerber%20export/EasyEDA-5-Gerber-preview.png)

Gerber View page  
![Gerber view](../Resources/EasyEDA%20Gerber%20export/EasyEDA-6-Gerber-view.png)

Redirecting to JLCPCB  
![JLCPCB redirect](../Resources/EasyEDA%20Gerber%20export/EasyEDA-7-JLCPCB-redirect.png)

If you choose redirection to JLCPCB, the Gerber file will be automatically downloaded to JLCPCB checked for trace errors, the price and time of production are calculated. After that you can pay for the formed order.  
![Gerber upload](../Resources/EasyEDA%20Gerber%20export/EasyEDA-8-Gerber-upload.png)

Successfully uploaded  
![Upload success](../Resources/EasyEDA%20Gerber%20export/EasyEDA-9-Gerber-upload-success.png)


[EasyEDA]: <https://easyeda.com/>
[JLCPCB]: <https://jlcpcb.com/>
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