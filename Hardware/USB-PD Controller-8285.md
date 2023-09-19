# Notes:

**WIP**

# Connectors & Jumpers:

| Connector | Purpose                                             | Notes                         |
| --------- |:---------------------------------------------------:| -----------------------------:|
| J1        | Programming connections (from Programmer Board)     |                               |
| J2        | USB 2.0 pass through (possibly TO Programmer Board) |                               |
| J3, J4    | PD output voltage (from PD Board)                   | Not actually used here        |
| J5, J6    | Secondary output voltage (from PD Board)            | See jumper JP1                |
| J7        | Connection to PD Board                              |                               |
| J10       | Antenna connector                                   | in case WiFi is actually used |

| Jumper    | Purpose                         | Notes                                       |
| --------- |:-------------------------------:| -------------------------------------------:|
| JP1       | Connect Vcc (3v3) Vsec (J5, J6) | Do NOT bridge unless Vsec is set up for 3v3 |

# TBD:

Should probably add a reset button.

Indicator LEDs might be handy...

Should see if it'd be usefull to break out any GPIO from the ESP...