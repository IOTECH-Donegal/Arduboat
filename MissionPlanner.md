# 2. Control PC and Mission Planner - WIP
My control PC is a modern laptop running VMWare Workstation. I installed MP on a W10 VM with 4GB and 2 CPU.

The telemetry dongle shows as a removable device, Future Devices FT230X Basic UART.
When I connect that to the VM, it shows as COM5.

Connect the Cube directly to the Laptop via USB and run Mission Planner. 
If you are doing updates, disconnect the servos and the GPS.
I got continuous clicks with the GPS connected, I think there was too much current draw for the USB.

Do NOT press the connect button in MP yet, just make sure the port is detected.
When you connect the Cube via USB, the red LED flashes rapidly.

1. In MP, **Settings -> Install Firmware -> Rover** (works for boat as well).
   When you are programming (c. 5 mins) the red LED on the cube is constant.
   If the bleeper is attached, it warbles when complete.
2. Unplug the unit briefly, then plug back in. 
   The unit warbles.
   My unit came up on a new COM port.
   I press **Connect** and it does.
3. After this, the menus etc. work fine, you can continue to configure.
4. The **Setup->Frame Type** does not give a boat option!!
   **Config->Full Parameter Tree->FRAME_CLASS** and set to **2**, then **Write Params**.
5. Go to **Setup->Mandatory Hardware->Accel Calibration** and go through the Calibrate Accel procedure. 
   The result is not intuitive, banking seems reversed, but this is correct (think about it!!).
6. The Cube Purple does not have a working compass chip, it is disabled. 
   You will either need a compass in the GNSS, or you will add a compass board later. 
   See the separate sheet on GNSS connections.
7. This boat will be Skid Steer. Go to **Setup->Mandatory Hardware->Servo Output**.
   Set channel 1 to ThrottleLeft and Channel 3 to ThrottleRight.  