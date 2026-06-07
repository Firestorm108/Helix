---
title: "Helix"
author: "Sidd"
description: "Coil Winder"
created_at: "2026-06-07"
total_time: "32 Hours"
---


# May 19th 2026: Initial CAD

I made the y axis and frame of the machine. The steppers, 750mm leadscrews, pillow bearings, and couplers were all placed. As well as the extrusions and corner brackets. This is for adjustment of pipe size and the movement of the coil throughout the length of the coil. However, I am not currently happy with the design and I also think this will be problematic to bring to open sauce. I think that it would be much better to change this to only making stuff like toroids, gate drive transformers, and especially flyback transformers. Winding entire tesla coil secondaries might not be ideal.

<img width="1363" height="818" alt="image" src="https://github.com/user-attachments/assets/8f2d57c3-3b6a-4e6f-973d-372db2493581" />

Time Spent: 4 Hours

# May 20th 2026: Motherboard Schematic

I decided to base the whole machine off the RP2040 chip, since I don't need any wireless communication and the control should be fairly simple. I started out by making the schematic for the core of the motherboard. So the flash, USB C, MCU, crystal, and caps. <img width="749" height="655" alt="Screenshot 2026-05-20 at 4 57 18 PM" src="https://github.com/user-attachments/assets/13cdf5c8-5689-4812-8f06-2ee5393f1778" />

After that I added in the two stepper drivers (both TMC2209s) and the interfacing which is just the LCD and the rotary encoder. I'm not sure what else I would need because it seems a lot of the sensing I need can be done in software using the stepper motors. Motorized tensioning could be cool but it is also something I can do without electronics and I don't want to overcomplicate an already tedious task. I'll probably sleep on it and work on this tomorrow, since it's getting late.<img width="1444" height="973" alt="Screenshot 2026-05-20 at 8 49 31 PM" src="https://github.com/user-attachments/assets/408e9aad-861c-4e89-91c8-b3e1b661dc99" />

Time Spent: 5 Hours

# May 22nd 2026: Motherboard Footprints and Layout

First, I assigned footprints to everything based on LCSC. I really hope everything is correct since if even one part fails then the whole board is down. There's not much more to this, it's just a really mundane and repetitive task.
<img width="512" height="480" alt="Screenshot 2026-05-22 at 12 57 51 PM" src="https://github.com/user-attachments/assets/7b55b72d-5cf8-4189-8f02-253d1be1bbfe" />

After that I had more fun doing the layout of the board. That took me a while due to the crazy amount of passives, but I think it's a good looking layout and I'm happy with it.
I also routed the differential pairs of the USB-C since I wanted that to the perfect before I started routing anything else.

<img width="1168" height="1149" alt="Screenshot 2026-05-22 at 10 36 47 PM" src="https://github.com/user-attachments/assets/faeddc18-997c-4dc9-a5be-d821e1a51045" />

Time Spent: 4 Hours

# May 24 2026: Finished routing!

I routed all the signal and power traces, following a rather unconventional layer stackup but I'm okay with it. 3 ground layers and one 24V layer, but it is what it is. It was very challenging to route but I'm very happy with the outcome. 
I'm like 90% certain this board is going to work, since I routed it so meticulously. I'm actually super proud since it looks kinda beautiful.

<img width="612" height="625" alt="Screenshot 2026-05-25 at 12 05 39 AM" src="https://github.com/user-attachments/assets/127b1fc9-6a63-4119-8d86-013d0aa58fe2" />

Here's the 3D image:

<img width="1303" height="1297" alt="Screenshot 2026-05-25 at 12 06 59 AM" src="https://github.com/user-attachments/assets/38bd3250-fdf3-4d60-b3fd-47f85952acec" />

Time Spent: 8 Hours

# May 25 2026 (Midnight): A problem

So after making the PCB, I realized that the microcontroller has no power source when the machine is powered by the 24V power supply. It is only powered when it is being programmed. The good news is that it only needs to be programmed once, so the USB-C port can be used for powering it after.
However, there is no inbuilt voltage regulator from 24V to 5V, and there is no space to add it in right now. So, my plan is to make a seperate PCB that handles the power.

So 24V flows in via the power supply. This is outputted on the other side into the PCB, however, there is a linear voltage regulator that bumps it down to 5V as well. This 5V goes to a power only USB C receptacle, which can plug into the board.

Here's a rough sketch:

<img width="1789" height="1078" alt="Screenshot 2026-05-25 at 12 58 07 AM" src="https://github.com/user-attachments/assets/3288265b-6e8a-4872-bbbf-0d1a12cacebf" />

First I made the schematic, nothing too complex.

<img width="1315" height="1048" alt="Screenshot 2026-05-25 at 1 14 48 AM" src="https://github.com/user-attachments/assets/29230010-8cdd-4a06-ac3a-0307da251f3e" />

Then I just made the PCB and did the footprints

<img width="1188" height="778" alt="Screenshot 2026-05-25 at 1 41 31 AM" src="https://github.com/user-attachments/assets/4aeea6fc-73ef-4fbb-bfed-681440e6c4f4" />

I made sure to do all THT since it would be a huge waste of money to get this assembled. It should be like $2 for the PCB and then a couple cents for the components.

# The Morning

I'm glad to finally be getting to the CAD. I firstly desgined the outer frame, inspired from James Albin. 

<img width="1144" height="967" alt="Screenshot 2026-05-25 at 10 28 40 AM" src="https://github.com/user-attachments/assets/8469fd93-aa62-4fd9-b174-735f541b0aa1" />

After thinking for a while and literally just staring at the screen until I came up with something that worked, I rearranged the frame a bit to accomdate better. Then, made the mechanism for spinning the coil that is being wound with a stepper motor. I made an adapter that mimics a flyback core so that the bobbin may spin well. Additionally, the mounts I made for the bearing is cool since I added a little Helix. I kinda focused a lot on covering up unnecessary stuff so that it doesn't look like a prototype.

<img width="1350" height="1057" alt="Screenshot 2026-05-25 at 11 46 03 AM" src="https://github.com/user-attachments/assets/2debddd8-1c16-47c9-b65c-186862a25a67" />

Time Spent: 5 Hours

# June 5 2026: Finishing up main mechanics

Today I added in the spooling system, which rotates back and forth on a leadscrew. This movement is constrained with a V wheel plate. So the spool rests on top, with hot swappable spool holders. It then goes through a thumbscrew compression based tensioner which feeds into the coil spinner.


<img width="1240" height="1102" alt="Screenshot 2026-06-05 at 8 45 06 PM" src="https://github.com/user-attachments/assets/ad7d925a-78a5-4f01-afbe-55ddcbe66595" />

Time Spent: 4 Hours

# June 7 2026: Electronics enclosure + finishing!
I made and mounted all the electronics in an emclosure that mounts to the frame. I would say that was the most annoying part because it was mundane and tedious but its okay because it's done now. In the morning I'll work on polishing up the repo and making a bom and stuff but im going to sleep



<img width="1259" height="1085" alt="Screenshot 2026-06-07 at 1 24 24 AM" src="https://github.com/user-attachments/assets/a827e364-02f5-4bbc-9623-392160d8db4e" />

Time Spent: 2 Hours
