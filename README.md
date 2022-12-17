**OLA trigger config files to control [WiZ lights & smart plugs](https://www.wizconnected.com/en/consumer/products/) with DMX (Art-Net, sACN or via DMX input)**  
Experimental beta version, some work left to do.    



**Requirements**

* [OLA](https://www.openlighting.org/ola/)
* [Node-RED](https://nodered.org/)
* [repeat node](https://flows.nodered.org/node/node-red-contrib-repeat)
* [curl](https://curl.haxx.se/)

**Installation**
  
* Download the [wiz_light.conf](wiz-rgb-cw-ww.conf) and edit the configuration section
* Download the [wiz_flow.json](wiz-rgb-cw-ww-flow.json) file, import it into Node-RED and edit the IP addresses to the lamps in the UDP out node in Node-RED and the OLA hostname in the DMX "blocks"

[OLA trigger documentation](https://www.openlighting.org/ola/advanced-topics/ola-dmx-trigger/)

**Usage** 

* Before running ola_trigger, make sure that olad is running and the universe has been configured with a DMX512 source.  
The config file is provided on the command line:

`wiz-rgb-cw-ww.conf`

**DMX protocol** 

| **Channel** | **Value** | **Function**                                    |
|-------------|-----------|-------------------------------------------------|
| 1           | 0\-10     | Lamp 1 off                                      |
| 1           | 11\-255   | Lamp 1 intensity\. Value 10\-100 % low \-> high |
| 2           | 0\-9      | No function                                     |
| 2           | 10\-20    | Lamp 1 color temperature 2700K                  |
| 2           | 30\-40    | Lamp 1 color temperature 3000K                  |
| 2           | 50\-60    | Lamp 1 color temperature 4200K                  |
| 2           | 70\-80    | Lamp 1 color temperature 6500K                  |
| 3           | 0\-255    | Lamp 1 Red intensity                            |
| 4           | 0\-255    | Lamp 1 Green intensity                          |
| 5           | 0\-255    | Lamp 1 Green intensity                          |
| 6           | 0\-255    | Lamp 1 Cold white intensity                     |
| 7           | 0\-255    | Lamp 1 Warm white intensity                     |
