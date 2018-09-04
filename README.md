# OctoPrint-LEDStripControl

OctoPrint Plugin that intercepts custom GCode commands and controls local GPIOs accordingly.

Implements a custom gcode command syntax.
        
        M123 as an example:
        M123: Set Status LED Color - R-G-B Optional (W)
        M123 R255       ; Turn LED red
        M123 R255 G127  ; Turn LED orange (PWM only)
        M123            ; Turn LED off
        M123 R G B      ; Turn LED white
        M123 W          ; Turn LED white if using RGBW strips (optional)

## Setup

1. Make sure that the OctoPrint user is in the gpio group via the following command.

    	usermod -a -G gpio pi

1. Install via the bundled [Plugin Manager](https://github.com/foosel/OctoPrint/wiki/Plugin:-Plugin-Manager)
or manually using this URL:

    	https://github.com/google/OctoPrint-LEDStripControl/archive/master.zip

1. Restart OctoPrint

## Configuration

**NOTE: GPIO pins should be specified as physical number and not BCM number.**

Configure the GPIO pins via the OctoPrint settings UI.

## Disclaimer

This is **not** an official Google product.
