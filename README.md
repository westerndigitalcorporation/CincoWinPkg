# README

The original [cinco](https://github.com/sifive/cinco) repo allows to program Freedom E300 boards using the Arduino IDE on **Linux** and **MacOS** only.

In this package, we enabled HiFive1 Arduino support on **Windows**.

Besides, we switched from 32-bit to 64-bit toolchain, made several Arduino core code improvements and optimizations (clocks and delays accuracy, stack and code size, interrupts, OpenOCD) and enabled HiFive1 interoperability with LCD, touch screen, SW UART, SW I2C, tone, servo and smart LED (see the `Examples for HiFive1` after installing the package).

The source code is located in the [https://github.com/westerndigitalcorporation/cinco](https://github.com/westerndigitalcorporation/cinco) repo.

## Notes:
1. Tested with Arduino IDE 1.6.12 - 1.8.7 on Windows 7 and 10.
2. Tested with HiFive1 board only.
3. Tested for standard and portable installations.

# Setup on Windows OS

## Install Arduino

Download and install Arduino IDE tarball from the Arduino website. Unpack it and run their installation script as directed.

## Install the SiFive Boards

Add the `https://raw.githubusercontent.com/westerndigitalcorporation/CincoWinPkg/master/package_sifive_index.json`
to the Additional Boards Manager URLs in the `Preferences->Settings`.

Use the Boards Manager to search for and install the `SiFive` boards.

## Install USB Driver

1. Connect HiFive1 board to USB port intended to be used with the HiFive1 board. The driver will be installed on this port only. For several USB ports installation, you will need the HiFive1 boards connected to all these ports at the driver installation time.
2. Download and install HiFive1 driver [HiFive1_Driver.exe](https://github.com/westerndigitalcorporation/CincoWinPkg/releases/download/v1.0/HiFive1_Driver.exe)
3. If FTDI driver is not installed on your computer and there is an available internet connection, Windows will silently connect to the Windows Update website and install any suitable driver it finds for the device. If no suitable driver is automatically found then follow the installation procedure for your version of Windows from FTDI [site](https://www.ftdichip.com/Drivers/VCP.htm).

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

Hit the `Verify` button to test that the program compiles,
then `Upload` to program your board. The green LED should blink.

## RGB LED fade Example

`File->Examples`, scroll down to `Examples for HiFive1` and select `RGB LED->RgbLedFade` sketch.
