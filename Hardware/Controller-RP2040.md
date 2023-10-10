# Notes:

**WIP** 

**WIP** 

**WIP** 

# Connectors & Jumpers:

| Connector | Purpose                                         | Notes                         |
| --------- |:-----------------------------------------------:| ------------------------------|
|           |                                                 |                               |
| J2        | USB 2.0 pass through                            | The RP2040 actually runs USB! |
| J3, J4    | PD/POE output voltage                           | Not actually used here        |
| J5, J6    | Secondary output voltage                        | See jumper JP1                |
| J7        | SPI Connection                                  |                               |
| J9        | I2C connection                                  |                               |

| Jumper    | Purpose                            | Notes                                       |
| --------- |:----------------------------------:| --------------------------------------------|
| JP1       | Connect Vcc (3v3) to Vsec (J5, J6) | Do NOT bridge unless Vsec is set up for 3v3 |

# TBD:

This is JUST BARELY started