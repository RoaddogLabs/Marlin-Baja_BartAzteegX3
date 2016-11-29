### Roaddog Labs Baja/Bart Marlin Firmware for AzteegX3 Controller
### 

This fork is configured specifically for the Roaddog Labs Baja or Bart
with an AzteegX3 controller.  It's based on Marlin 1.0.2-2 that was
pushed 06 Nov, 2016.

Details and specs for the AzteegX3 are at
http://reprap.org/wiki/Azteeg_X3

__What This Does__

The settings are preconfigured for the stock configuration as shipped
from Roaddog Labs for both Baja and Bart.  If you are familiar with
hacking Marlin I've just changed the board type from RAMPS to AzteegX3
(board def 67).  The other settings are direct ports from a stock Baja
or Bart with the exception of SD and display configs.  There is no
support for SD storage or external displays in this build.  This build supports reliable connections to the board at 250000 baud.


__How to Build__

Windows platforms need the USB VCP Drivers.  The Azteeg X3 uses the
newer FT231x USB to UART chip and it needs the updated VCP(virtual com
port) drivers from
[http://www.ftdichip.com/Drivers/VCP.htm](http://www.ftdichip.com/
Drivers/VCP.htm) . Download the correct version for your operating
system or you can get the executable version for Windows(easier).
Windows may try to do an update to locate the proper drivers but it is
recommended to install the FTDI drivers for better performance. The VCP
drivers will install a COM port on your computer for the Azteeg X3.  You
can check what port number was assigned by going to your device manager
and click on Ports(COM & LPT) look for something that says "USB Serial
Port(COM3)" where COM3 is you assigned port number(this will vary from
PC to PC). Remember this number as you will be using it later in
configuring other software.

On Mac and Linux the drivers should already be installed.  If not get a
driver from
[http://www.ftdichip.com/Drivers/VCP.htm](http://www.ftdichip.com/
Drivers/VCP.htm)

To build the firmare we use Arduino 1.6.7 IDE though any newer version should work.  We recommend not using any Arduino IDE version prior to 1.6.4 as we've had issues with newer Marlin dists not building properly on earlier IDE versions.





The [original README.md](Orig_README.md) from the fork.