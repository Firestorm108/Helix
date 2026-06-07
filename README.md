# Helix

An automatic coil winding machine for high voltage transformers, electromagnetics, motors, etc. The combination of the leadscrew controlled spool holder and aligning/tensioning system with the precise TMC2209 controlled stepper spinner ensures even winding across every layer.
The device aims to reduce long hours spent hand winding crappy transformers so that prototyping is quick and efficient. The all-in-one control board has integrated stepper drivers and hooks up to the LCD/rotary encoder based control panel. 
It is easily reprogrammable with USB-C. With a small <75mmx75mm footprint, it fits nicely into the enclosure.

## Main Features 

- Automatic alignment
- Software defined sensing
- High speeds and precision
- Easy reprogrammability + control panel
- Small, portable design
- Custom control board
- Anti-overlap protection


# Pictures
<img width="753" height="598" alt="Screenshot 2026-06-07 at 9 40 56 AM" src="https://github.com/user-attachments/assets/9f01b04a-d27b-49b6-bac1-96963a41846c" />
<img width="1326" height="1307" alt="Screenshot 2026-06-07 at 9 41 41 AM" src="https://github.com/user-attachments/assets/3f6f79e5-4971-4fa7-9088-c4483005cb4e" />


# Helix BOM

## Electronics

| Item                                           |  Cost |
| ---------------------------------------------- | ----: |
| JLCPCB + Assembly (2 PCBs)                     |   $80 |
| Pin Headers                                    | $3.00 |
| 2x1 Screw Terminals                            |    $3 |
| DC Barrel Jack                                 |    $2 |
| White LCD w/ I2C                               |    $4 |
| Rotary Encoder                                 |    $4 |
| 3× TMC2209 Drivers                             |    $9 |
| 2× Stepper Motors                              |   $12 |
| 24V 5A Power Supply                            |   $13 |
| USB-C Power Transfer Board                     |    $2 |
| LM7805 Voltage Regulator                       |    $2 |
| Backup Devboard *(in case of PCB failure)*     |    $3 |
| Backup 5V Regulator *(in case of PCB failure)* |    $3 |
| 330µF 35V Capacitor                            |    $3 |
| Jumpers                                        |    $4 |

## Hardware

| Item                                   | Cost |
| -------------------------------------- | ---: |
| M3 Standoffs (10 mm)                   |   $2 |
| M2 Standoffs (6 mm)                    |   $2 |
| 8 mm M3 Screws                         |   $1 |
| 8 mm M2 Screws                         |   $1 |
| TO-220 Heatsink                        |   $2 |
| 300 mm 2020 Aluminum Extrusions        |  $14 |
| 150 mm 2020 Aluminum Extrusions        |  $19 |
| Corner Brackets                        |  $20 |
| 5 mm → 8 mm Couplers (2×)              |   $5 |
| 250 mm 8 mm Rod                        |   $5 |
| 608 Bearings                           |   $7 |
| 250 mm T8 (2 mm Lead) Leadscrew w/ Nut |   $9 |
| M5 20 mm Thumbscrew                    |   $3 |
| 1 mm × 8 mm Spring                     |   $4 |

## Cost Summary

| Category    |     Cost |
| ----------- | -------: |
| Electronics |     $147 |
| Hardware    |      $94 |
| **Total**   | **$241** |
