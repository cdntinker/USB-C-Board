# The NerdMage Rabbit Stack  Project

* KiCAD Customs
  * Customised symbols, footprints & 3D models for KiCAD
* 3D
  * 3D render models & such
  * (I use FreeCAD here...)
* `___`
  * a copy of Prototype tucked away to make renaming simpler
  * (rename the files inside the folder, then ***COPY*** them out to the Hardware folder)
* Early Designs
  * Just keeping some of these around for future reference...

---

* USB-PD Board
  * The Power Delivery Sink board
  * This board talks to the USB-C PD source & tells it what voltage/current is needed.
  * Options have been left in to just populate for non-PD usage as well.
  * It also contains a 3v3 regulator to either drive the controller board or supply your project.
* USB-PD Board 2
  * An attempt at fixing J7... (See the notes below)
    * Switching J7 to just SPI
* USB-PD Controller-8285
  * A controller to tell the USB-PD Board what to request from the source.
  * (This one could also become a general usage ESP board... hhhmmm...)
* Prototype
  * Just a blank board with footprints in place to match up with the others.
* USB-PD Programmer
  * A CH340-based programmer board intended to sit on top of _USB-PD Controller-8285_ using pogo pins
  * Of course, if you want a more permanent connection, you _could_ populate pins & headers instead of pogos...
* Ethernet
  * SPI Ethernet connectivity based on the W5500 chip
* Ethernet-S
  * A placeholder board to make space in the stack for Ethernet jack
* Ethernet-POE-WIP
  * IEEE802.3af POE based on the Silvertel Ag9900 module
* Ethernet-POE-S
  * A placeholder board to make space in the stack for the Ag9900 module
* Random Vreg
  * Just a random voltage regulator board
* RP2040
  * Workin' on an RP2040-based controller board
* Tarduino Clone
  * An Atmega328-based controller board
  * (roughly based on an Arduino Pro-mini)
  
There will, from time to time, appear more boards...

## Some future thoughts...

* Other MCUs
* Battery Charger
* BMS
* Display driver
* Inputs...
* I/O expansion
* Audio

# Some notes about J7
(Yes, I know that J7 on all the boards is a bit of a mongrel...  Workin' on that...)

The purpose of J7 was initially to provide extra control signals between the PD board & the controller board.  As the PD board is managed via I2C, this may be un needed.

If so, then the connector should be available for SPI.  (ATM, The Ethernet board is using it as such.)

## A note about using SPI on J7
As SPI requires a separate select line (SCS) for each SPI device, this means that you can only have a single SPI device.  I am currently thinking about the idea of eliminating DEV-IO on pin 7 & designing some sort of 2-bit selection system using pins 7 & 8.

Another option might be to enforce placement of the feedthrough headers for J9 instead of copying I2C into J7.  This would give an option of a 3 or 4 bit selection system.

Must still put more thought into this...

# Notes
## 2023/09/26
Reworked *EVERYTHING* to 1.27mm headers & sockets to make stacking actually work.

## 2023/10/03
Changing J7 to dedicated I2C + SPI interface (well... Plus device reset & possibly 1 spare I/O...)
