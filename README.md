# xbmcnut's Home Assistant configuration
### For now, until I can figure out how to get my entire config into Github safely and securely, some of my config files can be accessed through my [Wiki](https://github.com/xbmcnut/Hass.ioConfig/wiki "Pete's Wiki") along with some Home Assistant tips and tricks. 
### My inspiration
When I first started out, no one was making Home Assistant videos until Ben from BRUH Automation came along. His videos were revolutionary and truely set me on a path of home automation obession. Thesedays, with Ben taking a hiatus, inspiration now comes from [BeardedTinker](https://www.youtube.com/c/beardedtinker), [DrZzs](https://www.youtube.com/c/drzzs), [BurnsHA](https://www.youtube.com/channel/UCSKQutOXuNLvFetrKuwudpg), [Csongor Varga](https://www.youtube.com/c/csongorvarga), [digiblurDIY](https://www.youtube.com/c/digiblurDIY), [Franck](https://www.youtube.com/c/FranckNijhof), one of the HA staff now, [Intermit.Tech](https://www.youtube.com/c/IntermitTech), [JuanMTech](https://www.youtube.com/c/JuanMTech), Rob over at [The Hook Up](https://www.youtube.com/c/TheHookUp), [vCloudInfo](https://www.youtube.com/c/vCloudInfo) and of course, the excellent community over at the [**Home Assistant forum**](https://community.home-assistant.io/) including the awesome Ninja Template Warriors who always come to my rescue when I break something. 
### Want to get more info?
<a href="https://twitter.com/xbmcnut?ref_src=twsrc%5Etfw" class="twitter-follow-button" data-show-count="false">Follow @xbmcnut</a> on Twitter, check out [xbmcnut on YouTube](https://www.youtube.com/petestothers) or if you want some specific code mentioned in the [Home Assistant podcast](https://hasspodcast.io/) in Sept 2020, DM me on Twitter or log an [issue](https://github.com/xbmcnut/Hass.ioConfig/issues/new/choose) here and I'll do my best to follow up.
### Hardware
My Home Assistant installation now resides on an [Intel NUC i5](https://amzn.to/2EXNOxO) with 16GB RAM and a [256GB nVME SSD](https://amzn.to/3gKl7Sk) (overkill!). This is more reliable than using any device that leverages a SD Card (in my opinion). If you are using a SD card, I highly encourage you, as your very first integration, to add the excellent [Google Drive Backup](https://github.com/sabeechen/hassio-google-drive-backup "Hass.io Google Drive Backup Add-on") for your installation files and set this to backup every day.

My [MQTT Broker](https://hub.docker.com/_/eclipse-mosquitto) is running on my [Synology NAS](https://amzn.to/34Swp4I) in a docker container along with a few other IoT components.
#### Gadgets
* 9 x [Shelly](https://amzn.to/3jwq2ba)1 (one integrated into mains powered outdoor PIR). Video [**here**](https://www.youtube.com/watch?v=M1o80liNrhs)
* 5 x Shelly PM1
* 1 x Shelly 2.5
* 2 x Shelly Dimmer
* 2 x ShellyEM
* 1 x Shelly Door/Window sensor
* 1 x [Smart Dimmer Switch by Martin Jerry](https://amzn.to/34TD26H) running custom Tasmota firmware by [digiblur](https://github.com/digiblur/Tasmota/tree/development/bins)
* 4 x Sonoff
* 5 x Sonoff POW
* 1 x Sonoff Dual
* 1 x Sonoff TH10 with temp probe
* 1 x Sonoff Zigbee DIY smart switch
* 1 x Sonoff RF Bridge (all running Tasmota)
* 1 x [OpenGarage](https://opengarage.io/) controller with Ultrasonic 'car-in-garage' detection
* 4 x Xiaomi Temperature and Humidity Sensors
* 5 x Xiaomi Motion Detectors
* 6 x Xiaomi Door and Window Sensors (integrated into IP65 boxes). Video [**here**](https://www.youtube.com/watch?v=eTgC9VP7Di8)
* 6 x Xiaomi Zigbee Smart Plugs with power monitoring (Soldering iron, Espresso machine, TV Cabinet, Office power...)
* 1 x Xiaomi Gateway used for doorbell, fire siren and nightlight
* 3 x Xiaomi buttons (Gen1 and Gen2) for running scenes
* 1 x Xiaomi wireless light switch
* 2 x Xiaomi Plant Sensors connected to:
* 1 x RPi Zero running [plantgateway](https://github.com/ChristianKuehnel/plantgateway) and [igrill-hassio](https://github.com/WilliamAlexanderMorrison/igrill-hassio)
* 1 x [Dresden Conbee II Zigbee Gateway](https://amzn.to/3jAXMUV) (currently running with deCONZ add-on)
* 1 x [Aeon Labs Z-Wave stick](https://amzn.to/3bipmDp)
* 2 x [Aeon Labs MultiSensor 6](https://amzn.to/3hWqjEg)
* 5 x Z-Wave in-wall switch modules
* 1 x [Yale Security Assure Lock with Z-Wave](https://amzn.to/2YVRDe1)
* 2 x Broadlink universal IR+RF remote control
* 1 x [QuinLED-Dig-Uno](https://quinled.info/2020/02/11/quinled-dig-uno-pre-assembled-available/) running [WLED](https://github.com/Aircoookie/WLED) connected to 12V Addressable LED's behind the Tele
* 1 x [Samsung Galaxy Tab A 10.1](https://amzn.to/3lBp9jL) running Fully Kiosk Browser. Video on that [**here**](https://www.youtube.com/watch?v=sv67ovOhjzQ).
#### Power Monitoring
* 1 x [Eastron SDM-220](https://s.click.aliexpress.com/e/_dVaddXe) DIN Rail MODBUS whole-house power monitoring module
* 1 x [USR-TCP232-410S](https://amzn.to/2YWPnUa) MODBUS to Ethernet converter for [connection to HA](https://www.home-assistant.io/integrations/modbus/)
#### Streaming
* 3 x [Echo Dot](https://amzn.to/31MuQTQ)
* 3 x Google Home  
* 4 x Google Home Mini  
* 3 x Chromecast  
* 4 x Chromecast Audio
* 1 x Odroid N2 running Kodi (CoreELEC) and Hyperion
* 1 x Android TV with [PiPup](https://play.google.com/store/apps/details?id=nl.rogro82.pipup&hl=en) installed which allows HA to send it messages and other content
* 1 x [Logitech Harmony Companion All in One Remote Control for Smart Home](https://amzn.to/2GlEQvd)
#### Security
* 1 x DSC 16-zone alarm panel with [Envisalink](https://amzn.to/2EZTckk) Ethernet interface for [connection to HA](https://www.home-assistant.io/integrations/envisalink/)
* 2 x Hikvsion G-Series 5MP H.265 Outdoor Dome Cameras integrated using [Hikvision](https://www.home-assistant.io/integrations/hikvision/) component
* 1 x Dahua SD22204T-GN Outdoor PTZ (integrated using [Amcrest](https://www.home-assistant.io/integrations/amcrest/) component)
* 3 x Dahua HDBW4431R-AS H.265 4MP IP Dome Cameras
* 1 x Synology Surveillance Station (running on RS814+) and integrated into HA using [SS platform](https://www.home-assistant.io/integrations/synology/)

#### Network
* 1 x [UniFi 24-port Gen2 PoE switch](https://amzn.to/2QLY7Ig)
* 1 x UniFi 24-port switch  
* 1 x UniFi 8-port PoE switch  
* 1 x UniFi 8-port switch  
* 2 x UniFi AC-Lite AP  
* 1 x [UniFi AC-Pro AP](https://amzn.to/2ELV7sI)
* 1 x UniFi USG 
* 1 x [Synology RS814+](https://amzn.to/34Swp4I) NAS (Docker: MQTT, TasmoAdmin, UniFi Controller and AdGuard)
* 1 x RPi3 running a 2nd AdGuard server as a [Ubuntu Appliance](https://ubuntu.com/appliance/adguard). Also running a backup MQTT broker
* 1 x [Smart-UPS X 1500](https://amzn.to/2DjRPME) with Network Management Card 2
### Integrations
* Alexa Media Player
* deCONZ
* Google Cast
* HACS
* HomeKit Bridge
* Logitech Harmony Hub
* Mobile App
* MQTT
* Samsung Smart TV
* Sony Bravia TV
* Sony Songpal
* Synology DSM
* Xiaomi Gateway (Aqara)
* Z-Wave
### Add-ons
* deCONZ
* [Hass.io Google Drive Backup](https://github.com/sabeechen/hassio-google-drive-backup "Hass.io Google Drive Backup Add-on"). **Must have!**
* MariaDB
* phpMyAdmin
* Samba share
* TasmoBackup
* Terminal & SSH
### HACS
#### Frontend
* [Alexa Media Player](https://github.com/custom-components/alexa_media_player)
* [Attributes](https://github.com/pilotak/homeassistant-attributes)
* [browser_mod](https://github.com/thomasloven/hass-browser_mod)
* [HACS](https://github.com/hacs/integration)
* [SmartIR](https://github.com/smartHomeHub/SmartIR)
#### Integrations
* [Bar Card](https://github.com/custom-cards/bar-card)
* [button-card](https://github.com/custom-cards/button-card)
* [Canvas Gauge Card](https://github.com/custom-cards/canvas-gauge-card)
* [card-mod](https://github.com/thomasloven/lovelace-card-mod)
* [card-tools](https://github.com/thomasloven/lovelace-card-tools)
* [Custom Header](https://github.com/maykar/custom-header) **Must have!**
* [Flexible Horseshoe Card for Lovelace](https://github.com/AmoebeLabs/flex-horseshoe-card)
* [Mini Graph Card](https://github.com/kalkih/mini-graph-card)
* [Search Card](https://github.com/postlund/search-card)
