# ATARI SXEGS Cartridge

![Grey Cartridge with Red Logo.jpg](photos/Grey%20Cartridge%20with%20Red%20Logo.jpg)

## Cartridge board and Housing for [ATARI 65XE/130XE/800XE/XEGS/1200XL/800XL/600XL/800/400](https://en.wikipedia.org/wiki/Atari_8-bit_family) 8-bit computers based on [SST39SF040](https://www.microchip.com/en-us/product/SST39SF040) CMOS multi-purpose **Flash memory** chip.

- This is a **[S/XEGS type cartridge](https://forums.atariage.com/topic/276194-switchable-xe-game-cartridges-swxegs-andor-sxegs/)** that allows you to store and run dozens of games.
- The project **does not use** programmable logic chips such as [GAL-chips](https://en.wikipedia.org/wiki/Generic_array_logic).
- Only conventional logic chips are used, such as **74LS00N**, **74LS74N** and **74LS374N**.
- In the process of manufacturing a cartridge, microchips of Russian production can be used, such as **ЭКР1533ИР23**, **К555ТМ2**, **К555ЛА3** etc.

![Cartridge Circuit](photos/Cartridge%20Circuit.png)

The ROM files for the cartridge are created from the XEX files using the [CreaXin1](http://chomikuj.pl/ccwrc/users/XEGS/x_angel_ccwrc_atari_custom_cart,6059920787.7z(archive)) utility,
and then merged using the [XEGS Merger](http://chomikuj.pl/ccwrc/users/XEGS/x_angel_ccwrc_atari_custom_cart,6059920787.7z(archive)) to combine four files into one, forming a total of **512 kb of ROM** memory.

The cartridge body consists of two 3D-printed parts. The parts connect to each other without the use of screws or glue.

Files:
- ***[XEGS Cartridge_2022-11-28.zip](XEGS%20Cartridge_2022-11-28.zip)*** - archive with Gerber files for PCB manufacturing
- ***[ATARI-Cartridge-v3-Body.stl](ATARI-Cartridge-v3-Body.stl)*** - 3D-model of cartridge housing body
- ***[ATARI-Cartridge-v3-Cover.stl](ATARI-Cartridge-v3-Cover.stl)*** - 3D-model of cartridge housing cover

**[Ready to order project on PCBWay here](https://www.pcbway.com/project/shareproject/ATARI_8bit_SXEGS_Cartridge_Shrinked_Version_2022_11_10_3705ed31.html)**

The following DIP chips are required to build a cartridge:
- SST39SF040 DIP32 (1pcs)
- 74LS374N (or ЭКР1533ИР23) DIP20 (1pcs)
- 74LS74N (or К555ТМ2) DIP14 (1pcs)
- 74LS00N (or К555ЛА3) DIP14 (1pcs)

And the following SMD 1206 parts are required to build a cartridge:
- 100 nF capacitors (3 pcs)
- 6.8 uF capacitor (1 pcs)
- 11 kOhm resistors (6 pcs)
- 3.3 kOhm resistor (1 pcs)

Optional: Round Hole IC Socket Connector DIP32 (1pcs) for SST39SF040.

And you need the ability to program the [SST39SF040](https://www.microchip.com/en-us/product/SST39SF040) Flash ROM, of course. Some sort of programmer like TL866II, or something else.

To make a cartridge body, you need the ability to print models on a 3D printer. The model of the cartridge case and its cover is attached.

![Cartridge Model](photos/Cartridge%20Model.png)

When assembling the case, no additional fasteners, screws or glue are required. The case cover simply snaps into the body of the case, securing the PCB.

Instructions for creating a binary firmware file to flash in SST39SF040:
1. Download [CreaXin1](http://chomikuj.pl/ccwrc/users/XEGS/x_angel_ccwrc_atari_custom_cart,6059920787.7z(archive)) utilities and unpack it.
2. Use '***Creaxin1.exe***' utility from 'CreaXin1' folder to create ***128 kB image file***. Add XEX files to fill 128 kB ROM space and save as 'Xin1 SXEGS cartridge ROM' file.
3. Repeat step 2 ***four times*** to create four 128 kB images with different XEXs.
4. Use '***XEGS merger.exe***' utility from 'XEGS merger' folder to merge four 128 kB images into one ***512 kB image***. Add four 128 kB ROM images, choose 512 kB FLASH SIZE and press 'Create' button.
   Enter name of the new SXEGS ROM file and save it.
5. ***Flash 512 kB ROM image*** into SST39SF040. Erase ROM chip, write image and verify it.
6. Place the written chip in round hole IC socket or solder it into PCB.

[![Grey Cartridge with Red Logo in ATARI](photos/small/Grey%20Cartridge%20with%20Red%20Logo%20in%20ATARI.jpg)](photos/Grey%20Cartridge%20with%20Red%20Logo%20in%20ATARI.jpg)
[![Black Cartridge](photos/small/Black%20Cartridge.jpg)](photos/Black%20Cartridge.jpg)
[![Grey Cartridge with Red Logo](photos/small/Grey%20Cartridge%20with%20Red%20Logo.jpg)](photos/Grey%20Cartridge%20with%20Red%20Logo.jpg)
[![Assembled PCB 2](photos/small/Assembled%20PCB%202.jpg)](photos/Assembled%20PCB%202.jpg)
[![PCB Model](photos/small/PCB%20Model.png)](photos/PCB%20Model.png)
[![PCB Model in Housing](photos/small/PCB%20Model%20in%20Housing.png)](photos/PCB%20Model%20in%20Housing.png)
[![PCB Dimensions](photos/small/PCB%20Dimensions.png)](photos/PCB%20Dimensions.png)
[![Blue PCB Closer](photos/small/Blue%20PCB%20Closer.jpg)](photos/Blue%20PCB%20Closer.jpg)
[![Blue PCB and Housing](photos/small/Blue%20PCB%20and%20Housing.jpg)](photos/Blue%20PCB%20and%20Housing.jpg)
[![Cartridge Housing Body](photos/small/Cartridge%20Housing%20Body.png)](ATARI-Cartridge-v3-Body.stl)
[![Cartridge Housing Cover](photos/small/Cartridge%20Housing%20Cover.png)](ATARI-Cartridge-v3-Cover.stl)
[![Cartridge PCB](photos/small/Cartridge%20PCB.png)](ATARI-Cartridge-v3-PCB.stl)
[![Games Sample](photos/small/Games%20Sample.png)](photos/Games%20Sample.png)

© prcoder, 2022
