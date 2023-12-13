# ACSI2STM-Quick-Start-Guide
---------------------------- 


This document explains the steps to get the recommended hardware and software as quickly and as simply as possible.
 
Installing the PCB
### 1 - Backup battery
Before installing, insert a CR2032 battery in the socket. The battery is only needed for keeping the clock running when the ST is off.
See this video on how to insert the battery: https://youtu.be/rgAsQ0IYjlg



### 2 - Installing on the DB19 port
* Plug the unit on the back of the ST, components toward the keyboard.  The mounting holes of the Hard Disk socket should be aligned.
* Put some screws to hold the unit in place (optional).  If you need screws, you can unscrew the hex screws of the Modem or Printer socket.
* Power the unit via the USB-C port.
* Optionally, you can plug other devices such as an UltraSatan on the IDC20  socket.



### 3A - Using microSD card formated in FAT32 in GemDrive mode
Using Fat and Fat32 microSD cards without any other action is known as “GemDrive” mode. This is the easiest way to use the card. It does not require any driver. The microSD card will be usable on a Windows PC (to transfer files to your Atari for example).
This mode has been tested and known to be working well on Atari ST, STE, Mega ST and Mega STE with TOS equal or above 1.04
That mode has not been tested on Atari TT030 and Falcon030. The TOS on these machines may not work in GemDrive mode.
 
#### 3A.1 - Setting date and time
In GemDrive mode, you can use any tool to set the date, such as `CONTROL.ACC` or `XCONTROL.ACC`. GemDrive redirects all system calls to the STM32 so the internal clock isn't used anymore.



### 3B - Using microSD card ACSI mode
Use a ready-made ACSI disk image
If you have a bootable hard disk image, the following sections will describe how to use it.


#### 3B.1 - Using the image directly
* Use a SD card formatted for PC (FAT32/ExFAT).
* Create a folder named `acsi2stm` at the root of the SD card.
* Copy your image inside that folder.
* Rename your image `hd0.img`.
* Insert the SD card in the ACSI2STM unit.
* Turn everything on.
* Enjoy.
The file format is the same used by the Hatari emulator. You can test your image in Hatari: go to the menu, click Hard disks, then click Browse on the first line (ACSI HD 0) then reboot the emulated ST. You can even use the image directly on the SD card by opening hd0.img from within Hatari !

When working with disk images, the SD card can be of any size, as long as it uses a standard filesystem (FAT, FAT32 or ExFAT). The ST only sees the content of the hd0.img file.

You can copy more than one disk image `xxxxx.img` on to the SD card, but only `hd0.img` will be used.

#### 3B.2 - Transfering a disk image to a raw SD card

Using a raw SD card is a bit faster than copying the image file.

To transfer images to the disk, you can use
[Raspberry Pi Imager](https://www.raspberrypi.com/software/):

* Open Raspberry Pi Imager.
* Click *Choose Os* under *Operating System*.
* Select *Use custom* in the list.
* Select the image file you wish to transfer.
* Under *Storage*, click *Choose storage*.
* Select the SD card you want to write to.
* Click *Write* to start writing. **Existing data on the SD card will be erased**. Click *Yes* to confirm.
* The SD card can now be used on the ST.

#### 3B.3 - Setting date and time
In ACSI mode, ACSI2STM emulates an UltraSatan clock, so you can use UltraSatan tools such as `US_SETCL.PRG` and `US_GETCL.PRG`. GemDrive mode also responds to UltraSatan clock queries as a convenience.
When the system is switched off, the STM32 clock is powered by the onboard CR2032 battery so it will keep time even when powered off.




 
If you want to do more than using microSD card in GemDrive mode, and how to use the card in general, please refer to the following links:

How to insert a battery https://youtu.be/rgAsQ0IYjlg

ACSI2STM GitHub https://github.com/retro16/acsi2stm

Atari ST pages by PP https://atari.8bitchip.info/

Disk Image with ICD driver http://joo.kie.sk/?page_id=332

How to launch ST disk images (Games) from the HD: https://atari.8bitchip.info/imgrun.php


 
