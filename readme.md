# Arduboat
Despite all the really good videos and notes on the Internet, I have yet to find a single, 
idiot's guide to building an Autonomous Surface Vehicle. 
This repo contains all notes and code for the Arduboat based ASV.
Apart from being a central repo, this material is mostly public domain.
Please treat it as licensed to Creative Commons (CC BY 4.0).
If you copy or share the information, you must attribute it to its source (here!).

A bill of material (BOM) will only be completed when an alpha vessel first sets sail.

In Ireland, we prefix Long Eireannach (LE) to the name of a boat, 
in the same way as the English use HMS and the Americans use (USS).

**LE Tupperware** is the REV 0.0 frame and no expense has been spared in its engineering. 

![](Tupperware1.jpg)

## Subsystems
Go back to manufacturer's documentation in every case.
The notes below are mostly the "gotchas", those things that are not obvious until you start the build.

### 1. Cube
1. Place the Cube on its carrier board.
   Ensure the Cube has an SDCard installed, mine came with a 16GB card preinstalled.
2. Install Mission Planner on a new W10 VM, I am using VMWare Workstation, works fine.
3. Plug the USB cable into the host laptop.
4. In VMWare, link the device to the VM.

### 2. Control PC and Mission Planner
Do NOT connect yet, just make sure the port is detected.
When you power up, the red LED flashes rapidly.

1. Settings -> Install Firmware -> Rover (works for boat as well).
   When you are programming (c. 5 mins) the red LED on the cube is constant.
   If the bleeper is attached, it warbles when complete.
2. Unplug the unit briefly, then plug back in. 
   The unit warbles.
   My unit came up on a new COM port.
   I press connect and it does.
3. After this, the menus etc. work fine, you can continue to configure.
4. The Setup->Frame Type does not give a boat option!!
   Config->Full Parameter Tree->FRAME_CLASS and set to 2, then Write Params.
5. Go to Setup->Mandatory Hardware->Accel Calibration and go through the Calibrate Accel procedure. 
   The result is not intuitive, banking seems reversed, but this is correct (think about it!!).
6. The Cube Purple does not have a working compass chip, it is disabled. 
   You will either need a compass in the GNSS, or you will add a compass board later.

### 3. GNSS
The cables which come out-of-the-box with the cube are JST-GH type, 4 and 6 pin for the GNSS.
Unfortunately, the Sparkfun boards only have a QWIK connector output and I have not found a conversion cable.
For the moment, I have not tested any cable-kludging.
The Ardusimple boards have a JST connector natively and I will be testing them real soon.
The menus do mention UBX ZED-9P but do not mention the ZED-9R. 
Both options still to be tested.

### 4. Blue Robotics Components
A basic kit has been purchased and assembled with a motor controller, all the instructions are included.
There is no independent PSU for 5VDC equipment, a power adapter needs to be separately purchased.
The power adapter cables also need to be ordered separately.

### 5. On board computer
A RPi 4B will be connected to the system eventually, work-in-progress (WIP).

