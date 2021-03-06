# Raspberry Pi Setup

During this lab, you will set up your Raspberry Pi as a functional computer. You will also connect it to your computer so you can remotely login using the monitor on your comuputer rather then having to attach an external monitor, keyboard and mouse. Finally you will configure your Raspberry Pi to synchronize it's clock with the internet so it aways has the correct time. 

## Install Solderless Header

1. Place Raspberry Pi in Jig with Header resting gently in GPIO holes.
1. Using a hammer, gently tap Header into place.

## Flash Raspbian Stretch Lite Operating System

NOTE: Depends on [Raspbian Stretch Lite](http://director.downloads.raspberrypi.org/raspbian_lite/images/raspbian_lite-2018-06-29/2018-06-27-raspbian-stretch-lite.zip) and [Etcher](https://etcher.io).

1. Insert Micro SD card into SD card adapter and then insert SD card adapter into the SD card reader on your computer.
1. Launch Etcher.
1. Select downloaded Raspbian image.
1. Ensure the SD card reader drive is selected.
1. Flash the Micro SD card.

## Enable SSH

On Mac:

Follow https://desertbot.io/blog/ssh-into-pi-zero-over-usb.

On Windows:

Follow https://desertbot.io/blog/headless-pi-zero-ssh-access-over-usb-windows

## Connect to Raspberry Pi

1. Move Micro SD card to Raspberry Pi Micro SD card slot.
1. Connect Raspberry Pi's USB port (not PWR) to computer using Micro USB to USB cable.
1. SSH to Raspbery Pi
    * Mac or Linux
        1. Open terminal window.
        1. SSH
        ```
        ssh pi@raspberrypi.local
        ```
        1. Approve authenticity of host.
1. Enter raspberry as password.

## Configure Networking & Timezone

Networking and Timezone should be configured so it can automatically get the correct time.

NOTE: When you bring the binary clock home or change WiFi networks, you will have to reconfigure the network.

1. At the Raspberry Pi's command-line type:
```
sudo raspi-config
```
1. Goto Network Options.
1. Choose Wi-fi.
1. Select US.
1. Enter CodeMash for SSID and press enter for passphrase.
1. Goto Localisation Options.
1. Choose Change Timezone.
1. US
1. Select Eastern or timezone you reside in.
1. Finish.
1. Type the following on the command-line to validate date and time.
```
date
```

NOTE: While you are in raspi-config, it is probably a good idea to change the password as the default password is insecure and well known!!!