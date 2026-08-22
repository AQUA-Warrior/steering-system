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

## Bill Of Materials:

### Main Board:

| # | Reference | Qty | Value | Manufacturer | Manufacturer Part # | Footprint | Description | Price (1 Component) | Link |
|---:|---|---:|---|---|---|---|---|---:|---|
| 1 | F1 | 1 | Polyfuse | YAGEO | SMD0603B050TF | `Fuse:Fuse_0603_1608Metric_Pad1.05x0.95mm_HandSolder` | Resettable fuse, polymeric positive temperature coefficient | $0.36 | [DigiKey](https://www.digikey.ca/en/products/detail/yageo/SMD0603B050TF/15212923) |
| 2 | SW2 | 1 | SW_SPDT | Wurth Elektronik | 4.5E+11 | `450406020024:450406020024` | 9.0 × 3.5 mm, SPDT, ON-ON, Pitch 2.5 mm, Vertical type, SMT, T&R | $2.51 | [DigiKey](https://www.digikey.ca/en/products/detail/w%C3%BCrth-elektronik/450406020024/26249501?s=N4IgTCBcDaICwFYAMckDYliZuIC6AvkA) |
| 3 | D1 | 1 | RED | Wurth Elektronik | 150060RS75000 | `LED_SMD:LED_0603_1608Metric_Pad1.05x0.95mm_HandSolder` | Light emitting diode | $0.15 | [DigiKey](https://www.digikey.ca/en/products/detail/w%C3%BCrth-elektronik/150060RS75000/4489901) |
| 4 | U2 | 1 | USBLC6-2SC6 | Shenzhen Slkormicro Semicon Co., Ltd. | USBLC6-2SC6 | `Package_TO_SOT_SMD:SOT-23-6` | Very low capacitance ESD protection diode, 2 data-line, SOT-23-6 | $0.18 | [DigiKey](https://www.digikey.ca/en/products/detail/shenzhen-slkormicro-semicon-co-ltd/USBLC6-2SC6/28143029) |
| 5 | U1 | 1 | STM32F732RET6 | STMicroelectronics | STM32F732RET6 | `Package_QFP:LQFP-64_10x10mm_P0.5mm` | STMicroelectronics Arm Cortex-M7 MCU, 512KB flash, 256KB RAM, 216 MHz, 1.7–3.6V, 50 GPIO, LQFP64 | $15.43 | [DigiKey](https://www.digikey.ca/en/products/detail/stmicroelectronics/STM32F732RET6/6621779?s=N4IgTCBcDaIMoBUCyBmMAxA7GgSgUQQDYQBdAXyA) |
| 6 | R4 | 1 | 100 | Panasonic Industry | ERJ-PA3F1000V | `Resistor_SMD:R_0603_1608Metric_Pad0.98x0.95mm_HandSolder` | Resistor | $0.24 | [DigiKey](https://www.digikey.ca/en/products/detail/panasonic-industry/ERJ-PA3F1000V/5035847) |
| 7 | R2, R3 | 2 | 5.1k | Panasonic Industry | ERJ-3GEYJ512V | `Resistor_SMD:R_0603_1608Metric_Pad0.98x0.95mm_HandSolder` | Resistor | $0.10 | [DigiKey](https://www.digikey.ca/en/products/detail/panasonic-industry/ERJ-3GEYJ512V/135918) |
| 8 | R1 | 1 | 10k | Panasonic Industry | ERJ-3EKF1002V | `Resistor_SMD:R_0603_1608Metric_Pad0.98x0.95mm_HandSolder` | Resistor | $0.10 | [DigiKey](https://www.digikey.ca/en/products/detail/panasonic-industry/ERJ-3EKF1002V/196066?s=N4IgTCBcDaIKICUBSBaAzHA0gMQIwAZ8wA1EAXQF8g) |
| 9 | FB1 | 1 | 120R | Murata Electronics | BLM18AG121SN1D | `Inductor_SMD:L_0603_1608Metric_Pad1.05x0.95mm_HandSolder` | Ferrite bead | $0.16 | [DigiKey](https://www.digikey.ca/en/products/detail/murata-electronics/BLM18AG121SN1D/584222?s=N4IgTCBcDaIEIBkCyBGAHAQQOIrCgygHIoAiIAugL5A) |
| 10 | C16 | 1 | 2.2uF | Murata Electronics | GRT188R61H225KE13D | `Capacitor_SMD:C_0603_1608Metric_Pad1.08x0.95mm_HandSolder` | Unpolarized capacitor | $0.20 | [DigiKey](https://www.digikey.ca/en/products/detail/murata-electronics/GRT188R61H225KE13D/5416754?s=N4IgTCBcDaIOICUAqBGAHGhA2FAJMYArANICiKAzACIgC6AvkA) |
| 11 | C11, C12 | 2 | 10pF | Murata Electronics | GCM1555C1H100JA16D | `Capacitor_SMD:C_0603_1608Metric_Pad1.08x0.95mm_HandSolder` | Unpolarized capacitor | $0.11 | [DigiKey](https://www.digikey.ca/en/products/detail/murata-electronics/GCM1555C1H100JA16D/4903546) |
| 12 | C8, C9, C14, C15 | 4 | 1uF | Murata Electronics | GRT188C8YA105KE13D | `Capacitor_SMD:C_0603_1608Metric_Pad1.08x0.95mm_HandSolder` | Unpolarized capacitor | $0.17 | [DigiKey](https://www.digikey.ca/en/products/detail/murata-electronics/GRT188C8YA105KE13D/5416719?s=N4IgTCBcDaIOICUAqBGAHGgwmgmgQRQAYBWAaQFEUBmAERAF0BfIA) |
| 13 | C7 | 1 | 10nF | Murata Electronics | GCM188R72A103KA37D | `Capacitor_SMD:C_0603_1608Metric_Pad1.08x0.95mm_HandSolder` | Unpolarized capacitor | $0.15 | [DigiKey](https://www.digikey.ca/en/products/detail/murata-electronics/GCM188R72A103KA37D/1641655) |
| 14 | C6, C17 | 2 | 10uF | Murata Electronics | GCJ21BR71A106KE01L | `Capacitor_SMD:C_0805_2012Metric_Pad1.18x1.45mm_HandSolder` | Unpolarized capacitor | $0.74 | [DigiKey](https://www.digikey.ca/en/products/detail/murata-electronics/GCJ21BR71A106KE01L/4903511) |
| 15 | C1, C2, C3, C4, C5, C10 | 6 | 100nF | Murata Electronics | GCM188L81H104KA57D | `Capacitor_SMD:C_0603_1608Metric_Pad1.08x0.95mm_HandSolder` | Unpolarized capacitor | $0.14 | [DigiKey](https://www.digikey.ca/en/products/detail/murata-electronics/GCM188L81H104KA57D/2591908?s=N4IgTCBcDaILIFcBOBDALigBAcQMJwEYAOIgGSIIAkCAGAFgGkBBAVgHYAREAXQF8g) |
| 16 | D2 | 1 | D_TVS | KYOCERA AVX | GG060305100N2P | `Diode_SMD:D_0603_1608Metric_Pad1.05x0.95mm_HandSolder` | Bidirectional transient-voltage-suppression diode | $0.45 | [DigiKey](https://www.digikey.ca/en/products/detail/kyocera-avx/GG060305100N2P/14552130?s=N4IgTCBcDaIOJwAwDZEGZEFYCMjEDkwAFEAXQF8g) |
| 17 | Y1 | 1 | 16MHz | Jauch Quartz | Q 16,0-JXS32-8-10/10-WA-LF | `Crystal:Crystal_SMD_3225-4Pin_3.2x2.5mm_HandSoldering` | Four pin crystal, GND on pins 2 and 4 | $0.61 | [DigiKey](https://www.digikey.ca/en/products/detail/jauch-quartz/Q-16-0-JXS32-8-10-10-WA-LF/8108046) |
| 18 | J1 | 1 | USB_C_Receptacle_USB2.0_14P | GCT | USB4085-GF-A | `Connector_USB:USB_C_Receptacle_GCT_USB4085` | USB 2.0-only 14P Type-C Receptacle connector | $0.91 | [DigiKey](https://www.digikey.ca/en/products/detail/gct/USB4085-GF-A/9859662?s=N4IgTCBcDaIKoGUBCAWADADgKwFoDiAYjgIIgC6AvkA) |
| 19 | U3 | 1 | AP2112K-3.3 | Diodes Incorporated | AP2112K-3.3TRG1 | `Package_TO_SOT_SMD:SOT-23-5` | 600mA low dropout linear regulator, with enable pin, 3.8–6V input voltage range, 3.3V fixed positive output, SOT-23-5 | $0.28 | [DigiKey](https://www.digikey.ca/en/products/detail/diodes-incorporated/AP2112K-3-3TRG1/4470746?s=N4IgTCBcDaIIIAcwEZlgNYFoDMA6bIAugL5A) |
| 20 | SW1 | 1 | SW_Push | Alps Alpine | SKSGACE010 | `ul_SKSGACE010:SKSGACE010_ALPS` | Push button switch, generic, two pins | $0.45 | [DigiKey](https://www.digikey.ca/en/products/detail/alps-alpine/SKSGACE010/19529157?s=N4IgTCBcDaIMoGk4HECCBhAogBgIzZAF0BfIA) |
| 21 | J8 | 1 | Conn_01x15_Socket | — | — | `Connector_PinHeader_2.54mm:PinHeader_1x15_P2.54mm_Vertical` | Generic connector, single row, 01x15, script generated | — | — |
| 22 | J7 | 1 | Conn_01x21_Socket | — | — | `Connector_PinHeader_2.54mm:PinHeader_1x21_P2.54mm_Vertical` | Generic connector, single row, 01x21, script generated | — | — |
| 23 | J6 | 1 | Conn_01x02_Socket USART2 | — | — | `Connector_PinHeader_2.54mm:PinHeader_1x02_P2.54mm_Vertical` | Generic connector, single row, 01x02, script generated | — | — |
| 24 | J4, J5 | 2 | Conn_01x03_Socket A1324LLHLT-T | — | — | `Connector_PinHeader_2.54mm:PinHeader_1x03_P2.54mm_Vertical` | Generic connector, single row, 01x03, script generated | — | — |
| 25 | J3 | 1 | Conn_01x06_Socket | — | — | `Connector_PinHeader_2.54mm:PinHeader_1x06_P2.54mm_Vertical` | Generic connector, single row, 01x06, script generated | — | — |
| 26 | J2 | 1 | Conn_01x04_Pin | — | — | `Connector_PinHeader_2.54mm:PinHeader_1x04_P2.54mm_Vertical` | Generic connector, single row, 01x04, script generated | — | — |

### AS5048 Adapter Board:

| # | Reference | Qty | Value | Manufacturer | Manufacturer Part # | Footprint | Description | Price (1 Component) | Link |
|---:|---|---:|---|---|---|---|---|---:|---|
| 1 | C1 | 1 | 100nF | Murata Electronics | GCM188L81H104KA57D | `Capacitor_SMD:C_0603_1608Metric_Pad1.08x0.95mm_HandSolder` | Unpolarized capacitor | $0.14 | [DigiKey](https://www.digikey.ca/en/products/detail/murata-electronics/GCM188L81H104KA57D/2591908?s=N4IgTCBcDaIOIGECyBGAHGgMmlAJFADACwDSAggKwDsAIiALoC%2BQA) |
| 2 | C2 | 1 | 10uF | Murata Electronics | GCJ21BR71A106KE01L | `Capacitor_SMD:C_0805_2012Metric_Pad1.18x1.45mm_HandSolder` | Unpolarized capacitor | $0.50 | [DigiKey](https://www.digikey.ca/en/products/detail/murata-electronics/GCJ21BR71A106KE01L/4903511?s=N4IgTCBcDaIOIGEBSYCMAhASgdlQQVQAYA2AaQFFDUAZEAXQF8g) |
| 3 | J1 | 1 | Conn_01x07_Socket | — | — | `Connector_PinHeader_2.54mm:PinHeader_1x07_P2.54mm_Vertical` | Generic connector, single row, 01x07, script generated | — | — |
| 4 | U1 | 1 | AS5048A | ams OSRAM AG | AS5048A-HTSP-500 | `Package_SO:TSSOP-14_4.4x5mm_P0.65mm` | Magnetic position sensor, 14-bit, PWM output, SPI Interface, TSSOP-14 | $8.80 | [DigiKey](https://www.digikey.ca/en/products/detail/ams-osram-ag/AS5048A-HTSP-500/3188615?s=N4IgTCBcDaIIIGUCsAGALADjgWgBIBUEAFbVFEAXQF8g) |

### Linear Sensor:

| # | Reference | Qty | Value | Manufacturer | Manufacturer Part # | Footprint | Description | Price (1 Component) | Link |
|---:|---|---:|---|---|---|---|---|---:|---|
| 1 | — | 1 | — | Texas Instruments | DRV5055A1QLPG | — | SEN HALL EFFECT ANLG VOLT TO92-3 | $0.77 | [Digikey](https://www.digikey.ca/en/products/detail/texas-instruments/DRV5055A1QLPG) |