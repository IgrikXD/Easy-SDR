# How to work with SDR receivers on Linux

In this tutorial, I'll show you how to work with SDR receivers in Linux. [Manjaro Linux] distribution will be used for the work, however, any Arch-based distribution will work for this manual.

## Why did I choose Manjaro Linux?
There are several reasons why I chose [Manjaro Linux]. I used Archlinux for a long time and I'm just used to working with this distribution, however, this distribution can be difficult to configure for beginners. Therefore, it was decided to find something simple to configure, "working out of the box", so that a user who had not previously encountered Linux could easily figure out what's what. For this reason, [Manjaro Linux] was chosen. As for the popular Ubuntu Linux distribution, in my opinion, the instructions presented below will be slightly simpler than the existing instructions for a similar configuration for the Ubuntu Linux distribution.

## What do you need for work?
- SDR receiver (I will use [RTL-SDR.COM V3]);
- Antenna for the range you are interested in (I will use [Antenna Mini-Whip (TH)]);
- Computer with [Manjaro Linux] installed (Preferably a laptop with battery power, will be less noise when receiving);
- Internet connection (for downloading the required packages);  

At this tutorial I will use [Manjaro Linux 17.1.7 with Deepin DE](https://osdn.net/projects/manjaro-community/storage/deepin/) with a pre-installed fish shell and a disabled sudo password. However, you don't need set this shell and turning off the password, all actions are repeated on the newly installed, clean system.

## Installing and configuring the required packages
First open the terminal and perform a complete [system upgrade](https://wiki.archlinux.org/index.php/pacman#Upgrading_packages) using the command:
```sh
sudo pacman -Syu
```
This command synchronizes the repository databases and updates the system's packages.  
![Upgrade](../Resources/SDR%20on%20Linux/Linux-1-Upgrade.png)  

The next step is to [install](https://wiki.archlinux.org/index.php/pacman#Installing_packages) the Gqrx package, which is used to work with SDR receivers.
```sh
sudo pacman -S gqrx
```
![Upgrade](../Resources/SDR%20on%20Linux/Linux-2-Gqrx-install.png)  

At the completion of this step, all the necessary dependencies will automatically load. Also, automatic unloading of the kernel modules interfering with the operation of the receiver in the SDR mode will be performed.

After the above steps, you can start working with your SDR receiver. Now, run gqrx and setting up its initial configuration.
```sh
gqrx
```
After executing this command, you will see the basic Gqrx settings window.  
![Upgrade](../Resources/SDR%20on%20Linux/Linux-3-Gqrx-basic-settings.png)  

To work with our SDR receiver in the field "**Device**" select the value "**Realtek RTL2832UHIDIR SN: 00000001**".  
If you need the "Direct sampling" mode, the "**Device string**" field is given to the following form: "**rtl=0,direct_samp=2**" (without the quotes). If the mode "Direct sampling" is not needed, leave the "**Device string**" field in the form: "**rtl=0**" (without the quotes);  
The value of "**Input rate**" is set to a value **1800000**;  
The value of "**Decimation**" is set to a value of **16**;  

The last two parameters can be set in their own way, but the settings shown above allow you to simultaneously display a bandwidth of 100 kHz, which is more convenient for me.  
After setting all the parameters press the "OK" button and get into the Gqrx program. To start receiving, press the "**Play (Start DSP processing)**" button in the upper left part of the program.
![Upgrade](../Resources/SDR%20on%20Linux/Linux-4-Start-Gqrx.png)  

For a more detailed guide to working with the Gqrx program, you can use the following link: [Practical tricks and tips – Gqrx SDR]  
To find additional software for working with the received signal, you can use the following link: [Amateur radio (Software list) - ArchWiki]

## How can I make sure my SDR receiver is working?
Insert your receiver into the USB connector of the computer and run the following command:
```sh
rtl_test
```
This command will be executed indefinitely, until the user aborts execution. Stop the command about a minute after the start (Ctrl + C). If, as a result of the command, the value of "Samples per million lost (minimum)" is zero, your device is working properly.  
![Upgrade](../Resources/SDR%20on%20Linux/Linux-5-Rtl-test.png)  

## How to use software selectable Bias Tee?
For using software selectable Bias Tee you should make following steps (manual from [RTL-SDR Blog V.3. Dongles User Guide]):
```sh
sudo pacman -S cmake
git clone https://github.com/rtlsdrblog/rtl_biast
cd rtl_biast
mkdir build
cd build
cmake ..
make
cd src
./rtl_biast -b 1
```
![Upgrade](../Resources/SDR%20on%20Linux/Linux-6-Install-cmake.png)  
![Upgrade](../Resources/SDR%20on%20Linux/Linux-7-Git-clone.png)  
![Upgrade](../Resources/SDR%20on%20Linux/Linux-8-Make.png)  
![Upgrade](../Resources/SDR%20on%20Linux/Linux-9-Rtl-biast.png)  

Important notice, **do not try to make "sudo make install"**, this command will work fine, but running the package with rtl_biast -b X will not work. This error was not eliminated by the developer at the time of April 2018. 

If you want to disable this mode, use the following command:
```sh
./rtl_biast -b 0
```

Other articles:  
[How to export Gerber file from EasyEDA](./How%20to%20export%20Gerber%20file%20from%20EasyEDA.md)  
[How to order from JLCPCB](./How%20to%20order%20from%20JLCPCB.md)  
[How to order from LCSC](./How%20to%20order%20from%20LCSC.md)  
[How to make a PCB (Toner transfer method)](./How%20to%20make%20a%20PCB%20(Toner%20transfer%20method).md)   
[How to make a PCB (Photoresist method)](./How%20to%20make%20a%20PCB%20(Photoresist%20method).md)  


[Manjaro Linux]: <https://manjaro.org/>
[RTL-SDR.COM V3]: <https://www.rtl-sdr.com/buy-rtl-sdr-dvb-t-dongles/>
[Antenna Mini-Whip (TH)]: <https://easyeda.com/igor.nikolaevich.96/Antenna_Mini_Whip-d8935f151d3a4221a9a3aacae3acdb65>
[Practical tricks and tips – Gqrx SDR]: <http://gqrx.dk/doc/practical-tricks-and-tips>
[Amateur radio (Software list) - ArchWiki]: <https://wiki.archlinux.org/index.php/Amateur_radio#Software_list>
[RTL-SDR Blog V.3. Dongles User Guide]: <https://www.rtl-sdr.com/rtl-sdr-blog-v-3-dongles-user-guide/>