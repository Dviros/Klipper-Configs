# Klipper-Configs
Just my set of configs for the Artillery Genius Pro running Klipper.

---------------------------------------------------------------------------------

### Current Klipper Converstion Project Status:
1. Artillery Genius Pro Stock - working very well
2. Artillery Genius Pro SKR3 + LGX + EBB42 - works flawlessly 
  - LGX Over extrusion, basic calibration
  - ~Linear Rails on all axis~
  - ~EBB42 1.0 on USB instead~ combined with the Genius EBB
  - ~EBB42 ADXL and Bltoutch~

---------------------------------------------------------------------------------

### My setup:
- LGX ACE Mosquito, CHT Nozzle, 24v Heating cartridge
- Bigtreetech SKR3 EZ with EZ-TMC2209 drivers
- Bigtreetech EBB42 1.0 running Klipper
- PT1000\ATC Semitec 104NT-4-R025H42G thermistors
- Linear Rails
- ADXL345 input shaper (using EBB42)
- Jetson Nano as the Moonraker\Octoprint\Mainsail server
- Antclabs Bltouch 3.1
---------------------------------------------------------------------------------

### How to flash:
I've flashed Klipper using USB even though this specific chip does not support it and should be flashed using SD Card - it didn't work for me.

At the moment, bootloader is skipped and I can't revert to Marlin - be careful if you ever want to.

Set your config to the following:

![image](https://user-images.githubusercontent.com/23431860/178116003-bf4d2adb-9c7d-4dac-b93c-876c1bf98000.png)

and use `dfu-util -a 0 -s 0x8000000:leave -D out/klipper.bin`

---------------------------------------------------------------------------------

### What did you use to enhance your printer?
Here are the relevant projects I've used - all respect goes to them!
Z Linear Rails:
- https://www.thingiverse.com/thing:4632881

X Linear Rails:
- https://www.thingiverse.com/thing:4941133/files

Rod support:
https://www.thingiverse.com/thing:5143100

Brace support:
- https://www.thingiverse.com/thing:4601974
- https://www.thingiverse.com/thing:4770873
- https://www.thingiverse.com/thing:4718116

Belt tensioners:
- https://www.aliexpress.com/item/1005001874457464.html

---------------------------------------------------------------------------------
Several considerations:
1. Original Artillery mechanical endstops do not work with the SKR3; I had to revert to the generic 2-wired endstops
2. Bltouch and Input Shaper settings needs to be defined in the printer.cfg for it to be modified by Mainsail
3. LGX current needs to be around .650 RMS to avoid skippings
