# ACSI2STM-Quick-Start-Guide
ACSI2STM Quick start guide

This document explains the steps to get the recommended hardware and software as quickly and as simply as possible.
 
Installing the PCB
### Backup battery
Before installing, insert a CR2032 battery in the socket. The battery is only needed for keeping the clock running when the ST is off.
See this video on how to insert the battery: 
 
### Installing on the DB19 port
* Plug the unit on the back of the ST, components toward the keyboard.  The mounting holes of the Hard Disk socket should be aligned.
* Put some screws to hold the unit in place (optional).  If you need screws, you can unscrew the hex screws of the Modem or Printer socket.
* Power the unit via the USB-C port.
* Optionally, you can plug other devices such as an UltraSatan on the IDC20  socket.
 
### Installing using the UltraSatan port
If you mounted an IDC20 socket, you can connect the ACSI2STM unit through it instead of the DB19 port. This is useful if you have other IDC20 devices.
Power the unit via the USB-C port. 
Using the unit
Power the unit via its USB-C port. It has no specific power requirements, so any 5V USB-C adapter (or PC) should be able to power the unit.
Insert any microSD card in its slots (at least the first slot). The SD card can be formatted as FAT32 (SDHC) or ExFAT (SDXC), which are the standard formats for the SD card.
Turn the ST on, the ACSI2STM unit should display a boot message and the C drive should be readily available on the desktop.
You need to manually install extra drive icons on the desktop to access the D or E drive.

Using Fat and Fat32 microSD cards is known as “GemDrive” mode. This is the easiest way to use the card. It does not require any driver. The microSD card will be usable on a Windows PC (to transfer files to your Atari for example).
 
Setting date and time
In GemDrive mode, you can use any tool to set the date, such as `CONTROL.ACC` or `XCONTROL.ACC`. GemDrive redirects all system calls to the STM32 so the internal clock isn't used anymore.
 
In ACSI mode, ACSI2STM emulates an UltraSatan clock, so you can use UltraSatan tools such as `US_SETCL.PRG` and `US_GETCL.PRG`. GemDrive mode also responds to UltraSatan clock queries as a convenience.
When the system is switched off, the STM32 clock is powered by the onboard CR2032 battery so it will keep time even when powered off.
 
If you want to do more than using microSD card in GemDrive mode, and how to use the card, please refer to the following links:

How to insert a battery https://youtu.be/rgAsQ0IYjlg

ACSI2STM GitHub https://github.com/retro16/acsi2stm

Atari ST pages by PP https://atari.8bitchip.info/

Disk Image with ICD driverhttp://joo.kie.sk/?page_id=332
 
