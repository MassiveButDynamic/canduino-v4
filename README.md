# CANdunio v4

Here you can find a tutorial how to get started with your CANduino `v4`. Please make sure that you really use the `v4`, because on `v3` the CS_Pin was `CS_Pin 8`!

If you don't have a CANduino yet, you can buy one here: https://canduino.de

On the new CANduino v4, the CAN controller and CAN transceiver are in one chip, the MCP25625, which contains both the MCP2515 and MCP2551.

## Getting started

Before we can start with the program it is important to check if the jumper `CAN_CS` (on top next to the USB-C port) is connected to a soldering point. Only if this is connected, it is possible to address the mcp2515.

The following library must be installed before use: https://github.com/autowp/arduino-mcp2515/archive/master.zip

If your CANduino is at the end of the CANbus chain, it is mandatory to connect the CAN_T jumper (next to the CAN connector)!

## Important parameters

So that the mcp2515 can be addressed it is important to set the following parameters:
```
MCP2515 mcp2515(10);
mcp2515.setBitrate("Your Bitrate", MCP_8MHZ);
```

Please note that the CAN controller uses the pins D2, D10, D11, D12 and D13 and that these can accordingly not be used or only to a limited extent when the CAN bus is active!

## Example Code

In the `examples` folder you will find two code examples with which you have the possibility to `send` and `receive` CAN messages.

## Troubleshooting

If the CANduino is not displayed, please download the driver for the CP2102 which can be found here: https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers?tab=downloads

## Dimensions and Pinout

Here you can find the Dimensions and the pinout of the CANduino v4:
![Pinout](/CANduino_v4_Sub_komp.png)