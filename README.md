# i.MX6 Demo Board
![iMX6 Demo Board-01.png](</kicad/images/TOP.png>)


<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#about-the-project">About The Project</a></li>
    <li><a href="#schematic">Schematic</a></li>
    <li><a href="#u-boot">U-Boot</a></li>
    <li><a href="#known-issues">Known Issues</a></li>
  </ol>
</details>


<!-- ABOUT THE PROJECT -->
## About The Project
This is a demo board for the i.MX 6 ULL application procesor from NXP. 


### Hardware:
- NXP i.MX6ULL 900 MHz ARM Coretex-A7
- 512 MB DDR3 RAM
- 32 MB NOR QUAD SPI
- 4 GB eMMC on-board storage
- Micro SD-Card Slot
- 1x 100Mb Ethernet
- 2x USB 2.0 Host Type A
- 1x USB 2.0 Device Type C Power + FTDI (DFU)
- 8x USER LEDs
- 5x STATUS LEDs
- 24 bit LCD


<!-- SCHEMATIC -->
## Schematic
![iMX6 Demo Board-01.png](</kicad/schematic/iMX6 Demo Board-01.png>)

### POWER TREE
![iMX6 Demo Board-02.png](</kicad/schematic/iMX6 Demo Board-02.png>)

### BLOCK DIAGRAM
![iMX6 Demo Board-03.png](</kicad/schematic/iMX6 Demo Board-03.png>)

### POWER
![iMX6 Demo Board-04.png](</kicad/schematic/iMX6 Demo Board-04.png>)

### CPU
![iMX6 Demo Board-05.png](</kicad/schematic/iMX6 Demo Board-05.png>)

### RAM DDR3
![iMX6 Demo Board-06.png](</kicad/schematic/iMX6 Demo Board-06.png>)

### eMMC QSPI SD
![iMX6 Demo Board-07.png](</kicad/schematic/iMX6 Demo Board-07.png>)

### USB TYPE A
![iMX6 Demo Board-08.png](</kicad/schematic/iMX6 Demo Board-08.png>)

### ETHERNET
![iMX6 Demo Board-09.png](</kicad/schematic/iMX6 Demo Board-09.png>)

### AUDIO CODEC
![iMX6 Demo Board-10.png](</kicad/schematic/iMX6 Demo Board-10.png>)

### LCD
![iMX6 Demo Board-11.png](</kicad/schematic/iMX6 Demo Board-11.png>)

### BOOT CONFIG
![iMX6 Demo Board-12.png](</kicad/schematic/iMX6 Demo Board-12.png>)

### CONTROL GPIO
![iMX6 Demo Board-13.png](</kicad/schematic/iMX6 Demo Board-13.png>)


<!-- U-BOOT -->
## U-Boot

### Prerequisites

    > sudo apt install gcc-arm-linux-gnueabihf

### Compiling U-Boot

    > cd linux/u-boot
    > make mx6ull_demo_board_defconfig
    > ARCH=arm CROSS_COMPILE=arm-linux-gnueabihf- make


## Known Issues

### Rev. 00 - Issues found during hardware debug

+ Wrong part number in BOM for resistors R103, R113, R114, R118.\
**Suggested Fix:** Replace with 680 KΩ resistors, applying power withot the fix will damage the board!!!

+ Wrong part number in BOM for resistors R13, R16.\
**Suggested Fix:** Replace with 68 KΩ resistors, applying power withot the fix will damage the board!!!

+ Wrong part number in BOM for resistors R14.\
**Suggested Fix:** Replace with 4.7 KΩ resistors, applying power withot the fix will damage the board!!!

+ Wrong part number in BOM for capacitors C100, C101, C12, C13, C130, C131, C133, C135, C140, C141, C15, C19, C57, C58, C7, C99.\
**Suggested Fix:** Replace with 100 nF capacitors.

+ Wrong connection for power pins in USB Type A ports, power and ground are flipped.\
**Suggested Fix:** Cut metal beind connector and rewire power and ground.

+ Wrong connection for power button pull-up resistor, board will not turn on with power button.\
**Suggested Fix:** Remove R23 and connect 10 KΩ pull-up between button and +3V3_STANDBY.