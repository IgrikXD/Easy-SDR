# The project implements some hardware devices and software for cheap SDR receivers based on Realtek RTL2832U controller 

## What is SDR?
[Software-defined radio (SDR)] is a radio communication system where components that have been traditionally implemented in hardware (e.g. mixers, filters, amplifiers, modulators/demodulators, detectors, etc.) are instead implemented by means of software on a personal computer or embedded system.

## What are the objectives of this project?
Creating affordable, easy-to-manufacture layouts of PCBs and software to working and expand the capabilities of existing low-cost SDR receivers available to ordinary users. All the created elements of the project will have a detailed description of the manufacturing process, with all the existing features and possible problems.

## Current available modules at EasyEDA platform:
- [Antenna Mini-Whip (TH)]
- [Antenna Mini-Whip (SMD)]
- [HF Upconverter (TH)]
- [HF Upconverter (SMD)]

## Current development progress:
[![Progress](http://progressed.io/bar/100?title=EasyEDA%20)](https://easyeda.com/IgrikXD) ![Progress](http://progressed.io/bar/100?title=Sprint%20Layout) ![Progress](http://progressed.io/bar/50?title=Documentation%20) ![Progress](http://progressed.io/bar/0?title=Testing)

## How to use this repository?
In the root of the repository, select the device of interest and go to the appropriate directory (for example [HF Upconverter](./HF%20Upconverter). After the transition, select the component group of interest ([SMD](./HF%20Upconverter/SMD) or [TH](./HF%20Upconverter/TH)), also in [Datasheets](./HF%20Upconverter/Datasheets) directory you can find all necessary technical documentation for the used components in chosen module. The next step is to choose the platform in which the project is implemented ([EasyEDA](./HF%20Upconverter/TH/EasyEDA) or [Sprint Layout](./HF%20Upconverter/TH/Sprint%20Layout)). After selecting the directory with the platform of interest, a list of files for implementing the device becomes available to you. After that, based on submitted files, you can make the device completely independently or order printed circuit boards for factory manufacturing.

## Where can I buy a SDR receiver?
You can order the SDR receiver on any of the currently available internet sites, such as Ebay, Aliexpress, Taobao, etc. Or you can use the following links to order some advanced versions of SDR receivers:

| SDR Store | Information |
| ----- | ----- |
| [RTL-SDR.COM] | International shipping. Performed selling modified versions of receivers. Performs support and develop new versions. There is a large set of various useful information (software, articles, manuals, news). |
| [NooElec] | International shipping. Large selection of receivers and accessories. |
| [Airspy] | You can choose a retailer according to your whereabouts. Performs support and develop new versions. There are links for downloading software and working with the server. |

Great thanks to [RTL-SDR.COM] for the provided samples of SDR receivers [RTL-SDR.COM V.3] and information support. And also [Mini-Circuits] for the provided samples of [ADE] frequency mixer by EZ-Sample program.

## What was used mainly in the development?
| Source | Description |
| ------ | ------ |
| [PA0RDT Mini-Whip] | The original circuit of the active receiving antenna was used. The PCBs for TH components on platforms EasyEDA and Sprint Layout was implemented. |
| [RA0SMS Mini-Whip] | The original circuit of the active receiving antenna was used. The PCBs for SMD components on platform EasyEDA was implemented. |
| [Opendous Inc.'s OpenHardware] | Some useful information about HF Upconverter. |
| [Basic SDR Upconverter v1.0] | The original circuit of the HF Upconverter was used. The PCB for TH components on platforms EasyEDA and Sprint Layout was implemented. |
| [Upconverter1v3] | Use some parts from original schematic. The PCBs for SMD components on platform EasyEDA was implemented. |

[Software-defined radio (SDR)]: <https://en.wikipedia.org/wiki/Software-defined_radio>
[RTL-SDR.COM]: <https://www.rtl-sdr.com/buy-rtl-sdr-dvb-t-dongles/>
[NooElec]: <http://www.nooelec.com/store/sdr.html>
[Airspy]: <https://airspy.com/purchase/>
[RTL-SDR.COM V.3]: <https://www.rtl-sdr.com/product/rtl-sdr-blog-v3-r820t2-rtl2832u-1ppm-tcxo-sma-software-defined-radio-dongle-only/>
[Mini-Circuits]: <https://ww2.minicircuits.com/homepage/homepage.html>
[ADE]: <https://www.minicircuits.com/WebStore/dashboard.html?model=ADE-1%2B>
[PA0RDT Mini-Whip]: <http://dl1dbc.net/SAQ/miniwhip.html>
[RA0SMS Mini-Whip]: <http://www.ra0sms.ru/p/the-active-antenna-mini-whip-10-khz-30.html>
[Opendous Inc.'s OpenHardware]: <https://github.com/ha7ilm/opendous/wiki>
[Basic SDR Upconverter v1.0]: <http://home.scarlet.be/on1bes/sdr_up_conv_v1.0_ade1_125_en.html>
[Upconverter1v3]: <https://github.com/opendous/Upconverter1v3>
[Antenna Mini-Whip (TH)]: <https://easyeda.com/igor.nikolaevich.96/Antenna_Mini_Whip-d8935f151d3a4221a9a3aacae3acdb65>
[Antenna Mini-Whip (SMD)]: <https://easyeda.com/IgrikXD/Antenna_Mini_Whip_SMD-74e9e6740b814f6c901a811855125754>
[HF Upconverter (TH)]: <https://easyeda.com/IgrikXD/HF_Upconverter_ADE_series_mixers-b319a09d843a495baa5be52cb93d76d8>
[HF Upconverter (SMD)]: <https://easyeda.com/IgrikXD/HF_Upconverter_SMD-3cfb364d4cd2413abd3e60c4312f322d>