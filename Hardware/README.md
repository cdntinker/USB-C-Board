# The NerdMage Rabbit Stack  Project

* KiCAD Customs
  * Customised symbols, footprints & 3D models for KiCAD
* 3D
  * 3D render models & such
  * (I use FreeCAD here...)
* `___`
  * a copy of USB-PD Proto tucked away to make renaming simpler
  * (rename the files inside the folder, then ***COPY*** them out to the Hardware folder)
* Early Designs
  * Just keeping some of these around for future reference...

---

* USB-PD Board
  * The Power Delivery Sink board
  * This board talks to the USB-C PD source & tells it what voltage/current is needed.
  * Options have been left in to just populate for non-PD usage as well.
  * It also contains a 3v3 regulator to either drive the controller board or supply your project.
* USB-PD Controller-8285
  * A controller to tell the USB-PD Board what to request from the source.
  * (This one could also become a general usage ESP board... hhhmmm...)
* USB-PD Proto
  * Just a blank board with footprints in place to match up with the others.
* USB-PD Programmer
  * A CH340-based programmer board intended to sit on top of _USB-PD Controller-8285_ using pogo pins
  * Of course, if you want a more permanent connection, you _could_ populate pins & headers instead of pogos...
* Ethernet
  * SPI Ethernet connectivity based on the W5500 chip
* Ethernet-S
  * A placeholder board to make space in the stack for Ethernet jack

There will, from time to time, appear more boards...

# Some notes about J7
(Yes, I know that J7 on all the boards is a bit of a mongrel...  Workin' on that...)

The purpose of J7 was initially to provide extra control signals between the PD board & the controller board.  As the PD board is managed via I2C, this may be un needed.

If so, then the connector should be available for SPI.  (ATM, The Ethernet board is using it as such.)

# Notes
## 2023/09/26
Reworked *EVERYTHING* to 1.27mm headers & sockets to make stacking actually work.
