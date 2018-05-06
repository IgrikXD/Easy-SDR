# How to make a PCB (Toner transfer method)

The manufacture of a PCB by **toner transfer method is based on the preliminary preparation of the template of the PCB and subsequent printing on photographic paper using a laser printer**. Next, the resulting image of the PCB is transferred to the copper clad board by heating. After that, the top part of the photo paper is removed, and the toner remains on the copper clad board. After that, etching and subsequent processing of the finished PCB is carried out.  

**This method is excellent for projects where there is no need for a low thickness of tracks, as well as for projects where there is no need to manufacture a large number of printed circuit boards (1-2 pieces)**. However, when using this method, there may be difficulties with the quality transfer of toner on the cooper clad board. In addition, this method is the cheapest if you have a laser printer at home.  

If you need to perform very tight placing of components or use a low thickness of the tracks, it is better to choose the photoresist method.  

As an example for the production of a PCB by toner transfer method, I will use the [Antenna Mini-Whip (TH)] module.

## Required components
To manufacture a PCB you will need:

- Single-layer copper clad board which corresponding size of the designed PCB  
- Tool for trimming the PCB workpiece  
- Fine grained sandpaper  
- Glossy photo paper or thermal transfer paper (its size should be greater than or equal to the manufactured PCB)  
- Clothes iron  
- Acetone or solvent
- Alcohol  
- Plastic or glass container for etching PCB  
- Hydrogen peroxide, 3% solution, 100 ml.  
- Citric acid, 30 g.  
- Table salt, 5 g.  
- Drill machine for drilling holes (in case of using TH components)  
- Drills, diameter 0.6 mm. and 1 mm. (in case of using TH components)  
- Liquid tin (optional)  
- Flux  
- Solder  

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
- BottomLayer - export (true) - mirror (false);  
Other layers doesn't used.  

**These parameters are used only for this example and are suitable only for printed circuit boards designed for TH components**, in case of PCB manufacture for SMD components you will have to use TopLayer with the parameter "mirror (true)".  
![Export settings](../Resources/PCB%20Toner%20transfer/PCB-4-Export-settings.png)  

After setting the above settings, click the "Export" button, after which the required file will be automatically downloaded. If the project has several PCB files, repeat this action for each of the files. In our example, we perform export for Antenna Mini-Whip PCB (TH) files: Main module and Antenna Mini-Whip PCB (TH): Power feed unit.  

The next step is to transfer the resulting images of PCBs to photo paper. Open the downloaded image files of the PCBs (I use Adobe Acrobat Reader DC) and print the received files using: File -> Print ... (Ctrl + P).  

**At this stage, you need to set the following parameters**:  
- Page Sizing & Handling - Push "Size" button and choice "Actual size";  
- Orientation - Portrait (this setting will set printing from the upper left corner of the paper);  

However, do not rush to print the template itself, at first you need to set up additional settings.  
![Templates printing settings](../Resources/PCB%20Toner%20transfer/PCB-5-Templates-printing-settings.png)  

You need to **turn off the toner save function** when printing (this is necessary in order to get more toner on the photographic paper and later on the PCB). To do this, you need to set this function in the settings of your printer before printing (for different printer models, the settings may vary).  
![Toner settings](../Resources/PCB%20Toner%20transfer/PCB-6-Toner-settings.png)  

Now you can insert photo paper or thermal transfer paper into your printer and print the templates. According to some reviews, the result of using thermal transfer paper will be better than the use of photo paper. However, in my projects I use photo paper and did not notice any negative moments. After printing templates, do not touch the toner surface with your hands. This can adversely affect the quality of toner transfer to the workpiece.  
![Templates printing](../Resources/PCB%20Toner%20transfer/PCB-7-Template-printing.png)  

After that you need to gently trim the excess photo paper on the outer contour of the printed template.  
![Template trimming](../Resources/PCB%20Toner%20transfer/PCB-8-Template-trimming.png)  

Now you have ready templates for toner transfer, prepare the copper clad board for the subsequent transfer of the toner. Cut the copper clad board according to the size of the printed template. **Do not leave unnecessary space**, since in the absence of a drilling machine small pieces of the PCB in future are difficult to remove with the help of a hand tool.  
![Copper clad board trimming](../Resources/PCB%20Toner%20transfer/PCB-9-Copper-clad-boadr-trimming.png)  

The resulting workpiece should be gently sanded with fine sandpaper to remove any oxides formed. **Do not apply great effort and do not use coarse-grained sandpaper to avoid spoiling the workpiece**.  
![Copper clad board sanding](../Resources/PCB%20Toner%20transfer/PCB-10-Copper-clad-boadr-sanding.png)  

Treat the surface of the workpiece with a acetone or solvent. After this stage, do not touch the working copper surface with your hands.  
![Finish preparing](../Resources/PCB%20Toner%20transfer/PCB-11-Finish-preparing.png)  

Now you are ready to transfer the toner to the workpiece. Turn on the clothes iron, set the maximum temperature and wait for it to warm up. At this time, place the printed template on top of the cutted out workpiece.  
![Template placing](../Resources/PCB%20Toner%20transfer/PCB-12-Template-placing.png)  

