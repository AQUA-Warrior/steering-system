## Custom Steering + Throttle/Brake System & Devboard

> *If You Want Total Control, You Have To Make It Yourself*

### Project Overview:
A custom, embedded hardware project to make my very own sim racing steering wheel and pedal systems. The project is powered by the STM32F732RET6 chip, using hall effect sensors for measuring inputs of the steering, throttle, and braking.

### Purpose Of The Project:
I started making this project knowing basically nothing about communication protocols or chip architectures. Instead of buying adapters that are already made for you. I wanted to make the entire system myself to learn and expand my knowledge, and create my very own sim racing setup. By designing this myself, I learned the strengths and weaknesses of communication protocols and which ones were best for which purpose. I wired up all the unused GPIO pins on the chip to connectors so that I would not just be locked down to the steering project, but instead, I can use it as a general purpose devboard for any future embedded hardware project I want to do.

### The Repository Contains:
- KiCad schematics and PCB's for the devboard and AS5048A adapter board.
- STM32CubeMX pinouts for the devboard.
- This repository will in the future contain the firmware/software.

### Main Board Hardware:
- **Chip:** STM32F732RET6 (64-pin)
- **Power:** 5V VBUS from the USB-C, regulated to 3V3 using an AP2112k

### Main Board Design:
- 2 Layer PCB
- Minimum component size of 0603 used
- Two mounting holes (One on top right, One on bottom left)
- GND Zone on front copper
- 3V3 Zone on back copper

### AS5048A Adapter Board Design:
- 1 Layer PCB
- Minimum component size of 0603 used
- Two mounting holes (One on top right, One on bottom left)
- GND Zone on front copper

## Visuals
### Main Board Schematic:
![main_schematic](https://cdn.hackclub.com/01a0201b-5359-7b5e-8d5f-06099dfe507c/image.png)

### Main Board PCB:
![main_PCB](https://cdn.hackclub.com/01a0201c-5ef3-77aa-8cbb-06e0476cf43d/image.png)

### Main Board 3D View:
![main_3D](https://cdn.hackclub.com/01a0201c-c2e5-71db-bde9-a216448ff4d2/image.png)

### AS5048A Adapter Board Schematic:
![AS5048A_schematic](https://cdn.hackclub.com/01a02019-a744-7b51-99f2-b1c21325ee12/image.png)

### AS5048A Adapter Board PCB:
![AS5048A_PCB](https://cdn.hackclub.com/01a0201a-e6cf-70c7-ba38-2d6a8c5d4a4e/image.png)

### AS5048A Adapter Board 3D View:
![AS5048A_3D](https://cdn.hackclub.com/01a0201f-c08a-7a5c-80c7-2277388eb9a6/image.png)