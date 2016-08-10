# RM186 demos
These are my demos using the Laird RM186 LoRa + BLE module

* _solarbeacon2lora_:  Receives BLE temperature and humidity advertisement readings from Cypress Solar-Powered BLE Sensor Beacons and sends the LoRaWAN application

### Setup

The smartBasic (.sb) files can be _XCompiled_ and loaded to the module using the UwTerminalX from Laird.

Make sure you copy the RM1xx-defs.h file first from the Laird SDK and place it in the same folder as the scripts. This is specific to your version of the firmware.

Then setup the module to your specific LoRaWAN/TTN settings using:

```
at+cfgex 1000 "Your App EUI"
at+cfgex 1002 "Your App Key"
atz
```


### Acknowledgements
@LairdCP for creating such a great module and providing sample code. Check their Github too!
https://www.thethingsnetwork.org for proving a free backend and a great community

### References
Laird Core smartBASIC User Guide: smartBASIC Extensions: http://cdn.lairdtech.com/home/brandworld/files/User%20Guide%20-%20smartBASIC%20Core%20Functionality.pdf

RM1xx Series: http://cdn.lairdtech.com/home/brandworld/files/Guide%20-%20smartBASIC%20Extensions%20-%20RM1xx.pdf
