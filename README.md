# The project implements some hardware devices for cheap SDR receivers based on Realtek RTL2832U controller 

![Easy-SDR](https://github.com/IgrikXD/Easy-SDR/blob/master/Resources/Main-cover.png)

## What is SDR?
[Software-defined radio (SDR)] is a radio communication system where components that have been traditionally implemented in hardware (e.g. mixers, filters, amplifiers, modulators/demodulators, detectors, etc.) are instead implemented by means of software on a personal computer or embedded system.  

## What are the objectives of this project?
Creating affordable, easy-to-manufacture prototypes of PCBs to working and expand the capabilities of existing low-cost SDR receivers based on RTL2832U chip. All the created elements of the project will have a detailed description of the manufacturing process, with all the existing features and possible problems.

## Current development progress:
[![Development status](https://img.shields.io/badge/Trello-Development%20status-blue.svg?longCache=true&style=for-the-badge)](https://trello.com/b/7NEPnfiD/easysdr) [![Create bug report](https://img.shields.io/badge/Google%20Form-Create%20bug%20report-red.svg?longCache=true&style=for-the-badge)](https://docs.google.com/forms/d/e/1FAIpQLSeUFM1p15N_vk8X_blSnZp6jPlZe_qRhiRlmntscx6jF2yRqw/viewform?usp=sf_link)

## Current available modules at EasyEDA platform:
- [Antenna Mini-Whip (TH)] &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;([Components list](./Antenna%20Mini-Whip/TH/Components%20list.md), [Assembly guide](./Antenna%20Mini-Whip/TH/Assembly%20guide.md))
- [Antenna Mini-Whip (SMD)] &nbsp;&nbsp;&nbsp;&nbsp;([Components list](./Antenna%20Mini-Whip/SMD/Components%20list.md), [Assembly guide](./Antenna%20Mini-Whip/SMD/Assembly%20guide.md))
- [HF Upconverter (TH)] &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;([Components list](./HF%20Upconverter/TH/Components%20list.md), [Assembly guide](./HF%20Upconverter/TH/Assembly%20guide.md), [Filters design files](./HF%20Upconverter/TH/Filters%20design%20files))
- [HF Upconverter (SMD)] &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;([Components list](./HF%20Upconverter/SMD/Components%20list.md), [Assembly guide](./HF%20Upconverter/SMD/Assembly%20guide.md), [Filters design files](./HF%20Upconverter/SMD/Filters%20design%20files))
- [PI Attenuator (SMD)] &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;([Components list](./PI%20Attenuator/SMD/Components%20list.md), [Assembly guide](./PI%20Attenuator/SMD/Assembly%20guide.md))

## Current available information articles:
- [How to export Gerber file from EasyEDA]
- [How to order from JLCPCB]
- [How to order from LCSC]
- [How to make a PCB (Toner transfer method)]
- [How to work with SDR receivers on Linux]

## How to use this repository?
In the root of the repository select a device of interest and go to the appropriate directory (for example [HF Upconverter](./HF%20Upconverter)). After the transition, select the component group of interest ([SMD](./HF%20Upconverter/SMD) or [TH](./HF%20Upconverter/TH)). Also in [Datasheets](./HF%20Upconverter/SMD/Datasheets) and [Schematics](./HF%20Upconverter/SMD/Schematics) directories you can find all necessary technical documentation for the used components in chosen module and schematic files in PDF format. If you only need GERBER files, you can find them in the appropriate [Gerbers](./HF%20Upconverter/SMD/Gerbers) directory for the selected components group. The next step is to choose the platform in which the project is implemented ([EasyEDA](./HF%20Upconverter/SMD/EasyEDA) or [Sprint Layout](./HF%20Upconverter/TH/Sprint%20Layout) (only for TH components)). After selecting the directory with the platform of interest, the list of files for implementing the device becomes available to you. After that, based on submitted files, you can make the device independently or order printed circuit boards for factory manufacturing.

## Where can I buy a SDR receiver?
You can order the SDR receiver on any of the currently available internet sites, such as Ebay, Aliexpress, Taobao, etc. Or you can use the following links to order some advanced versions of SDR receivers:

| SDR Store | Information |
| --------- | ----------- |
| [RTL-SDR.COM] | International shipping. Performed selling modified versions of receivers. Performs support and develop new versions. There is a large set of various useful information (software, articles, manuals, news). |
| [NooElec] | International shipping. Large selection of receivers and accessories. |
| [Airspy] | You can choose a retailer according to your whereabouts. Performs support and develop new versions. There are links for downloading software and working with the server. |

## Who helped me with the development of the project?
Great thanks to [RTL-SDR.COM] for the provided samples of SDR receivers RTL-SDR.COM V.3 and information support. [LCSC] company that provided most of the electronic components used for assembly for completely free. [Mini-Circuits] company for the providing samples of [ADE] frequency mixer by [EZ-Sample] program. And also [PCBWay] for $ 20 discount when ordering PCBs for the project.

## What was used mainly in the development?
| Source | Description |
| ------ | ------ |
| [PA0RDT Mini-Whip] | The original circuit of the active receiving antenna was used. The PCBs for TH components on platforms EasyEDA and Sprint Layout was implemented. |
| [RA0SMS Mini-Whip] | The original circuit of the active receiving antenna was used. The PCBs for SMD components on platform EasyEDA was implemented. |
| [Opendous Inc.'s OpenHardware] | Some useful information about HF Upconverter. |
| [Basic SDR Upconverter v1.0] | The original circuit of the HF Upconverter was used. The PCB for TH components on platforms EasyEDA and Sprint Layout was implemented. |
| [Upconverter1v3] | Some parts from original schematic were used. The PCBs for SMD components on platform EasyEDA was implemented. |

## How to contact me?
- E-mail: igor.nikolaevich.96@gmail.com
- Telegram: https://t.me/igrikxd
- LinkedIn: https://www.linkedin.com/in/igor-yatsevich/

[Software-defined radio (SDR)]: <https://en.wikipedia.org/wiki/Software-defined_radio>
[RTL-SDR.COM]: <https://www.rtl-sdr.com/buy-rtl-sdr-dvb-t-dongles/>
[NooElec]: <http://www.nooelec.com/store/sdr.html>
[Airspy]: <https://airspy.com/purchase/>
[LCSC]: <https://lcsc.com/>
[Mini-Circuits]: <https://ww2.minicircuits.com/homepage/homepage.html>
[PCBWay]: <https://www.pcbway.com/>
[ADE]: <https://www.minicircuits.com/WebStore/dashboard.html?model=ADE-1%2B>
[EZ-Sample]: <https://ww2.minicircuits.com/support/ez_sample.html>
[PA0RDT Mini-Whip]: <http://dl1dbc.net/SAQ/miniwhip.html>
[RA0SMS Mini-Whip]: <http://www.ra0sms.ru/p/the-active-antenna-mini-whip-10-khz-30.html>
[Opendous Inc.'s OpenHardware]: <https://github.com/ha7ilm/opendous/wiki>
[Basic SDR Upconverter v1.0]: <http://www.on1bes.be/sdr_up_conv_v1.0_ade1_125_en.html>
[Upconverter1v3]: <https://github.com/opendous/Upconverter1v3>
[Antenna Mini-Whip (TH)]: <https://easyeda.com/igor.nikolaevich.96/Antenna_Mini_Whip-d8935f151d3a4221a9a3aacae3acdb65>
[Antenna Mini-Whip (SMD)]: <https://easyeda.com/IgrikXD/Antenna_Mini_Whip_SMD-74e9e6740b814f6c901a811855125754>
[HF Upconverter (TH)]: <https://easyeda.com/IgrikXD/HF_Upconverter_ADE_series_mixers-b319a09d843a495baa5be52cb93d76d8>
[HF Upconverter (SMD)]: <https://easyeda.com/IgrikXD/HF_Upconverter_SMD-3cfb364d4cd2413abd3e60c4312f322d>
[PI Attenuator (SMD)]: <https://easyeda.com/IgrikXD/PI-Attenuator-SMD>
[How to export Gerber file from EasyEDA]: <./Useful%20info/How%20to%20export%20Gerber%20file%20from%20EasyEDA.md>
[How to order from JLCPCB]: <./Useful%20info/How%20to%20order%20from%20JLCPCB.md>
[How to order from LCSC]: <./Useful%20info/How%20to%20order%20from%20LCSC.md>
[How to make a PCB (Toner transfer method)]: <./Useful%20info/How%20to%20make%20a%20PCB%20(Toner%20transfer%20method).md>
[How to work with SDR receivers on Linux]: <./Useful%20info/How%20to%20work%20with%20SDR%20receivers%20on%20Linux.md>
