# This project emulates a Wemos device which works with Alexa to raise and lower the Bofu window roller motors.  
*Please make note that this project was not created by, affiliated with, or endorsed by Bofo, Wemos, Amazon, or the Alexa brand.

**Forked from Makersmusings Fauxmo library.  The WifiManager portion was contributed by Tapzu and the RF_Record portion by SillyFrog.  These libraries need to be installed in the Arduino IDE for this sketch to function. The repositories can be found at the following locations:

https://github.com/makermusings/fauxmo

https://github.com/tzapu/WiFiManager

https://github.com/sillyfrog/RFreplayESP

STL's for the project enclosure can be downloaded at 
https://www.thingiverse.com/thing:2764119

### Summary

This code allows the basic control of the Bofu window motors using the following components:

1.) 12V Bofu Window Motor/s

2.) NodeMCU 12E

3.) 5v-RF transmitter and receiver *Works with NodeMCU 3.3v logic level

### Design Notes
-Control of the Bofu roller shade motors is limited to fully open and fully closed positions via this code.  The remotes that come with the motors are used to set the limits.  Because the remotes continue to work concurently with this set up, they can still be used to stop the shades in variouse positions.  One of the great things about this method is that the shades can be triggered to open and close by voice, on a schedule or by other chain events.  An example of a chain event would be if you ask Alexa to turn on your DVD then the shades close and the lights dim from the same command.

-The WifiManager requires a 2.4 GHZ wireless connection. It will not work through 5 GHZ. Most any older or dual band router will do.

-The Wifimanager library was added to eliminate the need to manually configure a user name and password into the sketch in the event wireless network password or wireless access point are changed.

-If the NodeMCU cannot connect to the network the ESP xxxxx will apear in the list of available wireless networks for reconfiguration.
Links to thingy verse to be provided for the print of an enclosure for the NodeMCU.

### Instructions

Before uploadding this code to the NodeMCU the section of code commented, 

//INSERT BOFU DOWN CODE HERE
//INSERT BOFU UP CODE HERE

will need to be updated with the RF codes matching your specific remotes. The Wiki will provide information on how to decode the Bofu remote. I spent an embarasing amount of time finding a consistent way to decode these remotes so hopefully you wont's have to.
