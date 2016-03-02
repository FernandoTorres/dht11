Description
===========

This is a small tool that takes humidity and temperature measurements
using a DHT11 sensor on a Raspberry Pi.

The code has been adapted from
[this blog post.](http://www.rpiblog.com/2012/11/interfacing-temperature-and-humidity.html]

By default it outputs humidity (in %) and temperature (in degrees
Celsius). Here's an example:

```
$ sudo ./dht11 
36,24
```

which means that the humididy is 36 % and the temperature is 24 degrees
Celsius.

As shown above, you'll need to run it as the root user, or using sudo.

There are options to output the date and time before the measurements
and to use the Farenheit scale instead of Celsius. Run:

```
dht11 -h
```

to see all options.


Wiring
======


Holding the DHT11 sensor towards you (the side with the grid), you should
connect the left-most pin to 3V3 (GPIO pin 1 on the Raspberry Pi).
The second pin from the left is the data pin. That should be connected
to GPIO pin 7 on the Raspberry Pi.
Leave the third pin unconnected.
The right-most pin should be connected to a GND pin on the Raspberry Pi.

To prevent random data connect a 10K resistor between the data pin
(the second from the left) and 3V3.


Installation
============

You will need to have wiringpi installed, so first run:

```
sudo apt-get install wiringpi
```

After that run:

```
make
```

and a dht11 executable should be created in the same directory.



