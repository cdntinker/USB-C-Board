# Notes:

**WIP** 

So far, this board has no default power.

To make this board powered from the stack, Ensure that Vsec is 3v3 (i.e.: from the PD Board) & bridge JP1.

**WIP** 

Might be handy to put a little (optional) VREG local to this board but I suspect it'd need to be smaller than the R1501 circuit used elsewhere in this project.

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