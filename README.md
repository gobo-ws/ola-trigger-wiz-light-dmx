**OLA trigger config to control [WiZ lights](https://www.wizconnected.com/en/consumer/products/) with DMX (Art-Net, sACN or via DMX input)**  
Experimental beta version, some work left to do.

**Requirements**

* [OLA](https://www.openlighting.org/ola/)
* [Node-RED](https://nodered.org/)
* [repeat node](https://flows.nodered.org/node/node-red-contrib-repeat)
* [curl](https://curl.haxx.se/)

**Installation**
  
* Download the [wiz_light.conf](wiz_light.conf) and edit the configuration section
* Download the [wiz_flow.json](wiz_flow.json) file, import it into Node-RED and edit the lamp IP address in the UDP out node in Node-RED

[OLA trigger documentation](https://www.openlighting.org/ola/advanced-topics/ola-dmx-trigger/)

**Usage** 

* Before running ola_trigger, make sure that olad is running and the universe has been configured with a DMX512 source.  
The config file is provided on the command line:

`ola_trigger wiz_light.conf`

**DMX protocol** 

* Channel 1 lamp on/off. Value 0-114 lamp off. 140-255 lamp on  
* Channel 2 Dimmer. Value 10-100 (10%-100%)    
* ~~Channel 3 Color temperature. Value 0-255 (2200-6500K)~~  
* ~~Channel 4 Cold white intensity. Value 1-255~~  
* ~~Channel 5 Warm white intensity. Value 1-255~~  
* ~~Channel 6 Red intensity. Value 1-255~~  
* ~~Channel 7 Green intensity. Value 1-255~~  
* ~~Channel 8 Blue intensity. Value 1-255~~  
