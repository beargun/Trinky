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
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-1.jpg)

Etching the board in hydrochloric acid and hydrogen peroxide. I'm agitaring the board using a modified cd-rom drive.
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-2.jpg)

Almost done.
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-3.jpg)

If you look closely you still see some copper. In hindsight I should have left it in the eching solution a bit longer.
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-4.jpg)

With the toner removed you can clearly see the copper bridge. Easily fixed with a sharp knife.
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-5.jpg)

All fixed. Note that I also cut away some of the outline. Otherwise I couldn't test for short using my multi-meter
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-6.jpg)

Holding it agains the light reveals there are no more obvious shorts.
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-7.jpg)

Holes drilled.
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-8.jpg)

Outline cut using an electric scrollsaw.
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-9.jpg)


### Assembling the board

Since the led has to be at the top (the same side as the copper), I put the leads down, and then back up in the holes next to it. Otherwise you can't have the led flush with the board, as you have to be able to put the soldering iron underneath it.
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-10.jpg)
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-11.jpg)

Next add a jumper and the two zener diodes to the underside, and solder it.
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-12.jpg)
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-13.jpg)

The resistor for the led.
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-14.jpg)

The two 68-Ohm resistors. **You should move the resistors more to the right, to make the button fit better.**
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-15.jpg)

Note the solder bridge I accidentily made. I only noticed it when I was done, and did some final testing using my multimeter.
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-16.jpg)

Remove two of the leads from the button. I also had to remove a bit of one corner. You shouldn't have to do that if you moved the resistor a bit more to the right.
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-17.jpg)

Here I added the button and the 1800-Ohm resitor (Trinket uses 1500-Ohm). **You should put this resistor one the bottom. As it won't really fit, if you've moved the two resistors as I instructed above**
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-18.jpg)

Here come the brains. I've already flashed my altered the bootloader](https://github.com/beargun/Adafruit-Trinket-Gemma-Bootloader) onto it.
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-19.jpg)

Bend over the pins. 
<br />I also scraped away the trace between the two pads of the polyfuse. If you don't add the polyfuse you should just leave it there. 
<br />Here I've also tinned the usb connector. This will make it fit better into the usb socker, and prevent the copper from oxidizing and wearing out.
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-20.jpg)

Here I soldered the pins, and added the optional polyfuse. 
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-21.jpg)

Because the ATtiny is at the bottom, I had to put shims under the header pins to raise them high enough to reach the board.
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-22.jpg)

For a bit of extra bling, I added a few layers of nail varnish. This will prevent accidental short, oxidation and tin-whiskers (just kidding on the last one). I added some extra layers at the top right, where the board might touch the outside/shielding of the usb socket.
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-23.jpg)

Too scale. The board ended up fractionally shorter (29.5mm) than the board of the real Trinket (note that mini-usb sticks out even more). It is however slightly wider. I could just cut away some more of the board, but I'd have to slightly move some components in the layout to match the width of the Trinket. Win some, lose some
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-25.jpg)

<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-26.jpg)

<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-27.jpg)

And yes, it works!
<br />![Trinky](https://github.com/beargun/trinky/raw/master/pictures/trinky-28.jpg)

Thank you for watching!