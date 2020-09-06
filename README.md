**OLA trigger config to control [WiZ lights](https://www.wizconnected.com/en/consumer/products/) with DMX (Art-Net, sACN or via DMX input)**  
Experimental version.  

**Requirements**

* [OLA](https://www.openlighting.org/ola/)
* [Node-RED](https://nodered.org/)
* [repeat node](https://flows.nodered.org/node/node-red-contrib-repeat)
* [curl](https://curl.haxx.se/)

**Installation**
  
* Download the [wiz_light.conf](wiz_light.conf) and edit the configuration section
* Download the [wiz_flow.json](wiz_flow.json) file, import it into Node-RED and edit the Hue bridge settings

[OLA trigger documentation](https://www.openlighting.org/ola/advanced-topics/ola-dmx-trigger/)

**Usage** 

* Before running ola_trigger, make sure that olad is running and the universe has been configured with a DMX512 source.  
The config file is provided on the command line:

`ola_trigger wiz_light.conf`
