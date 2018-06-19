# raspbian-waveshare #
Simpler setup for the [waveshare raspberry pi tft 3.5" touch display](https://www.waveshare.com/wiki/3.5inch_RPi_LCD_(A))

## Steps ##

1. Plug in the micro sd card with rasbian installed into your computer's card reader
2. In the mounted ```boot``` partition, replace
    1. ```/boot/cmdline.txt```
    2. ```/boot/config.txt```
3. Copy the two overlay kernel drivers ```$ cp ./boot/overlays/* $MOUNTED_BOOT_PATH/overlays/```
4. Boot the raspberry pi and log in.
5. Run ```$ sudo nano /etc/default/console-setup```
    1. Overwrite value ```FONTFACE``` to ```FONTFACE="Terminus"```
    2. Overwrite value ```FONTSIZE``` to ```FONTSIZE="8x16"```
6. Run ```reboot``` and you're good to go!
