# DotStar PiPainter on a Zero
## Base System
Follow this
https://learn.adafruit.com/dotstar-pi-painter?view=all#raspberry-pi-setup

Highlights:
* Raspbian Lite
* sudo raspi-config
  * spi

## Packages
    sudo apt-get update
    sudo apt-get install git usbmount python-dev python-imaging python-pip
    sudo pip install evdev
    
## Support for System Halt by Buttons   
```
    git clone https://github.com/adafruit/Adafruit-GPIO-Halt
    cd Adafruit-GPIO-Halt
    make
    sudo make install
    sudo vi /etc/rc.local
    
   ``` 
   * add ```/usr/local/bin/gpio-halt 21 &``` before ```exit 0```
## Code
    git clone https://github.com/adafruit/Adafruit_DotStar_Pi
    git clone https://github.com/adafruit/DotStarPiPainter
    git clone https://github.com/adafruit/Adafruit_Python_SSD1306
    git clone https://github.com/adafruit/Adafruit_Python_GPIO.git
