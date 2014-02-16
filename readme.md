Trinky
=========

[![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-top.jpg)](https://github.com/beargun/trinky/raw/master/pictures/trinky-top-large.jpg)

## A Trinket clone using only through-hole components



The goal of this project was to create a [Trinket](https://github.com/adafruit/Adafruit-Trinket-USB) clone using only through-hole components. 

### Goals

*   **Use only though-hole components**. Since there are no through-hole mini-USB B sockets, I opted for a USB A etched right on the board (similar to the [Digispark](http://digistump.com/products/1))
*   **Small footprint**. Get it at least as small as the original Trinket.
*   **Optional fuse**. I'm really fond of my USB ports, so for extra peace of mind I added a polyfuse. I choose a surface-mount ptc fuse, as they tend to be faster than through hole versions. This fuse is optional (as it would break the first goal).  
*   **Different bootloader**. I slighty [altered the bootloader](https://github.com/beargun/Adafruit-Trinket-Gemma-Bootloader), to have it go into programming mode, only when the reset button is pressed. So when you power it up, your code will run immediately, instead of after 10 seconds.
*   **No voltage regulator**. The ATtiny85 will work on 2.7-5.5V. If you power your project using batteries, a voltage regulator will just decrease battery file. Just choose a battery with less than 5.5V. Also, I didn't have room for it. 

### Creating the board

Tranfering the layout to the board using toner-transfer. You can see some paper residue on the toner. This doesn't hinder the etching
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-1.jpg)

Etching the board in hydrochloric acid and hydrogen peroxide. I'm agitaring the board using a modified cd-rom drive.
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-2.jpg)

Almost done.
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-3.jpg)

If you look closely you still see some copper. In hindsight I should have left it in the eching solution a bit longer.
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-4.jpg)

With the toner removed you can clearly see the copper bridge. Easily fixed with a sharp knife.
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-5.jpg)

All fixed. Note that I also cut away some of the outline. Otherwise I couldn't test for short using my multi-meter
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-6.jpg)

Holding it agains the light reveals there are no more obvious shorts.
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-7.jpg)

Holes drilled.
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-8.jpg)

Outline cut using an electric scrollsaw.
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-9.jpg)


### Assembling the board

![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-10.jpg)
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-11.jpg)
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-12.jpg)
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-13.jpg)
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-14.jpg)
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-15.jpg)
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-16.jpg)
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-17.jpg)
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-18.jpg)
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-19.jpg)
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-20.jpg)
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-21.jpg)
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-22.jpg)
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-23.jpg)
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-24.jpg)
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-25.jpg)
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-26.jpg)
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-27.jpg)
![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-28.jpg)
