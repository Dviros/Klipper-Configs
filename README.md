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
Several considerations:
1. Original Artillery mechanical endstops do not work with the SKR3; I had to revert to the generic 2-wired endstops
2. Bltouch and Input Shaper settings needs to be defined in the printer.cfg for it to be modified by Mainsail
3. LGX current needs to be around .650 RMS to avoid skippings
