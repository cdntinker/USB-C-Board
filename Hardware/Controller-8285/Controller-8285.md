# Notes:

**WIP**

By default, power for this board is provided on pin 1 of J1.  This is provided from the Programmer Board when flashing the ESP or, possibly, also if communicating with the ESP over USB.

To make this board work without the Programmer board, Ensure that Vsec is 3v3 (i.e.: from the PD Board) & bridge JP1. Note that this will feed 3v3 to J1 instead of pulling power from it.

# Connectors & Jumpers:

| Connector | Purpose                                         | Notes                         |
| --------- |:-----------------------------------------------:| ------------------------------|
| J1        | Programming connections (from Programmer Board) |                               |
| J2        | USB 2.0 pass through                            |                               |
| J3, J4    | PD/POE output voltage                           | Not actually used here        |
| J5, J6    | Secondary output voltage                        | See jumper JP1                |
| J7        | SPI Connection                                  |                               |
| J9        | I2C connection                                  |                               |
| J10       | Antenna connector                               | in case WiFi is actually used |

| Jumper    | Purpose                            | Notes                                       |
| --------- |:----------------------------------:| --------------------------------------------|
| JP1       | Connect Vcc (3v3) to Vsec (J5, J6) | Do NOT bridge unless Vsec is set up for 3v3 |

# TBD:

Indicator LEDs might be handy...

Should see if it'd be usefull to break out any GPIO from the ESP...

* Extra signals to/from the PD Board
  * PD_RESET
  * PD_ALERT
  * PD_ATTACH
  * PD_POWER_OK2
  * PD_POWER_OK3
  * PD_GPIO
* Maybe indicator LED(s)

For now, each of the PD_*** signals are simply connected to GPIO on the ESP.  More research will determine if this is a good idea or not.

# Rabbit Holes:

One interesting thought that this layout brings up...

This board COULD be used as a general purpose ESP module this way. (Just by repurposing the signals on J7)
