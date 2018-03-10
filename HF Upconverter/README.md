# HF Upconverter

Easy and quick building of HF Upconverter at the [TH component group](./TH) or [SMD component group](./SMD/EasyEDA). Module includes schematic (EasyEDA) and PCB files (EasyEDA, Sprint layout). Based on the submitted files, you can independently manufacture a PCB or order its production at the factory. In turn, I developed PCB for the independently manufacturing based on the existing circuit. As a result, the self-made manufacture of the upconverter is cheaper than buying a ready-made module.

## How it works?
HF Upconverter was based on the idea of an shifting the frequency up by a certain value (I use 125 MHz value), after this conversion your receiver will be able to correctly process frequencies below 30 MHz with less loss of useful signal.

For example: 
We want to receive a signal with frequency **4625 kHz**. But if we try to receive this signal directly to SDR receiver, without any transformations, we most likely will not hear anything. Why? Answer is simple - **RTL2832 can not process a signal with such a low frequency**. Sure, now some SDR recievers allows to use Direct Sampling mode which transform signal directly to RTL2832 bypassing R820T/R820T2 chips (perfect realisation for example at RTL-SDR.COM V.3). But this method confidently receives signals only with frequency lower than 14400 kHz and also has a low sensitivity. However exist method shifting frequency by a certain value up, this method named Up-сonverting. For implementation, an auxiliary generator is used, to shift the original signal with a certain frequency(in this module we will use 125 MHz) and a mixer where the input signal is additioned to the generator signal. When we using a generator at 125 MHz, the frequency shift of our received radio station will look like this: **4.625 MHz + 125 MHz = 129.625 MHz**. Also, we need to use input and output filters to suppress unnecessary signals and reduce interference. After all transformations, our SDR receiver will be able to process the signal of this frequency without any problems. After that, we can also set the amount of offset in the software used for reception. The last step is necessary for the frequency of our radio station to be displayed exactly as 4.625 MHz and not 129.625 MHz.


## Current available implementations at EasyEDA platform:
- [HF Upconverter (TH)]
- [HF Upconverter (SMD)]

## What was used in the development?
| Source | Description |
| ------ | ------ |
| [Upconverter1v3] | Use some parts from original schematic. The PCBs for SMD components on platform EasyEDA was implemented. |
| [Basic SDR Upconverter v1.0] | The original circuit of the HF Upconverter was used. The PCB for TH components on platforms EasyEDA and Sprint Layout was implemented. |
| [Opendous Inc.'s OpenHardware] | Some useful information about HF Upconverter. |
| [Butterworth filter] |  |

[HF Upconverter (TH)]: <https://easyeda.com/IgrikXD/HF_Upconverter_ADE_series_mixers-b319a09d843a495baa5be52cb93d76d8>
[HF Upconverter (SMD)]: <https://easyeda.com/IgrikXD/HF_Upconverter_SMD-3cfb364d4cd2413abd3e60c4312f322d>
[Upconverter1v3]: <https://github.com/opendous/Upconverter1v3>
[Basic SDR Upconverter v1.0]: <http://home.scarlet.be/on1bes/sdr_up_conv_v1.0_ade1_125_en.html>
[Opendous Inc.'s OpenHardware]: <https://github.com/ha7ilm/opendous/wiki>
[Butterworth filter]: <https://en.wikipedia.org/wiki/Butterworth_filter>


[Elliptic filter]: <https://en.wikipedia.org/wiki/Elliptic_filter>
[Low-pass filter]: <https://en.wikipedia.org/wiki/Low-pass_filter>
[High-pass filter]: <https://en.wikipedia.org/wiki/High-pass_filter>
[Attenuator]: <https://en.wikipedia.org/wiki/Attenuator_(electronics)>
[Еще раз о приеме КВ на RTL-SDR]: <https://m.geektimes.ru/post/289241/>
[Защита устройств от неправильной подачи полярности питания]: <https://habrahabr.ru/post/254035/>
[Широкополосный SDR радиосканер из DVB тюнера]: <https://vk.com/dvb_tv>
[Снимки с метеоспутников + SDR]: <https://vk.com/noaa_sat>