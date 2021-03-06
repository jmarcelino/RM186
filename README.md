# RM186 demos
These are my demos using the [Laird RM186](http://www.lairdtech.com/products/rm1xx-lora-modules) LoRa + BLE module

Script  | Description
----- | -----
__solarbeacon2lora__ | Receives BLE temperature and humidity advertisement readings from Cypress Solar-Powered BLE Sensor Beacons and sends to the configured LoRaWAN application
__i2cscan__ | Simple I2C bus scanner
__ds3231-lib__ | Library of functions for the DS3231 Real Time Clock connected via I2C
__ds3231-test__ | Test script for ds3231-lib

### Setup

The smartBasic (.sb) files can be _XCompiled_ and loaded to the module using the [UwTerminalX](https://github.com/LairdCP/UwTerminalX) tool from Laird.

Make sure you copy the RM1xx-defs.h file first from the Laird SDK and place it in the same folder as the scripts. This is specific to your version of the firmware.

Then setup the module to your specific LoRaWAN/TTN settings:

```
at+cfgex 1000 "Your App EUI"
at+cfgex 1002 "Your App Key"
atz
```

You can get your app EUI and key from the Things Network Dashboard, ttnctl command line tool or check with your LoRaWAN provider

### Acknowledgements
[Laird](http://www.lairdtech.com/products/rm1xx-lora-modules) for creating such a great module and providing sample code. Check [their Github](https://github.com/LairdCP) too!

[The Things Network](https://www.thethingsnetwork.org) for proving a free backend and a great community

### References
[Laird Core smartBASIC User Guide] (http://cdn.lairdtech.com/home/brandworld/files/User%20Guide%20-%20smartBASIC%20Core%20Functionality.pdf)

[SmartBASIC Extensions for RM1xx Series] (http://cdn.lairdtech.com/home/brandworld/files/Guide%20-%20smartBASIC%20Extensions%20-%20RM1xx.pdf)
