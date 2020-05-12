# Threejs-VR-Sensors (under construction)

A project to explore a way to interface different sensors into virtual reality with a Raspberry Pi.

## System Requirements

The types of sensors interfaced to a Raspberry Pi is dependent on what the author have. The project is more about examples of using I<sup>2</sup>C, SPI, and GPIO pins on a Raspberry Pi.<br>

Raspberry Pi with wireless LAN (tested Raspberry Pi 3 Model B+, Model A+, Pi Zero W).<br>

Raspbian Buster with desktop (tested February 2020, 1138 MB version) from:

[https://www.raspberrypi.org/downloads/raspbian/](https://www.raspberrypi.org/downloads/raspbian/)

There are three versions of Raspbian Buster. No reason for choosing the 1138 MB version except it is half the size of the full version. The Lite version is Linux text-only terminals and is not recommended as most examples are shown with a GUI.

After Raspbian is booted, select "Preferences/Raspberry Pi Configuration" and enable I<sup>2</sup>C and SPI.

<img src="images/1-pi-config.png" width="512">

A display, keyboard, mouse, and power supply for Raspberry Pi.

Oculus Quest optional (tested Quest Update >16.0 and three.js r115).<br>

## 1. Melexis Non-contact Infrared Thermometer MLX90614

There are two versions of MLX90614. One 3V and the other, 5V. The author uses a 3V version because Raspberry Pi GPIO are 3.3V logic levels and NOT 5V tolerant.<br>

ALWAYS proper shutdown and power off Raspberry Pi before wiring sensors to GPIO.<br>

One useful terminal command is "pinout".<br>

Even more useful is the images on Raspberry Pi website:

https://www.raspberrypi.org/documentation/usage/gpio/

GPIO2 (Pin 3) is SDA and GPIO3 (Pin 5) is SCL. Pin 1 is 3.3V and Pin 9 is GND.<br>

<img src="images/1-i2cdetect.png" width="480">

<img src="images/1-PyMLX90614.png" width="600">

## 2. Lidar-Lite v2

## References

Derek Molloy, Exploring Raspberry Pi, John Wiley & Sons (2016).

https://pypi.org/project/PyMLX90614/

https://pypi.org/project/smbus2/

https://www.raspberrypi.org/

https://www.adafruit.com/

https://www.sparkfun.com/

<br>Copyright (c) 2020 Hartwell Fong
