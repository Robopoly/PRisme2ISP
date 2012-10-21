# PRisme2ISP

This sketch is an adaptation of the ArduinoISP by Randall Bohn that makes an ISP programmer out of the PRisme2.

## Connection
To load the bootloader on another board or to program another board without a bootloader, such as another PRisme2, you need to connect 4 pins and the power supply.

![Alt text](http://i.imgur.com/Naru5.png)

The left board (master) loads the program on the right one (slave) via emulated SPI protocol. The reset pin on the slave has to be triggered by some other pin than the master's reset pin for obvious reasons (B0).

## Usage
Once the PRisme2ISP is loaded on the master via usual UART programming select the _Arduino as ISP_ programmer from the _Tools->Programmer_ menu in Arduino IDE. Then the board type which will be programmed (slave) from the _Tools->Board_ menu and finally _Tools->Burn Bootloader_ to load the bootloader, or simply _File->Upload Using Programmer_ to load the program directly.
