# README

The original [cinco](https://github.com/sifive/cinco) repo allows to program Freedom E300 boards using the Arduino IDE on **Linux** and **MacOS** only.

This repository allows to program Freedom E300 boards using the Arduino IDE on **Windows** also.

## Notes:
1. Tested with Arduino IDE 1.6.12 - 1.8.6 on Windows.
2. Tested with HiFive1 board only.
3. Tested for standard and portable installations.

# Setup on Windows OS

## Install Arduino

Download and install Arduino IDE tarball from the Arduino website. Unpack it and run their installation script as directed.

## Install the SiFive Boards

Add the [https://raw.githubusercontent.com/westerndigitalcorporation/CincoWinPkg/master/package_sifive_index.json](https://raw.githubusercontent.com/westerndigitalcorporation/CincoWinPkg/master/package_sifive_index.json)
to the Additional Boards Manager URLs in the `Preferences->Settings`.

Use the Boards Manager to search for and install the "SiFive" boards.

## Install USB Driver

[https://github.com/westerndigitalcorporation/CincoWinPkg/releases/download/v1.0/HiFive1_Driver.exe](https://github.com/westerndigitalcorporation/CincoWinPkg/releases/download/v1.0/HiFive1_Driver.exe)

# Setup Your Board

## Select the board:
```
Tools->Board->HiFive1
```

## Select OpenOCD as the Programmer
```
Tools->Programmer->SiFive OpenOCD
```
## Select Serial port
```
Tools->Port->Serial ports
```
# Compile and Upload

## Basic Example

Select the `File->Examples->Basics->Blink` built-in example.

Hit the "Verify" button to test that  the program compiles,
then "Upload" to program your board. The green LED should blink.

## RGB LED fade Example

`File->Examples`, scroll down to `Examples for HiFive1` and select `RGB LED->RgbLedFade` sketch.