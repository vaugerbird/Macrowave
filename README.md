# Macrowave by Ampersand/swirlybeard
**I, vaugerbird, take *zero* responsibilty for any of the files available in this repository. I have only posted them here for personal storage and remixing purposes. Any text beyond this line is original from Ampersand (with some edits to make GitHub markdown work).**

--------------------------------

This is a guide to making the Macrowave by Ampersand. 
Written on 27/03/21. 
All files provided are to be shared and used freely.

Macrowave is based on and uses the schematic from the Freedeck project: https://github.com/FreeYourStream

### Options to select when ordering the PCBs from JLCPCB
* Layers: 2
* Dimensions: 72 * 100 mm
* PCB Qty: 5
* Different Design 1
* Delivery Format: Single PCB
* PCB Thickness: 1.2
* PCB Color: Black
* Surface Finish: HASL(with lead)
* Copper Weight: 1 oz
* Gold Fingers: No
* Confirm Production file: No
* Flying Probe Test: Fully Test for Middle PCB, Not Test for Top and Bottom PCBs
* Castellated Holes: No
* Remove Order Number: Specify a Location
* Ignore the Advanced Options, No for both

### Flashing the Pro Micro 
* Use the Arduino IDE to flash the Pro Micro: https://www.arduino.cc/en/software
* The Freedeck software is here: https://github.com/FreeYourStream/freedeck-ino
Note that you will need to install some specific Arduino libraries as mentioned on the GitHub.
* app.ino is the file you need to open and flash in the Arduino IDE.

### Making a config.bin
* Go to https://freedeck.gosewis.ch/

This is the configurator for the Freedeck, add a page via the button in the top left and start customising your device. <br>
There is a folder of images/icons provided alongside this txt file to get you started. There is also a premade config.bin file that you can load as an example. <br>
Place your config.bin file onto a FAT/FAT32 formatted micro SD card, in the root directory.

### Soldering the boards
This is a simple guide and assumes you have some common sense.
The components must be soldered in a specific order, read the guide before starting.
1. Start with the six SMD buttons.
2. The SN74HC4051N chips are next, make sure you put them on the correct way round (indicated on the board).
3. Bend the pins of the Micro SD Module so that they are perpendicular to the board, then solder it on.
4. The Pro Micro should have come with some header pins, solder them to the Middle PCB but do not solder the Pro Micro on yet.
5. Now trim all the legs on the side of the Middle PCB that the screens will be placed on.
6. Now solder the screens on, ensuring that they are straight and that the buttons are NOT pressed by default.
7. Trim the legs of the top center screen so that they won't touch the Pro Micro.
8. Solder on the flashed Pro Micro.
9. Insert the Micro SD card with the config.bin file.
10. Solder the male header pins to the Top PCB.
11. Solder the female header pins to the Bottom PCB.
12. Slide the Middle PCB onto the male header pins of the Top PCB, then plug it into the female header pins of the Bottom PCB, sandwiching the Middle PCB between them. Make sure the buttons all click and behave as expected. If you connect the Top and Bottom too tightly you may find that the buttons don't depress, loosen it up a little.
13. Stick the rubber feet in the circles on the Bottom PCB.
14. Plug it into your PC and it should all be working.

### Using the Macrowave
Since the buttons are along the lower edge of the screens, which are hinged at the top, pressing the lower edge of the screens will be easier.
You don't need to remove the Micro SD card to update the configuration; the Settings in the configurator allow you to read and write to the SD card.
