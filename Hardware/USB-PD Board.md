# Notes:
## U1 - STUSB4500 Standalone USB PD Sink Controller

(This chip and all of its support circuitry can be left off & then you can bridge JP1 and stuff R1 & R2 to treat the USB source as a standard 5V USB source.)

## U2 - R1501xxxxB Series LDO regulator

This chip is available in a wide range of output voltages.  Therefore, Vsec CAN be configured for anything from 3V to 18V.

In most configurations, the 3v3 version (R1501J033B) will be used...

# Connectors & Jumpers:

| Connector | Purpose                        | Notes            |
| --------- |:------------------------------:| -----------------|
| J1        | USB-C (From supply)            |                  |
| J2        | USB 2.0 pass through           |                  |
| J3, J4    | PD output voltage              | controlled by U1 |
| J5, J6    | Secondary output voltage       | controlled by U2 |
| J7        | Connection to Controller Board |                  |

| Jumper    | Purpose                       | Notes                                                |
| --------- |:-----------------------------:| -----------------------------------------------------|
| JP1       | Connect Vout directly to Vusb | really just for using the board without the PD parts |
| JP2-JP4   | For disconnecting I2C pullups | cut all 3 links to eliminate I2C pullups             |
| JP5       | For setting I2C address       |                                                      |

# TBD:

Need to find a spot for another LED...

Driven by VBUS_EN_SNK (pin 16) to indicate when Vout is enabled.

Not entirely certain that D7-D10 are useful...

## 2023/10/03
Removed ATTACH, POWER_OK2, POWER_OK3, & ALERT from J7
