# Connectors & Jumpers:

| Connector | Purpose              | Notes  |
| --------- |:--------------------:| ------:|
| J1        | USB-C (From supply)  |        |
| J2        | USB 2.0 pass through |        |
| J3, J4    | Available Vout       |        |
| J3, J4    | Vsec supplied by U2  |        |

| Connector | Purpose                       | Notes  |
| --------- |:-----------------------------:| ------:|
| JP1       | Connect Vout directly to Vusb | really just for using the board without the PD parts |
| JP2-JP4   | For disconnecting I2C pullups | cut all 3 links to eliminate I2C pullups |
| JP5       | For setting I2C address       |        |

# TBD:

Need to find a spot for another LED...

Driven by VBUS_EN_SNK (pin 16) to indicate when Vout is enabled.

Not entirely certain that D7-D10 are useful...
