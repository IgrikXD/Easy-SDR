# How to prepare a PCB template (toner transfer method)

The manufacture of a PCB by **toner transfer method is based on the preliminary preparation of the template of the PCB and subsequent printing on photographic paper using a laser printer**. Next, the resulting image of the PCB is transferred to the copper clad board by heating. After that, the top part of the photo paper is removed, and the toner remains on the copper clad board. After that, etching and subsequent processing of the finished PCB are carried out.  

**This method is excellent for projects where there is no need for a low thickness of tracks, as well as for projects where there is no need to manufacture a large number of printed circuit boards (1-2 pieces)**. However, when using this method, there may be difficulties with the quality transfer of toner on the copper clad board. In addition, this method is the cheapest if you have a laser printer at home.  

If you need to perform very tight placing of components or use a low thickness of the tracks, it is better to choose the photoresist method.  

As an example for the preparation of a PCB template, I will use the [Antenna Mini-Whip (TH)] module.

## Template preparation
First, go to the page of the module you are interested in on the EasyEDA website.  
![Module page](../Resources/PCB%20Toner%20transfer/PCB-1-Module-page.png)  

Select the Documents section, move down and click the "Open in Editor" button.  
![Open button](../Resources/PCB%20Toner%20transfer/PCB-2-Open-button.png)  

To prepare a future template, in the EasyEDA editor, choice PCB file and make: "Document -> Export -> PDF".  
![Template prepare](../Resources/PCB%20Toner%20transfer/PCB-3-Template-prepare.png)  

In the export settings, **you need to set the following parameters**:  
- Export option - **PDF**;  
- Layer type - **Separated layer**;  
- Color - **Black on White**;  

Layers settings:  
- BottomLayer - **export (true) - mirror (false)**;  
Other layers don't use.  

**These parameters are used only for this example and are suitable only for printed circuit boards designed for TH components**, in case of PCB manufacturer for SMD components you will have to use TopLayer with the parameter "mirror (true)".  
![Export settings](../Resources/PCB%20Toner%20transfer/PCB-4-Export-settings.png)  

After setting the above settings, click the "Export" button, after which the required file will be automatically downloaded. If the project has several PCB files, repeat this action for each of the files. In this example, I perform export for Antenna Mini-Whip PCB (TH) files: Main module and Antenna Mini-Whip PCB (TH): Power feed unit.  

The next step is to transfer the resulting images of PCBs to photo paper. Open the downloaded image files of the PCBs (I use Adobe Acrobat Reader DC) and print the received files using: File -> Print ... (Ctrl + P).  

**At this stage, you need to set the following parameters**:  
- Page Sizing & Handling - Push "Size" button and choice "Actual size";  
- Orientation - Portrait (this setting will set printing from the upper left corner of the paper);  

However, do not rush to print the template itself, at first you need to set up additional settings.  
![Templates printing settings](../Resources/PCB%20Toner%20transfer/PCB-5-Templates-printing-settings.png)  

You need to **turn off the toner save function** when printing (this is necessary in order to get more toner on the photographic paper and later on the PCB). To do this, you need to set this function in the settings of your printer before printing (for different printer models, the settings may vary).  
![Toner settings](../Resources/PCB%20Toner%20transfer/PCB-6-Toner-settings.png)  

Now you can insert photo paper or thermal transfer paper into your printer and print the templates. According to some reviews, the result of using thermal transfer paper will be better than the use of photo paper. However, in my projects, I use photo paper and did not notice any negative moments. After printing templates, do not touch the toner surface with your hands. This can adversely affect the quality of toner transfer to the workpiece.  
![Templates printing](../Resources/PCB%20Toner%20transfer/PCB-7-Template-printing.png)  

After that, you need to gently trim the excess photo paper on the outer contour of the printed template.  
![Template trimming](../Resources/PCB%20Toner%20transfer/PCB-8-Template-trimming.png)  

Other articles:  
[How to export Gerber file from EasyEDA](./How%20to%20export%20Gerber%20file%20from%20EasyEDA.md)  
[How to order from JLCPCB](./How%20to%20order%20from%20JLCPCB.md)  
[How to order from LCSC](./How%20to%20order%20from%20LCSC.md)  
[How to work with SDR receivers on Linux](./How%20to%20work%20with%20SDR%20receivers%20on%20Linux.md)


[Antenna Mini-Whip (TH)]: <https://easyeda.com/igor.nikolaevich.96/Antenna_Mini_Whip-d8935f151d3a4221a9a3aacae3acdb65>
