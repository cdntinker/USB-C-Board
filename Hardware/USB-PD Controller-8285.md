# Notes:

**WIP**

# Connectors & Jumpers:

| Connector | Purpose                                             | Notes                         |
| --------- |:---------------------------------------------------:| ------------------------------|
| J1        | Programming connections (from Programmer Board)     |                               |
| J2        | USB 2.0 pass through (possibly TO Programmer Board) |                               |
| J3, J4    | PD output voltage (from PD Board)                   | Not actually used here        |
| J5, J6    | Secondary output voltage (from PD Board)            | See jumper JP1                |
| J7        | Connection to PD Board                              |                               |
| J10       | Antenna connector                                   | in case WiFi is actually used |

| Jumper    | Purpose                         | Notes                                       |
| --------- |:-------------------------------:| --------------------------------------------|
| JP1       | Connect Vcc (3v3) Vsec (J5, J6) | Do NOT bridge unless Vsec is set up for 3v3 |

# TBD:

Indicator LEDs might be handy...

Should see if it'd be usefull to break out any GPIO from the ESP...

* Extra signals to/from the PD Board
  * RESET
  * ALERT
  * ATTACH
  * POWER_OK2
  * POWER_OK3
  * GPIO
* Maybe indicator LED(s)

~~Looks like I'm using up all the GPIO...  Might be worth just re-organising the board & making it neater.~~

Rabbit-Hole OCD!!!

