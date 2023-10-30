# Nav. Switch Mount

![5-way Navigation Switch Mount](Images/nav-switch-mount.png)

This is a simple PCB for mounting through-hole 5-way navigation switches such as
the [ALPS SKQUCAA010]. It is intended for use in keyboard projects and provides
a way to both secure a nav. switch and easily wire it into a keyboard matrix.

This switch has been discontinued by ALPS, but equivalents can be obtained from
[Adafruit][ada-504] and various vendors on [AliExpress][ali-SKQ][^1].

<img src="Images/5-five-way-switches.jpg" width="250" title="5-way Navigation Switches">

This repository contains the [KiCad] PCB design files and [Gerber format] files
for PCB production. Zipped Gerber packages are included in the release assets.


[^1]: If no results are shown, try refreshing the page.


## Additional Components Required

 * 1 × [ALPS SKQUCAA010] (or equivalent) navigation switch
 * 5 × 1N4841 [SOD-123] SMD diodes


## Wiring

The switch and diodes are installed as marked. The PCB is wired into the
[keyboard matrix] via the pads[^2] on the base. The row pad is the common pin
for the switch and should be connected to a row pin on the MCU. The other pads
should be connected to columns, with the silkscreen near the pad indicating the
direction (soo note below). It is envisaged that the wires will run to the
underside of the main keyboard PCB via the switch’s central hole, but this will
depend on the exact board being modified — in some cases it may be desirable to
run the wires between the plate and PCB.

### Notes

 * The markings on the silkscreen orient the diodes for **Column-to-Row** use.
   For Row-to-Column matrices the diodes must be installed in the opposite
   direction.
 * The arrows point in the direction that the switch is actually pushed. This
   means that when viewed from the bottom the left and right arrows indicate
   right and left movement respectively.


[^2]: Sorry, through-hole connections would have been much easier to use, but
could not be accommodated in the desired space!


## Mounting

The mounting PCB is intended to be secured to the plate using M2 hardware. Two
~2.1mm holes will need to be drilled through the plate.

Alternatively, for hand-wired builds[^3], the PCB can be used in conjunction
with Kevin Eckert’s [Nav Switch to MX Adapter][nav2mx]. The switch’s legs should
be just long enough to reach past the bottom of the adaptor and through the
mounting PCB. However, the switch’s legs will need to be straightened (be
careful when doing this — the fragility of these legs was one of the main
prompts to create this board) and careful consideration will need to be given
to the order of assembly.


[^3]: There is not enough room between a plate and keyboard PCB for the adaptor
*and* the mounting PCB *and* its diodes.


## Keycaps

Options for keycaps on navigation switches:

 * [Adafruit Black Rubber Joystick Nubbin Cap][ada-4697]
 * Kevin Eckert’s SA profile keycap for navigation switches is available
   alongside their [Nav Switch to MX Adapter][nav2mx]
 * If you don’t mind partially destroying a keycap, I have an [MX keycap to nav.
   switch adaptor][mx2nav] — **this is currently untested**



[ALPS SKQUCAA010]: https://tech.alpsalpine.com/e/products/detail/SKQUCAA010/
[KiCad]: https://www.kicad.org
[Gerber format]: https://en.wikipedia.org/wiki/Gerber_format
[ada-504]: https://www.adafruit.com/product/504
[ada-4697]: https://www.adafruit.com/product/4697
[ali-SKQ]: https://www.aliexpress.com/w/wholesale-SKQUCAA010.html?catId=0&SearchText=SKQUCAA010&spm=a2g0o.productlist.1000002.0
[SOD-123]: https://en.wikipedia.org/wiki/Small_Outline_Diode
[keyboard matrix]: https://www.pcbheaven.com/wikipages/How_Key_Matrices_Works/
[nav2mx]: https://www.thingiverse.com/thing:3958026
[mx2nav]: https://www.tinkercad.com/things/3gL4wvWRLj1?sharecode=r8TKDKdgjJ2txvJRraO-QcmJA2kGXZVvP2sOEYxu-jg
