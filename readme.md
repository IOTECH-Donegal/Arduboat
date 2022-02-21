# Arduboat
This repo contains all notes and code for the Arduboat based ASV.

## Cube
1. Place Cube on its carrier board.
   Ensure the Cube has an SDCard installed, mine came with a 16GB card pre0installed.
2. Install Mission Planner on a new W10 VM.
3. Plug the USB cable into the host laptop.
4. In VMWare, link the device to the VM.

### Mission Planner
Do NOT connect yet, just make sure the port is detected.
When you power up, the red LED flashes rapidly.

1. Settings -> Install Firmware -> Rover (works for boat as well).
   When you are programming (c. 5 mins) the red LED on the cube is constant.
   If the bleeper is attached, it warbles when complete.
2. Unplug the unit briefly, then plug back in. The unit warbles.
   My unit came up on a new COM port.
   I press connect and it does.
3. After this, the menus etc. work fine, you can continue to configure.
4. The Setup->Frame Type does not give a boat option.
   Config->Full Parameter Tree->FRAME_CLASS and set to 2, then Write Params.
5. Go to Setup->Mandatory Hardware->Accel Calibration and go through the Calibrate Accel procedure. 
   The result is not intuitive, banking seems reversed.
6. The Cube Purple does not have a working compass chip, it is disabled.