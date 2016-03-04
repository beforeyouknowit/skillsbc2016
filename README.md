# Skills BC 2016

This is happening on April 13th 2016 in Abbotsford, BC.

> It sounds like we've settled on the (LED matrix display that shows last texted emoji) as our booth demo project.

### The project needs to be broken down into the following parts:

- Raspberry Pi 2 as display controller and local (Node) web server
- LED matrix display build; 64x64 RGB LED display, incl. Raspberry Pi, HAT, power supply, acquired via Adafruit, (see cart with parts selection below.)
- Twilio API methods (regex'ing out the emoji, Node app picking up latest, updating display, debug etc.)
- Display/drawing methods
- Web page with basic status/debug on Twilio connection, display/draw status etc.

### If we still have additional time between now and April 13th:

- A two-player Pong or Snake game on the LED matrix display
- Multiple roles and web views from Node app, i.e. 'admin', 'leaderboard', '1st player view', '2nd player view' etc.
- Communal Lite-Brite® - LED matrix with ability to draw on colours and intensities by touch via a browser-based app (ie. used on a tablet)
- Solid documentation (via [Docco](https://jashkenas.github.io/docco/)?)
- Custom emoji importer for web front end?

### Adafruit parts build / cart with product IDs:
![adafruit cart](http://i.imgur.com/ocUsaFD.png)