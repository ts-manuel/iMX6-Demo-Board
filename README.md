# i.MX6 Demo Board
![iMX6 Demo Board-01.png](</kicad/images/TOP.png>)


<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#about-the-project">About The Project</a></li>
    <li><a href="#hardware-specifications">Hardware Specifications</a></li>
    <li><a href="#software">Software</a></li>
    <li><a href="#schematic">Schematic</a></li>
  </ol>
</details>


<!-- ABOUT THE PROJECT -->
## About The Project
This repository contains the design files and documentation for a custom-built Linux demo board based on the NXP i.MX6ULL (900 MHz ARM Cortex-A7). The purpose of this project isn't to solve a specific problem or build a commercial product. This is a dedicated learning platform designed to bridge the gap between simple micro-controllers and complex application processors. While micro-controllers (like STM32 or ESP32) are great for real-time tasks, application processors are better suited for "heavy lifting" and high-level software stacks. Checkout the full schematic [schematic](./kicad/schematic/iMX6%20Demo%20Board.pdf) and the [interactive BOM](./kicad/bom/ibom.html).

### Hardware Specifications
- **System**
    - CPU: NXP i.MX6ULL @ 900 MHz (ARM Cortex-A7)
    - RAM: 512 MB DDR3
- **Storage:**
    - 4 GB eMMC (On-board)
    - 32 MB NOR Quad SPI
    - Micro SD-Card Slot
- **Connectivity:**
    - 1x 100Mb Ethernet
    - 2x USB 2.0 Host (Type A)
    - 1x USB 2.0 Device (Type C)
    - 2x Audio Jacks 3.5 mm (WM8904 Codec)
- **UI & Indicators:**
    - 24-bit LCD Interface
    - 8x User LEDs + 5x Status LEDs

<!-- SOFTWARE -->
## Software
The current goal is to compile a basic Linux image using the Yocto Project to exercise and validate every hardware feature on the board (Ethernet, USB, Display, and GPIO).\

**Status: In Progress**. Development of the custom meta-layer and bitbake recipes is currently underway.


<!-- SCHEMATIC -->
## Schematic
Checkout the full [schematic](./kicad/schematic/iMX6%20Demo%20Board.pdf) in PDF.

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