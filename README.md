# Marlin 3D Printer Firmware for Prusa I3 pro B with 3DTouch and TMC2208
This is a fork of the original Marlin 2 printer firmware. The only changes here are in configuration files.
I did this because the configuration of every Marlin version I tried was different from the former one and it was quite difficult to reenable my little changes to the default configuration of the geetech i3 pro b.
So if you really have the same setup then I do, you may just download this, compile it and it should work. (If not, you probably have a differnt setup and need to make your own changes to the configure files. In that case you could as well download the original code...)

## Used Setup:
* Standard Geetech I3 pro B
* Geetech 3DTouch Z-Axis sensor
* TMC2208 stepper motor drivers for X/Y/Z Axis
* * default stepper motor driver for extruder
* added hot-end cooler
* reduced bed size because 
* * hot-end cooler needs some space (X-axis)
* * clamps to hold glass bed interfered with nozzle

## Important before use
Make sure you used the same stepper drivers and connected the 3DTouch sensor like shown here
[3DTouch documentation](https://www.geeetech.com/wiki/index.php/3DTouch_Auto_Leveling_Sensor)
or here
[3DTouch documentation, pdf](http://www.geeetech.com/Documents/3DTouch%20auto%20leveling%20sensor%20%20User%20Manual.pdf)
I connected the sensor to PIN 32, most others use PIN 11 and thus the defines in MARLIN point to PIN 11. That's why I did not use the "define BLTOUCH".
So make sure that this is correct and use the test commands as shown in pdf.

I prefer 3-point auto bed leveling, but this did not work for me, so I switched to bilinear leveling. This seems to produce best results.

## What hardware is used

* _Geetech 3DTouch sensor_
* * [3DTouch documentation](https://www.geeetech.com/wiki/index.php/3DTouch_Auto_Leveling_Sensor)
* _TMC2208_ stepper motor driver
* * [example info link](https://jgaurorawiki.com/a5/silent-stepper-driver-tmc2208)
* Fan duct for hot-end cooler
* * [Thingiverse item](https://www.thingiverse.com/thing:2139318/files)
* 3DTouch adapter was not needed (mine included one) otherwise try these
* * [3DTouch adapter 1](https://www.thingiverse.com/thing:1838009)
* * [3DTouch adapter 2](https://www.thingiverse.com/thing:2086357)

## Compiling:
Arduino IDE seems to be no longer suppported on windows, so use platformio
[PlatformIO](http://docs.platformio.org/en/latest/ide.html#platformio-ide)


# Additional Information
The original Marlin source code and more information can be found at the [marlin git](https://github.com/MarlinFirmware/Marlin).

Additional documentation can be found at the [Marlin Home Page](https://marlinfw.org/).

![GitHub](https://img.shields.io/github/license/marlinfirmware/marlin.svg)

<img align="right" width=175 src="buildroot/share/pixmaps/logo/marlin-250.png" />


## Credits of original marlin fw

The current Marlin dev team consists of:

 - Scott Lahteine [[@thinkyhead](https://github.com/thinkyhead)] - USA &nbsp; [Donate](http://www.thinkyhead.com/donate-to-marlin)
 - Roxanne Neufeld [[@Roxy-3D](https://github.com/Roxy-3D)] - USA
 - Chris Pepper [[@p3p](https://github.com/p3p)] - UK
 - Bob Kuhn [[@Bob-the-Kuhn](https://github.com/Bob-the-Kuhn)] - USA
 - Erik van der Zalm [[@ErikZalm](https://github.com/ErikZalm)] - Netherlands &nbsp; [![Flattr Erik](https://api.flattr.com/button/flattr-badge-large.png)](https://flattr.com/submit/auto?user_id=ErikZalm&url=https://github.com/MarlinFirmware/Marlin&title=Marlin&language=&tags=github&category=software)

## License

Marlin is published under the [GPL license](/LICENSE) because we believe in open development. The GPL comes with both rights and obligations. Whether you use Marlin firmware as the driver for your open or closed-source product, you must keep Marlin open, and you must provide your compatible Marlin source code to end users upon request. The most straightforward way to comply with the Marlin license is to make a fork of Marlin on Github, perform your modifications, and direct users to your modified fork.

While we can't prevent the use of this code in products (3D printers, CNC, etc.) that are closed source or crippled by a patent, we would prefer that you choose another firmware or, better yet, make your own.
