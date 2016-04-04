# Skills BC 2016 Demonstration
### Raspberry Pi RGB LED Matrix Display for last-sent emoji via Twilio API.
### Presentation on April 13th 2016 in Abbotsford, BC.

![Adafruit RGB Matrix HAT on Raspberry Pi 3](https://learn.adafruit.com/system/assets/assets/000/022/491/large1024/leds_RGB_Matrix_Hat_iso_demo_01_ORIG.jpg)

### Installation and Setup

#### Note: This assumes you:
- Have a **HDMI-connected computer display** and USB keyboard + mouse attached for the initial setup. HDTVs usually stretch the HDMI video signal beyond the borders of the bezel.
- Are connecting the Pi 3 as well as your setup computer to the same local wired/wireless network router, on the same subnet and permissions/visibility levels, etc.
- Have a broadband internet connection available to this router.
- Have a second computer for downloading and creating the initial Rasbian OS Micro SD card image. View the official Raspberry Pi Operating System Installation instructions [here.](https://www.raspberrypi.org/documentation/installation/installing-images/README.md)
- Already assembled and attached the Adafruit [RGB Matrix + RTC HAT](https://www.adafruit.com/products/2345) and as per the official [Adafruit Learn article](https://learn.adafruit.com/adafruit-rgb-matrix-plus-real-time-clock-hat-for-raspberry-pi).


### First configuration steps of the Pi:
- Download and disk-image a copy of [Raspbian Jessie Lite](https://www.raspberrypi.org/downloads/raspbian/) onto a fresh MicroSD card (8, 16, or 32GB card recommended.)
- Insert your MicroSD card into the Pi 3.
- Boot your Pi 3. 
- On the Raspbian desktop, open a Terminal window, and run `sudo raspi-config` for the first time.
- In `raspi-config`, select `1 Expand Filesystem` so that the remaining available space on your MicroSD card will be accessible to the OS; this runs a once-off script (upon reboot) that expands the partition on the MicroSD card. Press return/enter to get back to the menu.
- Back in the `raspi-config` main menu, select `3 Boot Options` and select `B2 Console Autologin` and press return/enter.
- Also in the `raspi-config` main menu, open up `9 Advanced Options` and `Enable` the following:
  - Disable `A1 Overscan` 
  - Enable `A4 SSH` to allow remote SSH access via the usual TCP port 22.
  - Enable `A7 I2C`, (this requires a few more "Yes" confirmations, etc.)
  - Optional: Run `A0 Update` to update the `raspi-config` utility to the latest version from Raspbian.
- Optional: Configure `5 Internationalisation Options` to your language and keyboard preferences.
- Select `Finish` at the bottom of the main menu, and when prompted to reboot, select `Yes` and wait for your Pi 3 to reboot.
- Your Pi 3 will now boot to a terminal, rather than into the Raspbian (Debian-like) desktop/GUI. (If you ever want or need to start the GUI with a HDMI display / keyboard / mouse attached again, just run `startx` from the terminal.)
- Your Pi 3 will also be outputting the HDMI video signal to 100% of the attached display, so if you're connected to an HDTV, part of the terminal text might be cut off along the edges of the screen. Defer to connecting via SSH as seen below.
- To display your Pi's local ethernet IP, run `sudo ip addr show` which will print a short list of your network interface details to the terminal. Look under `eth0` and find the number after `inet` - this is the IP of your Pi 3 on your local router. Make a note of this IP.

### SSH into the Pi 3
- Back on your main computer, open a terminal window (Terminal in OSX and Linux, PuTTy on Windows, etc.)
- In the terminal, enter `ssh pi@y.y.y.y` where `y.y.y.y` is the IP address you noted at the end of the previous batch of steps. Example: `ssh root@192.168.1.170` <return>.
- You'll be propmted to enter the password to log in to the `pi` account; the default is `raspberry`.

### Optional: Install `htop` and view Pi's CPU and Memory usage from SSH:
- Open another local terminal window on your spare computer, and SSH into the Pi as per previous steps.
- In the terminal, run `sudo apt-get -y install htop` to install the [htop](https://github.com/hishamhm/htop) interactive process viewer.
- Once installation has completed, run `htop` from the prompt to view the CPU usage, process tree, memory usage, uptime, etc.
- Exit `htop` by pressing `q` on your keyboard, and then enter `exit` in the terminal to disconnect the SSH session when done.

### Update and install necessary software:
- Once you've logged in via SSH, lets immediately update the software to the latest versions from Raspberry; run `sudo apt-get -y update` then `sudo apt-get -y upgrade` -- the upgrade process might take 10-20 minutes to complete.
- Install necessary apps and dependencies:
> `wget http://node-arm.herokuapp.com/node_latest_armhf.deb`
> `sudo dpkg -i node_latest_armhf.deb`
- Clone this repo:


### Want to build your own? Our Parts List to can be found in `partslist.md`.

### Documentation
- Documentation via (via [Docco](https://jashkenas.github.io/docco/)?)
- Read the [Adafruit build guide](https://learn.adafruit.com/raspberry-pi-led-matrix-display) and this [Adafruit RGB HAT tutorial](https://learn.adafruit.com/adafruit-rgb-matrix-plus-real-time-clock-hat-for-raspberry-pi) for this build. Another LED guide from Adafruit can be found [here](https://github.com/hzeller/rpi-rgb-led-matrix).