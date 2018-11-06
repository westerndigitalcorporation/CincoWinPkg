# README

The original [cinco](https://github.com/sifive/cinco) repo allows to program Freedom E300 boards using the Arduino IDE on **Linux** and **MacOS** only.

In this package, we enabled HiFive1 Arduino support on **Windows**, switched from 32-bit to 64-bit toolchain, made several Arduino core code improvements and optimizations (tuning clocks and delays accuracy, stack and code size, interrupts, OpenOCD) and enabled HiFive1 interoperability with LCD, touch screen, SW UART, SW I2C, tone, servo and smart LED (see the “Examples for HiFive1” after installing the package).

The source code is currently hosted [here](https://github.com/westerndigitalcorporation/cinco/tree/SeptemberUpdate) with an intention to upstream it back into SiFive’s cinco repo after our next major release.

## Notes:
1. Tested with Arduino IDE 1.6.12 - 1.8.7 on Windows 7 and 10.
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

1. Connect the HiFive1 board to the USB port intended to be used with the HiFive1 board. The driver will be installed on this port only. For several USB ports installation, you will need the HiFive1 boards connected to all these ports at the driver installation time.
2. Install FTDI driver for your version of Windows from [here](https://www.ftdichip.com/Drivers/VCP.htm)
2. Install HiFive1 driver [https://github.com/westerndigitalcorporation/CincoWinPkg/releases/download/v1.0/HiFive1_Driver.exe](https://github.com/westerndigitalcorporation/CincoWinPkg/releases/download/v1.0/HiFive1_Driver.exe)

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