# busboard - bus breakout board for Arduino pro-mini
Created to allow easy prototyping of battery-powered remote sensing projects.
Designed to fit genuine (Sparkfun) boards, or most common clones.
Created using KiCad.

Features:
* SPI bus broken out for 2 devices, with optional nRF24 connector also on the bus (connected through jumpers). Default SS pin (D10) connected to nRF24 CS/SS.
* I2C/TWI bus broken out for 3 devices (with pull-up resistors).
* 4 analog pins broken out with separate ground plane.
* Digital pins broken out (but note - using non-standard pin pitch).
* 5cm x 5cm form factor; mounting holes for 3 M3 stand-offs with 4cm pitch, connected to ground plane to support shielding (but note nRF24 antenna must remain outside shielding).

# Power
Optional connector for Pololu drop-down regulators (4-pin). Battery connected through switch and a resistor divider for battery voltage measurement (on pin A7).
SHDN pin connected (through jumper) to D7 (but can be left floating on these devices).
If another regulator is used (including the built-in regulator), solder a jumper wire from RAW pin on Pololu connector to RAW pin on the pro-mini.

# Analog pins
* A0-A3 - broken out to analog section (with a separate ground plane connected at a star point)
* A6 - available but not broken out
* A7 - connected to battery (through resistor divider)
* A4-A5 are shared with I2C on Pro-minis.

# nRF24 connector (with 3.3v Pro-minis)
SPI pins (MOSI/MISO/SCLK) connected through solder jumpers (to reduce EMI when not used).
SS connected (through jumper) to D10.
IRQ connected (through jumper) to D3.
CE/EN connected (through jumper) to D8.

# RX/TX
Broken out.

# FTDI header
Not broken out (should be available directly on Pro-mini board depending on the headers used).

# TODO (in next revision)
* Add jumper to bypass DC-DC converter module and connent batt. RAW to board RAW.
* Add second power switch footprint (for a 2.54mm-pitch switch)
* Move the power switch footprint closer to the edge of the board
* Change power switch footprint to have slightly larger diameter outer mounting holes
* Increase the width of the traces of the RAW network (the existing width should be more than sufficient for the low currents used, but why not?)
* Add github URL and OSH logo
