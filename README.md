# README #

The original [cinco](https://github.com/sifive/cinco) repo allows to program Freedom E300 boards using the Arduino IDE on `Linux` and `MacOS` only.

This repository allows to program Freedom E300 boards using the Arduino IDE on `Windows` also.

## Notes: ##
1. Tested with Arduino IDE 1.6.12 - 1.8.5 on Windows.
2. Tested with HiFive1 board only.
3. Tested for standard and portable installations.

# Setup on Windows OS #

## Install Arduino ##

Download and install Arduino IDE tarball from the Arduino website. Unpack it and run their installation script as directed.

## Install the SiFive Boards ##

Add the [https://raw.githubusercontent.com/westerndigitalcorporation/CincoWinPkg/master/package_sifive_index.json](https://raw.githubusercontent.com/westerndigitalcorporation/CincoWinPkg/master/package_sifive_index.json)
to the Additional Boards Manager URLs in the `Preferences->Settings`.

Use the Boards Manager to search for and install the "SiFive" boards.

# Setup Your Board #

## Select the board: ##
```
Tools->Board->HiFive1
```

## Select OpenOCD as the Programmer ##
```
Tools->Programmer->SiFive OpenOCD
```

# Compile and Upload #

## Basic Example ##

Select the `File->Examples->Basics->Blink` built-in example.

Hit the "Verify" button to test the program compiles,
then "Upload" to program to your board. The green LED should blink.

## rgb_lead_fade Example ##

The example, achieves the same fade effect as in the led_fade example come with Freedom Studio.

`File->Open` and select `C:\Users\<user>\AppDAta\Local\Arduino15\packages\sifive\hardware\riscv\1.0.3\freedom-e-sdk\software\arduino\rgb_led_fade\rgb_led_fade.ino`
