# webos-player
A custom mod webos player compact size for Home Assistant Lovelace

![wosp04](https://user-images.githubusercontent.com/47286900/135503828-a5a50469-71ab-4dca-bd35-f47422d25306.png)
![wosp05](https://user-images.githubusercontent.com/47286900/135503838-bd0fc489-81cb-4c75-a79f-405a5596cec3.png)
![wosp06](https://user-images.githubusercontent.com/47286900/135503851-3ff78571-b0b1-4d2f-a3ed-9a5b37e2a900.png)
![wosp03](https://user-images.githubusercontent.com/47286900/135503813-69e47c1d-cf89-4ae3-b569-e1ef61c07982.png)
![wosp09](https://user-images.githubusercontent.com/47286900/135503877-bd31ceb6-ee2a-41e4-a8ba-23b515ff88b6.png)
![wosp08](https://user-images.githubusercontent.com/47286900/135503867-4eaf1517-88dc-4a96-995a-1255e02381a6.png)
![wosp02](https://user-images.githubusercontent.com/47286900/135503789-744eed7a-a5f6-4137-8ffa-39bc92afb19f.png)

# Features
* navigator pad
* keynumber pad
* sources selector
* favorite channels selector
* channel up/down
* play/pause
* forward/rewind
* volume slider
* volume value
* volume mute button
* home, back, exit buttons
* settings, channels list, info buttons
* color buttons
* channel logo background
* source image background
* power on/off
* channel/source name label
* input text to write, notify or web search

## Requirements
- [custom-button-card](https://github.com/custom-cards/button-card)
- [card-mod](https://github.com/thomasloven/lovelace-card-mod)
- [slider-entity-row](https://github.com/thomasloven/lovelace-slider-entity-row)

## Prerequisites
At least one webos tv integrated in Home Assistant with customized sources
```
webostv:
  - name: my_tv
    host: !secret my_tv_ip
    turn_on_action:
      service: wake_on_lan.send_magic_packet
      data:
        mac: !secret my_tv_mac
    customize:
      sources:
        - Browser Web 
        - Live TV   
        - HDMI 1
        - ...
```
## Instructions
1. Download **tv_logos** into ' **www/** ' folder, add here yours tv logos with **.png** extension
2. Add the webos player custom template **wosp-template.yaml** to **button_card_templates:**
3. #### Set wosp entities for one webos tv
   Add a package **wosp-package.yaml**  into the packages folder, and rename it for the specific tv.  
   E.g.: *wosp-package_my_tv.yaml* or *wosp-package_bedroom.yaml* or *wosp-package_livingroom.yaml*.  
   Into the renamed package:
     * replace all occurences of **WOSP_ENTITY** with the webos media_player object_id.  
       E.g.: media_player.**bedroom_tv** --> replace **WOSP_ENTITY** with **bedroom_tv**
     * edit your favorite channels after **'favorites'** field
       E.g.:
       ```
         options: >
           {{ [
             'favorites'
           , 'channel 1'
           , 'channel 2'
           , 'channel 3' ] }}
       ```
    Repeat step 3 for every tv device
### Troubleshooting
if you have a webos version x, replace "Live TV" with correct name of channels source
Ex: for italian language is "Canali TV"


