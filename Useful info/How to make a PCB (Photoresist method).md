# How to make a PCB (Photoresist method)

The production of a printed circuit board by the photoresist method is based on the preliminary preparation of a photomask of the future board. Next, using a photosensitive material (photoresist) by illuminating with an ultraviolet lamp, the template is transferred to the copper clad board, after which the future printed circuit board is developed in a solution of soda ash. After that, etching and subsequent processing of the finished PCB is carried out.  

This method of manufacturing PCBs is more labor-intensive than the toner transfer method, but it allows to obtain a better PCB. **The use of the photoresist method is more appropriate in the following cases**:
  
- Manufacturing of large PCBs. The toner transfer method can not guarantee high-quality toner transfer over large areas;  
- Manufacturing of printed circuit boards with a low thickness of tracks;  
- Manufacturing of printed circuit boards with a dense arrangement of components;  
- Manufacture of a large number of identical printed circuit boards. In this case, the manufactured photomask for one card can be reused for the production of similar PCBs.  

**The disadvantages of this method include the need to purchase additional materials** (UV lamp, film photoresist, transparent film for printing (it is not required if you order a seal in a printing house)) which can be difficult in some cities (in my city I could not find UV lamps in retail, so I ordered the necessary lamp from Ebay).

As an example for the production of a PCB by photoresist method, I will use the [HF Upconverter (TH)] module.

## Required components
To manufacture a PCB you will need:

- Single-layer copper clad board which corresponding size of the designed PCB  
- Tool for trimming the PCB workpiece  
- Fine grained sandpaper  
- Film photoresist  
- Scalpel or a sharp knife  
- Scotch tape  
- Transparent film for printing on inkjet/laser printer (it is not required if you order a seal in a printing house)  
- UV lamp  
- Plexiglas for covering workpiece  
- Calcined soda  
- Small brush  
- Container for applying photoresist by wet method and developing photoresist  
- Clothes iron  
- Acetone or solvent (also, any liquid dishwashing detergent can be used for degreasing)  
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
![Module page](../Resources/PCB%20Photoresist/PCB-1-Module-page.png) 

Select the Documents section, move down and click the "Open in Editor" button.  
![Open button](../Resources/PCB%20Photoresist/PCB-2-Open-button.png)  

To prepare a future template, in the EasyEDA editor, choice PCB file and make: "Document -> Export -> PDF".  
![Template prepare](../Resources/PCB%20Photoresist/PCB-3-Template-prepare.png)  

Other articles:  
[How to export Gerber file from EasyEDA](./How%20to%20export%20Gerber%20file%20from%20EasyEDA.md)  
[How to order from JLCPCB](./How%20to%20order%20from%20JLCPCB.md)  
[How to order from LCSC](./How%20to%20order%20from%20LCSC.md)  
[How to make a PCB (Toner transfer method)](./How%20to%20make%20a%20PCB%20(Toner%20transfer%20method).md)  
[How to work with SDR receivers on Linux](./How%20to%20work%20with%20SDR%20receivers%20on%20Linux.md)


[HF Upconverter (TH)]: <https://easyeda.com/IgrikXD/HF_Upconverter_ADE_series_mixers-b319a09d843a495baa5be52cb93d76d8>