# HF Upconverter

An easy and quick building of "HF Upconverter" module based on [SMD components](./SMD/EasyEDA) and used for working with [LF], [MF] and [HF] bands on SDR receivers. The module includes a [schematic](./SMD/Schematics) and [PCB GERBER files](./SMD/Gerbers) prepared for setting up into aluminum enclosure with dimensions 80 x 50 x 20 mm with SMA connectors. Based on the submitted files, you can order PCB manufacturing at the factory ([PCBWay], [JLCPCB]). In turn, I developed PCB for the independently manufacturing based on the existing circuit. As a result, the self-made manufacture of the "HF Upconverter" module is cheaper than buying a ready-made device.

## Current development progress:
[![Progress](https://img.shields.io/badge/HF%20Upconverter%20%28SMD,%20ENCLOSURE%29-tested-green.svg)](https://easyeda.com/IgrikXD/hf-upconverter-smd-enclosure) [![Progress](https://img.shields.io/badge/version-1.0.EE-blue.svg)](./SMD/EasyEDA)  

## Current available implementations at EasyEDA platform:
- [HF Upconverter (SMD, ENCLOSURE)] ([Components list](./SMD/Components%20list.md), [Assembly guide](./SMD/Assembly%20guide.md), [Filters design files](./SMD/Filters%20design%20files), [Enclosure model files](./SMD/Enclosure%20model%20files))

## How does it work?
HF Upconverter was based on the idea of an shifting the frequency up by a certain value (I use 125 MHz value), after this conversion your receiver will be able to correctly process frequencies below 30 MHz with less loss of useful signal.

For example, we want to receive a signal with frequency [**4625 kHz**](https://en.wikipedia.org/wiki/UVB-76). But if we try to receive this signal directly to SDR receiver, without any transformations, we most likely will not hear anything. Why? The answer is simple - **SDR receivers based on RTL2832U and R820T/R820T2 can not process a signal with such a low frequency**. Sure, now some SDR receivers allow using Direct Sampling mode which transforms signal directly to RTL2832U bypassing R820T/R820T2 chips (perfect realization for example at [RTL-SDR.COM V.3]) and allows you to receive signals up to 30 MHz. But this method confidently receives signals only with a frequency lower than 14400 kHz and also has a low sensitivity and the presence of a mirror channel.  
However exist method shifting frequency by a certain value up, this method named **Up-сonverting**. For implementation, an auxiliary generator is used, to shift the original signal to a certain frequency (in this module we will use 125 MHz, this is important since the output filters are designed specifically for operation with this frequency) and a mixer where the input signal is mixed up to the generator signal. When we using a generator at **125 MHz**, the frequency shift of our received radio station will look like this: **4.625 MHz + 125 MHz = 129.625 MHz**. Also, we need to use input ([Low-pass filter]) and output ([High-pass filter]) filters to suppress unnecessary signals and reduce noise. After all transformations, our SDR receiver will be able to process the signal of this frequency without any problems.  
After that, we can also set the amount of offset in the software used for reception. The last step is necessary for the frequency of our radio station to be displayed exactly as 4.625 MHz and not 129.625 MHz.

At the moment, the method described above is the best way to work with the SDR receiver in the frequency range up to 30 MHz (subject to the availability of an appropriate antenna).

## HF Upconverter diagram
![HF Upconverter diagram](../Resources/HF%20Upconverter/Upconverter-diagram.png)

## Basic characteristics of the HF Upconverter module:

- **Input voltage:** USB type B, DC 5 V  
- **Input frequency range:** 0.5 - 65 MHz (according to the [datasheet on ADE-1+](./SMD/Datasheets/Mixers/ADE-1+-Frequency-mixer-Datasheet.pdf) and filters characteristics)  
- **Output frequency range:** 125.5 - 190 MHz  
- **RF connector:** SMA  
- **Feed line:** 50 Ohm coaxial cable  
- **Used PCB Material:** FR-4  
- **PCB thickness:** 1.6 mm  
- **PCB copper weight:** 1 oz  

## What was used in the development?
| Source | Description |
| ------ | ------ |
| [Upconverter1v3] | Some parts from the original schematic were used. The PCBs for SMD components on platform EasyEDA was implemented. |
| [Opendous Inc.'s OpenHardware] | Some useful information about HF Upconverter. |
| [Understanding Mixers and Their Parameters] | Article describing the operation principle of radio-frequency mixers and their parameters. |
| [PI Attenuator Calculator] | Online calculator for calculating the attenuator if you knowing the values of the resistors used. |
| [Еще раз о приеме КВ на RTL-SDR] | Article in Russian, describing how the converter works. |
| [USB-кабели и кабели питания] | Article in Russian, describing the types of USB cables encountered and the role of cable shield in USB devices. |
| [Типы зарядных портов] | An article in Russian, describing the power supply schemes for USB devices. |
| [Широкополосный SDR радиосканер из DVB тюнера] | The Russian community works with SDR receivers. Any user can ask a question of interest, open discussions. |
| [Software Defined Radio meteo] | The Russian community works with SDR receivers and is engaged in receiving images from meteorological satellites. Closed discussions, messages are moderated. |
| [VRTP community] | A large Russian community dedicated to electronics technologies implemented in hardware and software, including SDR and radio communications. |

Some theoretical information about used parts:
- [Low-pass filter]
- [High-pass filter]
- [Band-pass filter]
- [Butterworth filter]
- [Elliptic filter]
- [Attenuator]
- [Frequency mixer]

## Who helped improve this project?

- Guys from the [VRTP community]: [maugly](https://vrtp.ru/index.php?showuser=114228), [Werewolf](https://vrtp.ru/index.php?showuser=3), [Vit9xr](https://vrtp.ru/index.php?showuser=112693), [AntonSor](https://vrtp.ru/index.php?showuser=25633), [Eddy71](https://vrtp.ru/index.php?showuser=27360). Active assistance in the discussion of the developed design of the HF Upconverter PCB and analysis of technical solutions used in already existing solutions.
- [Alexander Sashimanu-San](https://vk.com/sashimanu) - Recommendation for improving the power circuit for noise reduction.

[LF]: <https://en.wikipedia.org/wiki/Low_frequency>
[MF]: <https://en.wikipedia.org/wiki/Medium_frequency>
[HF]: <https://en.wikipedia.org/wiki/Shortwave_radio>
[PCBWay]: <https://www.pcbway.com/>
[JLCPCB]: <https://jlcpcb.com/>
[HF Upconverter (SMD, ENCLOSURE)]: <https://easyeda.com/IgrikXD/hf-upconverter-smd-enclosure>
[Upconverter1v3]: <https://github.com/opendous/Upconverter1v3>
[Opendous Inc.'s OpenHardware]: <https://github.com/ha7ilm/opendous/wiki>
[Understanding Mixers and Their Parameters]: <http://www.mwrf.com/components/understanding-mixers-and-their-parameters>
[PI Attenuator Calculator]: <http://www.leleivre.com/rf_pipad.html>
[Еще раз о приеме КВ на RTL-SDR]: <https://habr.com/ru/post/373465/>
[USB-кабели и кабели питания]: <http://rones.su/techno/usb-dc-cables.html>
[Типы зарядных портов]: <http://rones.su/techno/charging_ports_types.html>
[Широкополосный SDR радиосканер из DVB тюнера]: <https://vk.com/dvb_tv>
[Software Defined Radio meteo]: <https://vk.com/noaa_sat>
[VRTP community]: <https://vrtp.ru/index.php?showforum=139>
[Low-pass filter]: <https://en.wikipedia.org/wiki/Low-pass_filter>
[High-pass filter]: <https://en.wikipedia.org/wiki/High-pass_filter>
[Band-pass filter]: <https://en.wikipedia.org/wiki/Band-pass_filter>
[Butterworth filter]: <https://en.wikipedia.org/wiki/Butterworth_filter>
[Elliptic filter]: <https://en.wikipedia.org/wiki/Elliptic_filter>
[Attenuator]: <https://en.wikipedia.org/wiki/Attenuator_(electronics)>
[Frequency mixer]: <https://en.wikipedia.org/wiki/Frequency_mixer>
[RTL-SDR.COM V.3]: <https://www.rtl-sdr.com/buy-rtl-sdr-dvb-t-dongles/>
