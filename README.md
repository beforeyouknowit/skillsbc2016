# Skills BC 2016

This is happening on April 13th 2016 in Abbotsford, BC.

> It sounds like we've settled on the (LED matrix display that shows last texted emoji) as our booth demo project.

### The project needs to be broken down into the following parts:

- Raspberry Pi 2 as display controller and local (Node) web server
- LED matrix display build; 64x64 RGB LED display, incl. Raspberry Pi, HAT, power supply, acquired via Adafruit, (see cart with parts selection below.)
- Essentially we're following this [Adafruit build guide](https://learn.adafruit.com/raspberry-pi-led-matrix-display) and this [Adafruit RGB HAT tutorial](https://learn.adafruit.com/adafruit-rgb-matrix-plus-real-time-clock-hat-for-raspberry-pi) for this build. Another LED guide from Adafruit can be found [here](https://github.com/hzeller/rpi-rgb-led-matrix).
- Twilio API methods (regex'ing out the emoji, Node app picking up latest, updating display, debug etc.)
- Display/drawing methods
- Web page with basic status/debug on Twilio connection, display/draw status etc.

### If we still have additional time between now and April 13th:

- A two-player Pong or Snake game on the LED matrix display
- Multiple roles and web views from Node app, i.e. 'admin', 'leaderboard', '1st player view', '2nd player view' etc.
- Communal Lite-Brite® - LED matrix with ability to draw on colours and intensities by touch via a browser-based app (ie. used on a tablet)
- Solid documentation (via [Docco](https://jashkenas.github.io/docco/)?)
- Custom emoji importer for web front end?

### March 4th Update

Risk reduction: best to switch to 3x 32x32px RGB matricies, as this removes any questions about whether or not the RGB HAT is capable of handling 2x 32x64px panels instead.

Now that the Raspberry Pi 3 is available, although at a steep premium in Canada at the moment, our parts builds now look like this:

~ $92 CAD: [Raspberry Pi 3 on Amazon](http://www.amazon.ca/gp/product/B01C6FRVQM)

~ $225 USD: Adafruit cart of parts; (Expect to pay another $30-50 CAD for duty upon delivery via UPS.)

![adafruit cart](http://i.imgur.com/iaj8ZOH.png)