# spark-debug
# Navigation
- [About project](#about-project)
  - [Motivation for the project](#motivation-for-the-project)
  - [Humorous additions](#humorous-additions)
  - [Pin tables](#pin-tables)
  - [Development tools](#development-tools)
  - [Features](#features)
- [Images](#images)
- [License](#license)

# About project

spark-devboard-rf is RF focused devboard based on ESPRESSIF ESP32-WROVER-IE-N16R8 allowing Wi-Fi b/g/n, Bluetooth 4.2 Classic and Bluetooth 4.2 BLE communication using external u.FL antena

## Motivation for the project

spark-devboard-rf was created from boreness, but also as a stepping stone before using the same module in upcoming audio player of mine

## Pin functions

Pin functions are written on back of the PCB. Alternate functions can be found in [this datasheet](https://documentation.espressif.com/esp32-wrover-e_esp32-wrover-ie_datasheet_en.pdf)

## Usage

You use it as any other developement board. Important caveats are programming and powering the board.

### Programming

You need to program this board via UART interface specified on the back side of PCB. To enter flashing mode you need to hold BOOT button during power on or resetting the board


### Powering

Board can be either powered by 5x 3.3V pins on board, where you need to supply minimum of 500 mA for board to work properly, or via USB-C power-only port on board, where the pins become 3.3V output. **It is important to make sure that you are powering the board from only one supply method at the time**

## Directory overview

- 3D file of PCB is available in `/3D`
- KiCad project files are available in `/KiCad Project Files`
- Gerber files are available in `/Gerbers`

## Development tools

- KiCad for EDA work

## Features

- ESP32 module with 8MB PSRAM and 16MB flash
- u.FL antenna slot
- USB-C port for power
- Integrated 3.3V LDO

# Images

Schematic

![schematic](/Images/Schematic.png)

PCB editor view

![pcb editor view](/Images/PCB.png)

3D viewer top side

![3d top side](/Images/3D-top.png)

3D viewer bottom side

![3d bottom side](/Images/3D-bottom.png)

# License

## PCB / Schematic License

All files in `/PCB`, `/Schematic` and `/Gerbers` folders and their subsequent subfolders are licensed under the CERN Open Hardware License v2 (Weakly Reciprocal).

See `/Licenses/CERN-OHL.txt` for full terms.

## 3D files, images and documentation License

All files in `/3D`, `/Images` and `/Docs` folders and their subsequent subfolders are licensed under the CC-BY 4.0 License.

See `/Licenses/CC-BY-4.0.txt` for full terms

# BOM

|Name                          |Purpose                 |Quantity|Total Cost (USD)|Link                                                                                                     |Distributor|
|------------------------------|------------------------|--------|----------------|---------------------------------------------------------------------------------------------------------|-----------|
|PCB                           |PCB                     |5       |2.10            |                                                                                                         |JLCPCB     |
|MOLEX 206994-0100             |Antenna for connectivity|1       |2.38            |https://www.tme.eu/pl/details/2069940100/anteny-wifi-bluetooth/molex/206994-0100/                        |TME        |
|ESP32-WROVER-E-N16R8          |MCU module              |1       |6.40            |https://www.tme.eu/pl/details/esp32-wrover-e-16/moduly-iot-wifi-bluetooth/espressif/esp32-wrover-e-n16r8/|TME        |
|SHOU HAN TYPE-C 16PIN 2MD(073)|USB-C power port        |1       |0.00            |https://www.lcsc.com/product-detail/C2765186.html?s_z=n_C2765186                                         |LCSC       |


© 2026 emb3rcia

Hardware: CERN OHL v2
3D & Images: CC BY 4.0
