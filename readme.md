Trinky
=========

## A Trinket clone using only through-hole components

[![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-top.jpg)](https://github.com/beargun/trinky/raw/master/pictures/trinky-1.jpg)


The goal of this project was to create a [Trinket](https://github.com/adafruit/Adafruit-Trinket-USB) clone using only through-hole components. 

### Goals

*   **Use only though-hole components**. Since there are no through-hole mini-USB B sockets, I opted for a USB A etched right on the board (similar to the [Digispark](http://digistump.com/products/1))
*   **No voltage regulator**. The ATtiny85 will work on 2.7-5.5V. If you power your project using batteries, a voltage regulator will just increase battery usage. Just choose a battery with less than 5.5V.
*   **Small footprint**. Get it at least as small as the original Trinket.
*   **Optional fuse**. I'm really fond of my USB ports, so for extra peace of mind I added a polyfuse. I choose a surface-mount ptc fuse, as they tend to be faster than through hole versions. This fuse is optional (as it would break the first goal).  
*   **Different bootloader**. I slighty altered the bootloader, to have it go into programming mode, only when the reset button is pressed. So when you power it up, your code will run immediately, instead of after 10 seconds.

