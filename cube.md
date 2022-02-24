# Autopilot
The autopilot chosen was the Cube Purple, as being "good enough" for a rover type application.

## Parts
This was ordered as a kit, Cube Purple, mini-carrier, cables.
### Cables and Connectors
Connector information can be found [here](https://docs.cubepilot.org/user-guides/carrier-boards/mini-carrier-board).
Out of the box, the signal connectors are JST-GH 1.25 pitch on the mini-carrier side. 
On the other side they are Molex DF13 4P/5P/6P. The power cables are Molex CLIK-Mate 2 mm (6-pin).

![](CubeCables.jpg)

### Telemetry
There is no telemetry link, this needs to be ordered separately.
This was ordered from 3DXr as Holybro - Telemetry Radio Set V3 - 100mw 433MHz
Code: HB-03-14-433-100mw-V3

## Installation
1. Place the Cube on its carrier board.
   Ensure the Cube has an SDCard installed, mine came with a 16GB card preinstalled.
2. Install Mission Planner (MP) on a new Windows 10 VM, I am using VMWare Workstation, it works fine.
3. Plug the USB cable into the host laptop.
4. In VMWare, link the device to the VM.

