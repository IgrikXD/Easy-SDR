# How to make a PCB (Toner transfer method)

The method of manufacturing a PCB using the toner transfer method is performs by printing a workpiece of PCB at a laser printer with using photo paper. After that, the image of the resulting blank is transferred to the copper clad board using clothes iron. The next step is etching the printed circuit board and preparing the mounting holes. Further, tinning of PCB is carried out and a layer of solder mask and silkscreen are applied. Instead of a solder mask, it is possible to apply a protective varnish.

## Required components
To manufacture a PCB you will need:

- Single-layer copper clad board which corresponding size of the designed PCB  
- Tool for trimming the PCB workpiece  
- Fine grained sandpaper  
- Glossy photo paper. Its size should be greater than or equal to the manufactured PCB  
- Clothes iron  
- Degreaser or solvent  
- Plastic or glass container for etching PCB  
- Hydrogen peroxide, 3% solution, 100 ml.  
- Citric acid, 30 g.  
- Table salt, 5 g.  
- Drill machine for drilling holes (in case of using TH components)  
- Drills, diameter 0.6 mm. and 1 mm. (in case of using TH components)  
- Liquid tin (optional)  
- Flux  
- Solder  

The manufacture of a PCB by **toner transfer method is based on the preliminary preparation of the template of the PCB and subsequent printing on photographic paper using a laser printer**. Next, the resulting image of the PCB is transferred to the copper clad board by heating. After that, the top part of the photo paper is removed, and the toner remains on the copper clad board. After that, etching and subsequent processing of the finished PCB is carried out.  

**This method is excellent for projects where there is no need for a low thickness of tracks, as well as for projects where there is no need to manufacture a large number of printed circuit boards (1-2 pieces)**. However, when using this method, there may be difficulties with the quality transfer of toner on the cooper clad board. In addition, this method is the cheapest if you have a laser printer at home.  

If you need to perform very tight placing of components or use a low thickness of the tracks, it is better to choose the photoresist method.  

As an example for the production of a PCB by toner transfer method, we will use the [Antenna Mini-Whip (TH)] module.

## Template preparation
First, go to the page of the module you are interested in on the EasyEDA website.  
![Module page](../Resources/PCB%20Toner%20transfer/PCB-1-Module-page.png)  

Select the Documents section, move down and click the "Open in Editor" button.  
![Open button](../Resources/PCB%20Toner%20transfer/PCB-2-Open-button.png)  

To prepare a future template, in the EasyEDA editor, choice PCB file and make: "Document -> Export -> PDF".  
![Template prepare](../Resources/PCB%20Toner%20transfer/PCB-3-Template-prepare.png)  

In the export settings, **you need to set the following parameters**:  
- Export option - PDF;  
- Layer type - Separated layer;  
- Color - Black on White;  

Layers settings:  
- TopLayer - export (true) - mirror (true);  
Other layers doesn't used.  
![Export settings](../Resources/PCB%20Toner%20transfer/PCB-4-Export-settings.png)  

After setting the above settings, click the "Export" button, after which the required file will be automatically downloaded. If the project has several PCB files, repeat this action for each of the files. In our example, we perform export for Antenna Mini-Whip PCB (TH) files: Main module and Antenna Mini-Whip PCB (TH): Power feed unit.  


[Antenna Mini-Whip (TH)]: <https://easyeda.com/igor.nikolaevich.96/Antenna_Mini_Whip-d8935f151d3a4221a9a3aacae3acdb65>