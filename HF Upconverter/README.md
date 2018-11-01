# HF Upconverter

An easy and quick building of HF Upconverter at the [TH component group](./TH) or [SMD component group](./SMD/EasyEDA). The module includes schematic (EasyEDA) and PCB files (EasyEDA, Sprint layout). Based on the submitted files, you can independently manufacture a PCB or order its manufacturing at the factory. In turn, I developed PCB for the independently manufacturing based on the existing circuit. As a result, the self-made manufacture of the upconverter is cheaper than buying a ready-made module.

## Current development progress:
[![Progress](https://img.shields.io/badge/HF%20Upconverter%20%28TH%29-not%20tested-yellow.svg)](https://easyeda.com/IgrikXD/HF_Upconverter_ADE_series_mixers-b319a09d843a495baa5be52cb93d76d8) [![Progress](https://img.shields.io/badge/version-7.10.EE-blue.svg)](./TH/EasyEDA)  
[![Progress](https://img.shields.io/badge/HF%20Upconverter%20%28TH%29-not%20tested-yellow.svg)](./TH/Sprint%20Layout) [![Progress](https://img.shields.io/badge/version-*.*.SL-blue.svg)](./TH/Sprint%20Layout)  
[![Progress](https://img.shields.io/badge/HF%20Upconverter%20%28SMD%29-tested-green.svg)](https://easyeda.com/IgrikXD/HF_Upconverter_SMD-3cfb364d4cd2413abd3e60c4312f322d) [![Progress](https://img.shields.io/badge/version-12.21.EE-blue.svg)](./SMD/EasyEDA)  

## Current available implementations at EasyEDA platform:
- [HF Upconverter (TH)] ([Components list](./TH/Components%20list.md), [Assembly guide](./TH/Assembly%20guide.md), [Filters design files](./TH/Filters%20design%20files))
- [HF Upconverter (SMD)] ([Components list](./SMD/Components%20list.md), [Assembly guide](./SMD/Assembly%20guide.md), [Filters design files](./SMD/Filters%20design%20files))

## How does it work?
HF Upconverter was based on the idea of an shifting the frequency up by a certain value (I use 125 MHz value), after this conversion your receiver will be able to correctly process frequencies below 30 MHz with less loss of useful signal.

For example, we want to receive a signal with frequency **4625 kHz**. But if we try to receive this signal directly to SDR receiver, without any transformations, we most likely will not hear anything. Why? The answer is simple - **RTL2832U can not process a signal with such a low frequency**. The sensitivity of the receiver in this range is extremely low, which at best will allow us to receive only powerful broadcast stations. Sure, now some SDR receivers allow using Direct Sampling mode which transforms signal directly to RTL2832U bypassing R820T/R820T2 chips (perfect realization for example at [RTL-SDR.COM V.3]) and allows you to receive signals up to 30 MHz. But this method confidently receives signals only with a frequency lower than 14400 kHz and also has a low sensitivity.  
However exist method shifting frequency by a certain value up, this method named **Up-сonverting**. For implementation, an auxiliary generator is used, to shift the original signal to a certain frequency (in this module we will use 125 MHz, this is important since the output filters are designed specifically for operation with this frequency) and a mixer where the input signal is mixed up to the generator signal. When we using a generator at **125 MHz**, the frequency shift of our received radio station will look like this: **4.625 MHz + 125 MHz = 129.625 MHz**. Also, we need to use input ([Low-pass filter]) and output ([High-pass filter]) filters to suppress unnecessary signals and reduce noise. After all transformations, our SDR receiver will be able to process the signal of this frequency without any problems.  
After that, we can also set the amount of offset in the software used for reception. The last step is necessary for the frequency of our radio station to be displayed exactly as 4.625 MHz and not 129.625 MHz.

At the moment, the method described above is the best way to work with the SDR receiver in the frequency range up to 30 MHz (subject to the availability of an appropriate antenna).

## HF Upconverter diagram
![HF Upconverter diagram](../Resources/HF%20Upconverter/Upconverter-diagram.png)

## What was used in the development?
| Source | Description |
| ------ | ------ |
| [Upconverter1v3] | Some parts from the original schematic were used. The PCBs for SMD components on platform EasyEDA was implemented. |
| [Basic SDR Upconverter v1.0] | The original circuit of the HF Upconverter was used. The PCB for TH components on platforms EasyEDA and Sprint Layout was implemented. |
| [Opendous Inc.'s OpenHardware] | Some useful information about HF Upconverter. |
| [Understanding Mixers and Their Parameters] | Article describing the operation principle of radio-frequency mixers and their parameters. |
| [PI Attenuator Calculator] | Online calculator for calculating the attenuator if you knowing the values of the resistors used. |
| [How to protect circuits from reversed voltage polarity!] | The video describing the principle of protecting electrical appliances from an improper polarity of power. This decision was used in HF Upconverter (SMD) module. |
| [Еще раз о приеме КВ на RTL-SDR] | Article in Russian, describing how the converter works. |
| [Защита устройств от неправильной подачи полярности питания] | Article in Russian, describing the principle of protecting electrical appliances from improper polarity of power. This decision was used in HF Upconverter (SMD) module. |
| [Схемы переключения устройства на резервный источник] | Article in Russian, describing examples of various switching schemes for power supplies. |
| [USB-кабели и кабели питания] | Article in Russian, describing the types of USB cables encountered and the role of cable shield in USB devices. |
| [Типы зарядных портов] | An article in Russian, describing the power supply schemes for USB devices. |
| [Широкополосный SDR радиосканер из DVB тюнера] | The Russian community works with SDR receivers. Any user can ask a question of interest, open discussions. |
| [Software Defined Radio meteo] | The Russian community works with SDR receivers and is engaged in receiving images from meteorological satellites. Closed discussions, messages are moderated. |

Some theoretical information about used parts:

- [Low-pass filter]
- [High-pass filter]
- [Band-pass filter]
- [Butterworth filter]
- [Elliptic filter]
- [Attenuator]
- [Frequency mixer]

## Who helped improve this project?

- [Alexander Sashimanu-San](https://vk.com/sashimanu) - Recommendation for improving the power circuit for noise reduction. The idea of implementing an upconverter, which using power circuit based at LM1117 (not implemented at the moment).

[HF Upconverter (TH)]: <https://easyeda.com/IgrikXD/HF_Upconverter_ADE_series_mixers-b319a09d843a495baa5be52cb93d76d8>
[HF Upconverter (SMD)]: <https://easyeda.com/IgrikXD/HF_Upconverter_SMD-3cfb364d4cd2413abd3e60c4312f322d>
[Upconverter1v3]: <https://github.com/opendous/Upconverter1v3>
[Basic SDR Upconverter v1.0]: <http://www.on1bes.be/sdr_up_conv_v1.0_ade1_125_en.html>
[Opendous Inc.'s OpenHardware]: <https://github.com/ha7ilm/opendous/wiki>
[Understanding Mixers and Their Parameters]: <http://www.mwrf.com/components/understanding-mixers-and-their-parameters>
[PI Attenuator Calculator]: <http://www.leleivre.com/rf_pipad.html>
[Еще раз о приеме КВ на RTL-SDR]: <https://m.geektimes.ru/post/289241/>
[How to protect circuits from reversed voltage polarity!]: <https://www.youtube.com/watch?v=IrB-FPcv1Dc>
[Защита устройств от неправильной подачи полярности питания]: <https://habrahabr.ru/post/254035/>
[Схемы переключения устройства на резервный источник]: <http://avrproject.ru/forum/4-101-1>
[USB-кабели и кабели питания]: <http://rones.su/techno/usb-dc-cables.html>
[Типы зарядных портов]: <http://rones.su/techno/charging_ports_types.html>
[Широкополосный SDR радиосканер из DVB тюнера]: <https://vk.com/dvb_tv>
[Software Defined Radio meteo]: <https://vk.com/noaa_sat>
[Low-pass filter]: <https://en.wikipedia.org/wiki/Low-pass_filter>
[High-pass filter]: <https://en.wikipedia.org/wiki/High-pass_filter>
[Band-pass filter]: <https://en.wikipedia.org/wiki/Band-pass_filter>
[Butterworth filter]: <https://en.wikipedia.org/wiki/Butterworth_filter>
[Elliptic filter]: <https://en.wikipedia.org/wiki/Elliptic_filter>
[Attenuator]: <https://en.wikipedia.org/wiki/Attenuator_(electronics)>
[Frequency mixer]: <https://en.wikipedia.org/wiki/Frequency_mixer>
[RTL-SDR.COM V.3]: <https://www.rtl-sdr.com/buy-rtl-sdr-dvb-t-dongles/>
