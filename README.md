# webos-player
custom webos player for Home Assistant Lovelace

## Requirements
- [custom-button-card](https://github.com/custom-cards/button-card)
- [card-mod](https://github.com/thomasloven/lovelace-card-mod)
- [slider-entity-row](https://github.com/thomasloven/lovelace-slider-entity-row)

## Prerequisites
Almost a webos tv integrated in Home Assistant with customized sources
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



![wosp04](https://user-images.githubusercontent.com/47286900/135503828-a5a50469-71ab-4dca-bd35-f47422d25306.png)
![wosp05](https://user-images.githubusercontent.com/47286900/135503838-bd0fc489-81cb-4c75-a79f-405a5596cec3.png)
![wosp06](https://user-images.githubusercontent.com/47286900/135503851-3ff78571-b0b1-4d2f-a3ed-9a5b37e2a900.png)
![wosp03](https://user-images.githubusercontent.com/47286900/135503813-69e47c1d-cf89-4ae3-b569-e1ef61c07982.png)
![wosp09](https://user-images.githubusercontent.com/47286900/135503877-bd31ceb6-ee2a-41e4-a8ba-23b515ff88b6.png)
![wosp08](https://user-images.githubusercontent.com/47286900/135503867-4eaf1517-88dc-4a96-995a-1255e02381a6.png)
![wosp02](https://user-images.githubusercontent.com/47286900/135503789-744eed7a-a5f6-4137-8ffa-39bc92afb19f.png)
