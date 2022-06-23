# Boat and Submersible
Despite all the really good videos and notes on the Internet, I have yet to find a single, 
idiot's guide to building an **Autonomous Surface Vehicle (ASV)** or 
an **Autonomous Underwater Vehicle (AUV)**. 
This repo contains all notes and code for the Arduboat based ASV, the first step to an AUV.

The primary purpose for this vessel is for taking video/photgraphs for photogrammetry.
The specification is for:
- RTK positioning accuracy of c. 1cm
- Heading response at 5Hz with 0.5°
These values will need to be available as meta data for video/camera.
  
A second option is to use an INS to maintain positional accuracy under piers or in caves.

This platform can support an Airmar SS510 for hydographic survey and a transon mount transducer for seabed search.

Apart from being a central repo, this material is mostly public domain, 
please treat it as licensed to Creative Commons (CC BY 4.0).
If you copy or share the information, you must attribute it to its source (here!).
Any subsystem complete for alpha test will be marked so.
Anything else will be marked as **Work-in-Progress (WIP)** or **Not Started**.

A bill of material (BOM) will only be completed when an alpha vessel first sets sail.

In Ireland, we prefix Long Eireannach (LE) to the name of a boat, 
in the same way as the English use HMS and the USA uses USS.
**LE Tupperware** was a big plastic box and the REV 0.0 frame.
Everything was moved to an Azul Junior Basic Kayak for sea trials. 
- Length: 1850mm
- Width: 610 mm
- Height: 230mm
- Weight: 8.1kg

![](Azul1.jpg)

A (too big at 20kg!) lead-acid leisure battery was used as it was available.
It is mounted above the thrusters and the boat can rotate about its centre of gravity.
Two patch antenna sit on ground planes.

## Subsystems
Go back to manufacturer's documentation in every case.
The notes below are mostly the "gotchas", those things that are not obvious until you start the build.
Don't touch anything until you have read extensively, one wrong connection will blow components. 

### 1. Cube Autopilot - Alpha
This has been extensively tested.

[Information relating to the Autopilot](cube.md)


### 2. Control PC and Mission Planner - Alpha
Extensive testing has been completed.


### 3. GNSS with heading and Inertial Navigation System (INS) - WIP 
[Information relating to the GNSS](GNSS.md)

### 4. Blue Robotics Components - WIP
[Information relating to the thrusters and ESCs](BR.md)


### 5. On board computer - WIP
A RPi 4B will be connected to the system eventually as an onboard computer.
Early research done.

### 6. LIDAR - Not Started

### 7. Cameras suited for photogrammetry - Not Started

### 8. Single Beam Echo Sounder (SBES) - Not Started

### 9. Side Scan (SS) - Not Started

### 10. Radio Remote Control (RC) - Not Started

### 11. Charging and Batteries - WIP
The alpha version will use a monstrous lead-acid leisure battery. 
Eventually, Li-ion parts and methods will be described here.
