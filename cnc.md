# Installation

## RPi

* Replace the SD-card with a USB-stick
* Powerup
* Choose the Internet installation option in the boot

## Arduino IDE

* sudo apt install arduino

## GRBL

* Clone https://github.com/gnea/grbl
* Open Arduino IDE
* Go to Sketch > Include Library > Add Zip Library
* Navigate to the grbl-folder in the cloned repo and click “Open”
* Edit the HOMING_CYCLE-macros in grbl/config.h, e.g.:
```
      #define HOMING_CYCLE_0 (1<<X_AXIS)                 // REQUIRED: First move Z to clear workspace.
      //#define HOMING_CYCLE_1 ((1<<X_AXIS)|(1<<Y_AXIS)) // OPTIONAL: Then move X,Y at the same time
```
* Connect to Arduino with USB
* Go to File > Examples > grbl > grblUpload
 
https://www.diyengineers.com/2023/01/05/grbl-with-arduino-cnc-shield-complete-guide/

## UGS

* Follow https://universalgcodesender.com/installing/
* In UGS, go to Machine > setup-wizard to set GRBL, 115200 Baud, and port
* 

# Calibration

## Vref of stepper motor driver

* https://www.zyltech.com/arduino-cnc-shield-instructions/
 https://thinkrobotics.com/blogs/learn/complete-cnc-shield-v3-tutorial-setting-up-grbl-for-arduino-cnc-control
