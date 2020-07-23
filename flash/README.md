# Flashing Microcontrollers


Each station node is build atop a microcontroller, where each
microcontroller is connected to one or more sensors either directly or
by [Grove hubs](https://www.seeedstudio.com/Grove-I2C-Hub.html). 

The CCX system is designed to be used with the [m5Stack Atom Lite](https://m5stack.com/collections/m5-core/products/atom-lite-esp32-development-kit)
ESP32-Pico based microcontroller.  

There are two nodes that the core Arduino code has been developed for.
Before compiling the microcode onto the Arduino, you will also need to
install the core IoTwx shared library which controls many of the
communications and initialization functions of each node.

This core library can found at the following repository. It should be
installed in your `Arduiono/libraries` directory and once installed, you
may use it by the `#include "IoTwx.h"` directive.


* [https://github.com/NCAR/esp32-atomlite-arduino-iotwx](https://github.com/NCAR/esp32-atomlite-arduino-iotwx)

Please see the
[parts list](https://drive.google.com/file/d/1Hnn0Ms2DzVQgRFmGBpLQ9W2NGEz2gopc/view?usp=sharing)
for the microcontroller, sensors and cables required or recommended to
build and connect a base system.


## Atmos Node 

The Atmos node is comprised of two sensors and two 3d-printed housing
units. The first sensor houses the atmospheric conditions for air
temperature, humidity and barometric pressure. It can be fitted with the
[Seeedstudio BME280 Grove](https://www.seeedstudio.com/Grove-BME280-Environmental-Sensor-Temperature-Humidity-Barometer.html)
environmental sensor, or if you would like to obtain aggregate VOC
measurements, you can fit the housing with the
[BME680 Grove](https://www.seeedstudio.com/Grove-Temperature-Humidity-Pressure-and-Gas-Sensor-for-Arduino-BME680.html)
sensor. The code is designed to work with both sensors (but not
simultaneously). These parts can be found in the
[parts list](https://drive.google.com/file/d/1Hnn0Ms2DzVQgRFmGBpLQ9W2NGEz2gopc/view?usp=sharing).


### Radiation Shield

<img width="360" alt="atmos node"
src="https://raw.githubusercontent.com/ClimateChangeXplorers/ClimateChangeXplorers.github.io/master/img/atmos-node.jpg"/>

The radiation shield sensor captures the following measurements:
temperature, humidity, barometric pressure, and optionally VOC (if using
the BME680 sensor).

**PRINTING**

* the radiation shield design 3d print files can be found in the
  [`/build/stl/atmos`](../build/build/stl/atmos) page. If you need to
  print, you will need to follow the instructions there to print the
  housing.

**FLASHING**

* the code to flash the node can be found in the
  [esp32-atomlite-arduino-atmos-node repository](https://github.com/NCAR/esp32-atomlite-arduino-atmos-node).
  You will to follow the instructions there to understand the Arduino
  flashing requirements and procedures.

### UV 
 
 Radiation Shield and UV Temperature, Humidity, Presure, VOC, and UV

https://github.com/NCAR/esp32-atomlite-arduino-atmos-node

### Hydro Node: Precipitation

https://github.com/NCAR/esp32-atomlite-arduino-hydro-node

### AeroNode: Wind Vane & Anemometer
Wind speed and direction

coming soon 


