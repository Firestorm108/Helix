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
