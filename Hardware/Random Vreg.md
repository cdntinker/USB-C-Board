# Notes:
Just a random voltage regulator board

Proof of concept really...

But then again...

With the PCA9557BS I/O expander, you can control which Vrnd output(s) are on & off.

# Connectors & Jumpers:

| Connector | Purpose                                             | Notes                         |
| --------- |:---------------------------------------------------:| ------------------------------|
| J2        | USB 2.0 pass through (from PD Board)                |                               |
| J3, J4    | PD output voltage (from PD Board)                   |                               |
| J5, J6    | Secondary output voltage (from PD Board)            |                               |
| J7        | SPI connection                                      |                               |
| J9        | I2C connection                                      |                               |
| J10       | Output of Vreg0                                     |                               |
| J11       | Output of Vreg1                                     |                               |
| J12       | Output of Vreg2                                     |                               |

# TBD:

U4 relly needs to rotate 90 degrees to the left...
