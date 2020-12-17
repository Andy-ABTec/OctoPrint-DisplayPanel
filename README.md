# OctoPrint-DisplayPanel

![Header image made of photos of the control panel](https://raw.githubusercontent.com/sethvoltz/OctoPrint-DisplayPanel/master/docs/header.jpg)

This plugin implements the software control side of an OctoPrint Control Panel for Octopi. The hardware half is a series of 4 buttons, an OLED screen and a 3D printed case that mounts on the printer next to the Raspnerry Pi so it can be plugged in to the header pins.

**Watch a demo of the panel in action!** More photos are at the end of this readme.

[![Screenshot of demo video](https://img.youtube.com/vi/78emT1ollu4/0.jpg)](https://youtu.be/78emT1ollu4 "Click here to watch a demo on YouTube")

## Hardware

Besides the [3D printed parts](https://www.thingiverse.com/thing:4674214), you will need the following parts:

- 1x 30x70mm proto board (similar to [this product](https://www.amazon.com/gp/product/B06XGWSWT1))
- 1x 0.96" i2c OLED display ([Amazon](https://www.amazon.com/gp/product/B0833PF7ML))
- 4x 12mm tactile buttons ([Amazon](https://www.amazon.com/gp/product/B019I11FI2))
- Wires

Wire up the board as in the diagram below, ensuring that the OLED is set at or below the height of the buttons. The buttons will not fit through the proto board holes, instead they will just fit in and sit above the board. This is expected and the 3D model accounts for it.

Once the board is wired up, run the wires through the hole in the back of the base of the case, slide the board into the lid and slide the lid into the base. Depending on your printer, the lid should slide on with just enough grip to hold in place and the lid and base work together to hold the board in the correct position.

![Wiring diagram for the control panel](https://raw.githubusercontent.com/sethvoltz/OctoPrint-DisplayPanel/master/docs/wiring-diagram.png)

## Setup

**NOTE:** This plugin required OctoPrint to be updated to run on Python 3. Please follow [these instructions](https://community.octoprint.org/t/upgrade-your-octoprint-install-to-python-3/23973) if you are not already on Python 3.

Before installation, you will need to `pip` install a few dependencies. Please ensure you are using the `virtualenv` bundled version:

    ~/oprint/bin/pip install pillow
    ~/oprint/bin/pip install adafruit-circuitpython-ssd1306

These will allow communication with the OLED display.

Lastly, install via the bundled [Plugin Manager](https://docs.octoprint.org/en/master/bundledplugins/pluginmanager.html)
or manually using this URL:

    https://github.com/sethvoltz/OctoPrint-DisplayPanel/archive/master.zip

## Configuration

There are no configuration options for this plugin at the moment. Plug and play!

## More Photos

![Hardware shot from front](docs/glamour-1.jpeg)
![Hardware shot from back](docs/glamour-2.jpeg)
![Hardware In-Situ](docs/in-situ.jpeg)
