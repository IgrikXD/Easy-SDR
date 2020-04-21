# The project implements some hardware devices for cheap SDR receivers based on Realtek RTL2832U controller 

![Easy-SDR](https://github.com/IgrikXD/Easy-SDR/blob/master/Resources/Main-cover.png)

## What is SDR?
[Software-defined radio (SDR)] is a radio communication system where components that have been traditionally implemented in hardware (e.g. mixers, filters, amplifiers, modulators/demodulators, detectors, etc.) are instead implemented by means of software on a personal computer or embedded system.  

## What are the objectives of this project?
Creating affordable, easy-to-manufacture prototypes of PCBs to working and expand the capabilities of existing low-cost SDR receivers based on [RTL2832U](https://www.realtek.com/en/products/communications-network-ics/item/rtl2832u) chip. All the created elements of the project will have a detailed description of the assembly process, with all the existing features and possible problems.

## Current development progress:
[![Development status](https://img.shields.io/badge/Trello-Development%20status-blue.svg?longCache=true&style=for-the-badge)](https://trello.com/b/7NEPnfiD/easysdr) [![Create bug report](https://img.shields.io/badge/Google%20Form-Create%20bug%20report-red.svg?longCache=true&style=for-the-badge)](https://docs.google.com/forms/d/e/1FAIpQLSeUFM1p15N_vk8X_blSnZp6jPlZe_qRhiRlmntscx6jF2yRqw/viewform?usp=sf_link)

## Currently available modules at EasyEDA platform:
[Antenna Mini-Whip (TH)] <div align="right">([README](./Antenna%20Mini-Whip/README.md), [Components list](./Antenna%20Mini-Whip/TH/Components%20list.md), [Assembly guide](./Antenna%20Mini-Whip/TH/Assembly%20guide.md)) </div> 

- [Antenna Mini-Whip (SMD)] &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;([README](./Antenna%20Mini-Whip/README.md), [Components list](./Antenna%20Mini-Whip/SMD/Components%20list.md), [Assembly guide](./Antenna%20Mini-Whip/SMD/Assembly%20guide.md))
- [Coax power supply, fixed voltage (SMD, ENCLOSURE)] &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;([README](./Coax%20power%20supply/Fixed%20voltage/README.md), [Components list](./Coax%20power%20supply/Fixed%20voltage/SMD/Components%20list.md), [Assembly guide](./Coax%20power%20supply/Fixed%20voltage/SMD/Assembly%20guide.md))
- [HF Upconverter (SMD, ENCLOSURE)] &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;([README](./HF%20Upconverter/README.md), [Components list](./HF%20Upconverter/SMD/Components%20list.md), [Assembly guide](./HF%20Upconverter/SMD/Assembly%20guide.md), [Filters design files](./HF%20Upconverter/SMD/Filters%20design%20files))
- [LNA, Bias Tee powered (SMD, ENCLOSURE)] &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;([README](./LNA/Bias%20Tee%20powered/README.md), [Components list](./LNA/Bias%20Tee%20powered/SMD/Components%20list.md), [Assembly guide](./LNA/Bias%20Tee%20powered/SMD/Assembly%20guide.md))
- [LNA, Bias Tee powered + filtering (SMD, ENCLOSURE)] &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;([README](./LNA/Bias%20Tee%20powered%20+%20filtering/README.md), [Components list](./LNA/Bias%20Tee%20powered%20+%20filtering/SMD/Components%20list.md), [Assembly guide](./LNA/Bias%20Tee%20powered%20+%20filtering/SMD/Assembly%20guide.md))
- [SPDT Antenna switch (SMD, ENCLOSURE)] &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;([README](./SPDT%20Antenna%20switch/README.md), [Components list](./SPDT%20Antenna%20switch/SMD/Components%20list.md), [Assembly guide](./SPDT%20Antenna%20switch/SMD/Assembly%20guide.md))

### Deprecated implementations of modules on the EasyEDA platform (will be reworked or removed):
- [HF Antenna power supply (SMD)] &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;([README](./HF%20Antenna%20power%20supply/README.md), [Components list](./HF%20Antenna%20power%20supply/SMD/Components%20list.md), [Assembly guide](./HF%20Antenna%20power%20supply/SMD/Assembly%20guide.md))
- [HF Upconverter (TH)] &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;([README](./HF%20Upconverter/README.md), [Components list](./HF%20Upconverter/TH/Components%20list.md), [Assembly guide](./HF%20Upconverter/TH/Assembly%20guide.md), [Filters design files](./HF%20Upconverter/TH/Filters%20design%20files))
- [HF Upconverter (SMD)] &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;([README](./HF%20Upconverter/README.md), [Components list](./HF%20Upconverter/SMD/Components%20list.md), [Assembly guide](./HF%20Upconverter/SMD/Assembly%20guide.md), [Filters design files](./HF%20Upconverter/SMD/Filters%20design%20files))
- [LNA (SMD)] &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;([README](./LNA/README.md), [Components list](./LNA/SMD/Components%20list.md), [Assembly guide](./LNA/SMD/Assembly%20guide.md))
- [PI Attenuator (SMD)] &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;([README](./PI%20Attenuator/README.md), [Components list](./PI%20Attenuator/SMD/Components%20list.md), [Assembly guide](./PI%20Attenuator/SMD/Assembly%20guide.md))


## Current available information articles:
- [How to export Gerber file from EasyEDA]
- [How to order from JLCPCB]
- [How to order from LCSC]
- [How to work with RTL-SDR receivers on Linux]

## How to use this repository?
In the root of the repository select a device of interest and go to the appropriate directory (for example [HF Upconverter](./HF%20Upconverter)). After the transition, select the component group of interest ([SMD](./HF%20Upconverter/SMD) or [TH](./Antenna%20Mini-Whip/TH)). Also in [Datasheets](./HF%20Upconverter/SMD/Datasheets) and [Schematics](./HF%20Upconverter/SMD/Schematics) directories, you can find all necessary technical documentation for the used components and schematic files in PDF format. If you only need GERBER files, you can find them in the appropriate [Gerbers](./HF%20Upconverter/SMD/Gerbers) directory for the selected components group. By the next step, you can download project files for the [EasyEDA](./HF%20Upconverter/SMD/EasyEDA) platform, which can later be [loaded into the editor](./HF%20Upconverter/SMD/EasyEDA/README.md) for viewing and editing. After that, based on the files presented, you can perform the necessary modifications to the device and order PCB for factory manufacturing.

## Where can I buy an SDR receiver?
You can order the SDR receiver on any of the currently available internet sites, such as eBay, Aliexpress, Taobao, etc. Or you can use the following links to order some advanced versions of SDR receivers:

| Store | Information |
| ----- | ----------- |
| [RTL-SDR.COM] | International delivery. Performed selling modified versions of receivers based on RTL2832U chip. Performs support and develop new versions of hardware solutions. There is a large set of various useful information (software, articles, manuals, news). |
| [NooElec] | International delivery. Large selection of SDR receivers based on RTL2832U chip and accessories, such as HF Upconverters, SAW filters, LNA, attenuators, antennas. |
| [Airspy] | Much more productive and expensive devices compared to devices based on RTL2832U. You can choose a retailer according to your whereabouts. Performs support and develop new versions of software and hardware solutions. There are links for [downloading SDRSharp](https://airspy.com/download/) and software for working with the server part. |

## Who helped me with the development of the project?
Great thanks to [RTL-SDR.COM] for the provided samples of SDR receivers RTL-SDR.COM V.3 and information support. [LCSC] company that provided most of the electronic components used for assembly for completely free. [Mini-Circuits] company for the providing samples of [ADE] frequency mixers, [PSA4-5043+] and [PGA-103+] amplifiers, and Bias Tees [TCBT-14+] by [EZ-Sample] program. And also [PCBWay] for $ 70 discount when ordering PCBs for the project.

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
[PSA4-5043+]: <https://www.minicircuits.com/WebStore/dashboard.html?model=PSA4-5043%2B>
[PGA-103+]: <https://www.minicircuits.com/WebStore/dashboard.html?model=PGA-103%2B>
[TCBT-14+]: <https://www.minicircuits.com/WebStore/dashboard.html?model=TCBT-14%2B>
[EZ-Sample]: <https://www.minicircuits.com/WebStore/ez_sample.html>
[Antenna Mini-Whip (TH)]: <https://easyeda.com/igor.nikolaevich.96/Antenna_Mini_Whip-d8935f151d3a4221a9a3aacae3acdb65>
[Antenna Mini-Whip (SMD)]: <https://easyeda.com/IgrikXD/Antenna_Mini_Whip_SMD-74e9e6740b814f6c901a811855125754>
[Coax power supply, fixed voltage (SMD, ENCLOSURE)]: <https://easyeda.com/IgrikXD/coax-power-supply-smd-enclosure>
[HF Upconverter (SMD, ENCLOSURE)]: <https://easyeda.com/IgrikXD/hf-upconverter-smd-enclosure>
[LNA, Bias Tee powered (SMD, ENCLOSURE)]: <https://easyeda.com/IgrikXD/bias-tee-lna-smd-enclosure>
[LNA, Bias Tee powered + filtering (SMD, ENCLOSURE)]: <https://easyeda.com/IgrikXD/bias-tee-filtering-lna-smd-enclosure>
[SPDT Antenna switch (SMD, ENCLOSURE)]: <https://easyeda.com/IgrikXD/spdt-antenna-switch-smd-enclosure>
[HF Antenna power supply (SMD)]: <https://easyeda.com/IgrikXD/Antenna-power-supply-SMD>
[HF Upconverter (TH)]: <https://easyeda.com/IgrikXD/HF_Upconverter_ADE_series_mixers-b319a09d843a495baa5be52cb93d76d8>
[HF Upconverter (SMD)]: <https://easyeda.com/IgrikXD/HF_Upconverter_SMD-3cfb364d4cd2413abd3e60c4312f322d>
[LNA (SMD)]: <https://easyeda.com/IgrikXD/LNA-SMD>
[PI Attenuator (SMD)]: <https://easyeda.com/IgrikXD/PI-Attenuator-SMD>
[How to export Gerber file from EasyEDA]: <./Useful%20info/How%20to%20export%20Gerber%20file%20from%20EasyEDA.md>
[How to order from JLCPCB]: <./Useful%20info/How%20to%20order%20from%20JLCPCB.md>
[How to order from LCSC]: <./Useful%20info/How%20to%20order%20from%20LCSC.md>
[How to work with RTL-SDR receivers on Linux]: <./Useful%20info/How%20to%20work%20with%20RTL-SDR%20receivers%20on%20Linux.md>
