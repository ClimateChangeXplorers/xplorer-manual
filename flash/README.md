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
may use it by the `#include "IoTwx.h" directive.


* [https://github.com/NCAR/esp32-atomlite-arduino-iotwx](https://github.com/NCAR/esp32-atomlite-arduino-iotwx)

### Atmos Node: Radiation Shield and UV
Temperature, Humidity, Presure, VOC, and UV

https://github.com/NCAR/esp32-atomlite-arduino-atmos-node

### Hydro Node: Precipitation

https://github.com/NCAR/esp32-atomlite-arduino-hydro-node

### AeroNode: Wind Vane & Anemometer
Wind speed and direction

coming soon 


