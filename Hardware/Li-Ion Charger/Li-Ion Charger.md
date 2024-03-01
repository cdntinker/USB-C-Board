# Notes:

Based on battery charger by Austins Creations

# Connectors & Jumpers:

| Connector | Purpose                                             | Notes                         |
| --------- |:---------------------------------------------------:| ------------------------------|
| J2        | USB 2.0 pass through (from PD Board or Hub)         | Pass thru (except power...)   |
| J3, J4    | PD output voltage (from PD Board)                   | Pass thru                     |
| J5, J6    | Secondary output voltage (from PD Board)            | Pass thru                     |
| J7        | SPI connection                                      | Not actually used here        |
| J9        | I2C connection                                      |                               |
| J10       | Output for load                                     |                               |
| J11       | For connection to BMS board                         |                               |

| Jumper    | Purpose                                | Notes                                      |
| --------- |:--------------------------------------:| -------------------------------------------|
| JP1       | Connect Vload to the Vsec connectors   |                                            |
| JP2       | Connect Vload to the Vout connectors   |                                            |

# TBD:

J10 either on this board or the BMS board needs to change to something different.
