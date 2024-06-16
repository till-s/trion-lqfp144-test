# Efinix Trion JTAG Programmer and Evaluation Board

This board implements a JTAG programmer that can be used with
the efinity software to access [efinix](https://www.efinixinc.com)
FPGAs vie JTAG.

The board also hosts a Trion T8Q144 device (pin-compatible with
the more loaded T20Q144 which could be used as an alternative),
ULPI and full-speed PHYs and a bunch of LEDs/GPIOs.

I have used this board successfully to exercise the
[mecatica-usb](https://www.github.com/till-s/mecatica-usb) with
trion devices.

The programmer is connected to the trion's JTAG port with a
flat ribbon cable which makes it possible to use the PCB
as a programmer for other boards with an Efinix FPGA.

## Programmer-only Mode

It is possible to partially load the board if you are only looking
for a programmer.

 - load everything on the FT-USB-JTAG sheet
 - load the 3V3 converter (U12) and associated components
   on the Power sheet. You can omit U6 and everything associated
   with it.
 - However, make sure you *do load* R56 (may be a zero-Ohm jumper
   if U6 is omitted) in order to enable the 3V3 converter.
