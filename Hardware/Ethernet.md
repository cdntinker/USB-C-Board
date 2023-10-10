# Notes:

# Connectors & Jumpers:

| Connector | Purpose                        | Notes                                  |
| --------- |:------------------------------:| ---------------------------------------|
| RJ45-1    | The Ethernet connection        |                                        |
| J2        | USB 2.0 pass through           |                                        |
| J3, J4    | PD output voltage              | Fed through from the rest of the stack |
| J5, J6    | Secondary output voltage       | Fed through from the rest of the stack |
| J7        | Connection to Controller Board | On this board: both SPI & I2C          |
| J9        | QWIIC I2C connection           | Not actually used here                 |
| J10       | VB to the POE Board            |                                        |
| J11       | VA to the POE Board            |                                        |

# TBD:

Work out the implimentation of the SPI connection.