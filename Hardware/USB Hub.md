# Notes:

**WIP**

U2 is maximum 6V input...  So be careful not to do higher voltage from PD.

Being configured in "Bus Powered" mode, each downstream USB should be limited to 100mA.

This particular design does NOT have overcurrent protection built in ATM...

There is no transient suppression so far either...

Pads of J11 & J12 next to mounting holes are problematic. During assembly, care must be taken to avoid solder buildup on these 2 pads to avoid interferance with mounting.

# Connectors & Jumpers:

| Connector | Purpose                                | Notes                                      |
| --------- |:--------------------------------------:| -------------------------------------------|
| J2        | Upstream USB 2.0 (From board below)    |                                            |
| J3, J4    | PD output voltage (passthrough)        | Not actually used here                     |
| J5, J6    | Secondary output voltage (passthrough) | Not actually used here                     |
| J7        | SPI connection                         | Not actually used here                     |
| J9        | I2C connection                         | Not actually used here                     |
| J10       | Downstream USB 2.0 Port 1              |                                            |
| J11       | Downstream USB 2.0 Port 2              |                                            |
| J12       | Downstream USB 2.0 Port 3              |                                            |

# TBD:

## Overcurrent Protection
Look at TPS2550 for overcurrent protection. (USB Hub2 is a version with overcurrent being implimented...)

## Transient Suppression
Maybe find space for a pair of PGB1010603s per port...

## Self Powered Mode
Would need a 5V 1500mA source. (Maybe through Vsec?)
