# The __Nerd Mage "Universal" USB-C Board__  Project

* 3D
  * 3D renders & such
* Early Designs
  * Just keeping some of these around for future reference...
* KiCAD Customs
  * Customised symbols, footprints & 3D models for KiCAD

---

* USB-PD Board
  * The Power Delivery Sink board
  * This board talks to the USB-C PD source & tells it what voltage/current is needed.
  * Options have been left in to just populate for non-PD usage as well.
  * It also contains a 3v3 regulator to either drive the controller board or supply your project.
* USB-PD Controller-8285
  * A controller to tell the USB-PD Board what to request from the source.
  * (This one has a long way to go yet...)
* USB-PD Proto
  * Just a blank board with footprints in place to match up with the others.
* USB-PD Programmer
  * A CH340-based programmer board intended to sit on top of _USB-PD Controller-8285_ using pogo pins
  * Of course, if you want a more permanent connection, you _could_ populate pins & headers instead of pogos...