Cover the workpiece with a sheet of plain paper and heat it for about 40 seconds. Do circular motions with an iron with a little effort (without applying significant effort, since in some cases the toner may shift). **It is necessary to warm the entire workpiece evenly**.  
![Heating](../Resources/PCB%20Toner%20transfer/PCB-13-Heating.png)  

After the warm-up is over, place the workpiece under the small press (I use several books) and allow the workpiece to cool completely (about 20 minutes).  
![Workpiece pressing](../Resources/PCB%20Toner%20transfer/PCB-14-Workpiece-pressing.png)  

The next step is to remove the top of the photo paper under which the toner remains. In a small basin pour water at room temperature and place the workpiece there for about 40 minutes.  
![Workpiece soaking](../Resources/PCB%20Toner%20transfer/PCB-15-Workpiece-soaking.png)  

After a lapse of 40 minutes, remove the workpiece from the water and gently, rolling with your fingers, remove the top layer of photo paper.  
**At this stage, the most fundamental problem of this method of manufacturing PCBs can arise - the toner is not transferred completely**, there are areas with fallen off toner. There may be several reasons for this:  
- Insufficient processing of the copper clad board. Poor removal of oxides (performing more intensive cleaning of workpiece), the appearance of greasy stains after the degreasing process (do not touch the work surface of the workpiece by hand).  
- The appearance of greasy spots on the printed template (do not touch the working surface of the template with your hands).  
- Insufficient warming up of the template (increase the warm-up time or pay attention to the uniformity of warm-up).  
- Uneven copper clad board, there are curvatures (use another copper clad board).  

If you are faced with an problem of incomplete toner transfer, you will need to repeat the template printing and clear the workpiece from the old toner. Then repeat the transfer of toner process.  
![Paper removing](../Resources/PCB%20Toner%20transfer/PCB-16-Paper-removing.png)  

Now your workpiece is ready for etching. **Prepare the etching solution according to the following instructions**:  
- Take a plastic or glass container and pour in it 100 ml of 3% hydrogen peroxide;  
- Add 30 grams of citric acid;  
- Add 5 grams of table salt.  
Thoroughly mix the resulting solution until all components are completely dissolved.  

Place your workpiece in the prepared solution.  
![Performs etching](../Resources/PCB%20Toner%20transfer/PCB-17-Performs-etching.png)  

Wait until all the copper around the toner has dissolved, after which the etching process can be considered complete. Using tweezers, remove the printed circuit board.  
![Etching complete](../Resources/PCB%20Toner%20transfer/PCB-18-Etching-complete.png)  

Now you need to clean the workpiece of the residual etching solution with conventional water.  
![Workpiece washing](../Resources/PCB%20Toner%20transfer/PCB-19-Workpiece-washing.png)  

Then remove the toner with a acetone (solvent).  
![Toner removing](../Resources/PCB%20Toner%20transfer/PCB-20-Toner-removing.png)  

Current step is drilling holes for the installation of the necessary components (in case of using TH components) and sharp edges processing PCB with a sandpaper. In this example I use a 0.6 mm diameter drill for resistor / capacitor / inductor / transistor holes and 1 mm for diodes. After drilling all the necessary holes, peel the PCB with fine-grained sandpaper from the burrs.  
![Drilling](../Resources/PCB%20Toner%20transfer/PCB-21-Drilling.png)  

Now your circuit board is ready for tinning. Preheat the soldering iron, process the received PCB with flux and after that tin all copper tracks with the help of solder. Do not use too much solder, the main purpose of this stage is just to create a small protective layer, rather than pour all the PCB with solder.  
![Soldering iron tinning](../Resources/PCB%20Toner%20transfer/PCB-22-Soldering-iron-tinning.png)  

Alternatively, you can use liquid tin, for this, take a small container, pour out the solution of liquid tin and place the received PCB there. Wait until the process of chemical tinning is completed (all the tracks will be covered with a layer of tin).    
![Liquid tin](../Resources/PCB%20Toner%20transfer/PCB-23-Liquid-tin.png)  

Wash the printed circuit board from the flux residues with alcohol, or from the remnants of the chemical etching solution with water. After that, your circuit board is ready for soldering the necessary components. A printed circuit board made using a toner transfer method:  
![Finished PCB](../Resources/PCB%20Toner%20transfer/PCB-24-Finished-PCB.png)  

Other articles:  
[How to export Gerber file from EasyEDA](./How%20to%20export%20Gerber%20file%20from%20EasyEDA.md)  
[How to order from JLCPCB](./How%20to%20order%20from%20JLCPCB.md)  
[How to order from LCSC](./How%20to%20order%20from%20LCSC.md)  
[How to make a PCB (Photoresist method)](./How%20to%20make%20a%20PCB%20(Photoresist%20method).md)  
[How to work with SDR receivers on Linux](./How%20to%20work%20with%20SDR%20receivers%20on%20Linux.md)


[Antenna Mini-Whip (TH)]: <https://easyeda.com/igor.nikolaevich.96/Antenna_Mini_Whip-d8935f151d3a4221a9a3aacae3acdb65>