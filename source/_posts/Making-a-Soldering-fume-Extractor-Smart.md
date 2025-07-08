---
title: 'Smart Home Mod: Automating a Solder Fume Extractor with ESPHome'
tags:
  - Smart Home
  - ESPHome
  - Home Assistant
  - ESP8266
  - Wemos D1
  - Soldering
desc: >-
  This post shows how I added smart controls to a Vevor solder fume extractor
  using ESPHome, allowing full automation and voice/app control via Home
  Assistant.
date: 2025-07-08 13:12:11
---


![Vevor 150W Fume Extractor](images/vevor-fume-extractor/vevor-fan-product-photo.jpg)

Up until recently, I've not been doing lots of soldering at home and didn't have a proper solution for fume extraction. With the increased work I decided to buy this fume extractor from [Vevor](https://www.vevor.com.au/plasma-cutter-c_10061/vevor-150w-solder-fume-smoke-extractor-3-stage-filters-332-m3-h-strong-suction-p_010981971654). <!--more--> So far, it's been pretty good to work with. Like some others online I don't like that the button is so low down when you have the fan sitting on the floor. Compounding the issue, the unit usually rolls away while trying to adjust the speed up and down. To fix this, I decided to modify it and add it to my Home Assistant Smart Home allowing phone app and voice control.

## Operation
The momentary switch toggles the fan speed from Off -> Low -> Medium -> High -> Off. Feedback is provided to the user by changing from a Flashing Red light to Solid Blue Green or Red. To simulate pressing the button I added the relay across the switch. I decided it's not necessary to monitor the LED for feedback and assume that the button press is always registered accurately. It is possible for the physical switch and the Home assistant component to get out of sync. Now that it's controlled from the smart home setup I have no real need to use the manual switch.

## Modifications
I took the base off and the architecture is fairly simple. 

![Internals of Vevor Fume extractor](images/vevor-fume-extractor/inside-extractor-fan-enclosure.jpg)

The power for the DC regulator is picked up from the main PCB (red wires) and the relay goes across the switch from the NO and COM terminals (white wires). 

![](images/vevor-fume-extractor/extractor-pcb-solder-locations.jpg)

## Parts used
- [Wemos D1 mini](https://s.click.aliexpress.com/e/_oCurdvM) (USB C versions have started to come out now)
- [Relay shield](https://s.click.aliexpress.com/e/_oktNcYA)
- [AC to DC Step down converter (230VAC to 5VDC)](https://s.click.aliexpress.com/e/_oml0lHM)


## Code
[ESPHome .yaml file](https://gist.github.com/ryanralph/d77c45ab71a5f36806d0d3f197a48bdf)

```
#Excerpt from https://gist.github.com/ryanralph/d77c45ab71a5f36806d0d3f197a48bdf
fan:
  - platform: template
    name: "Fan"
    id: extraction_fan
    speed_count: 3  # 1=Low, 2=Med, 3=High
    on_turn_on:
      - if:
          condition:
            lambda: 'return id(fan_state) == 0;'
          then:
            - lambda: |-
                id(fan_state) = 1;
                id(int_fan_speed) = id(extraction_fan).speed;
            - script.execute: sync_fan_state
    on_speed_set:
      - lambda: |-
          id(int_fan_speed) = id(extraction_fan).speed;
      - script.execute: sync_fan_state
    on_turn_off:
      - lambda: |-
          id(int_fan_speed) = 0;
          id(fan_state) = 0;
      - script.execute: sync_fan_state
```

## Home Assistant
Using an ESPHome Fan component and some custom lambda script, the relay is toggled the correct number of times to achieve the requested speed.
![The result in Home Assistant](images/vevor-fume-extractor/HomeAssistantUI.gif)

## Further work
To make this all a bit neater I have a few extra HA Automations to tie it all together. My goal is to only minimally use the HA app, and everything "just work" (TM). The extraction fan is on constant power and my Soldering station is all connected to a power board via a smart power monitoring plug.

- Automation #1: Turn On/Off the smart plug for my soldering bench with the Shed lights. This means that if I forget to turn off the soldering station it will spend less time in sleep mode. 

- Automation #2: If the Soldering bench plug's power draw is above a threshold, turn on the extraction fan. 

- Automation #3: If the Soldering bench plug's power draw is below a threshold for over a minute, turn OFF the extraction fan.

This combination of Automations works for my soldering iron, desoldering and hot air stations. Let me know if you want the .YAMLs, this is usually just easier to set up from the UI nowadays.

## Video

{% youtube dKqJysCQ_qM %}
You can hear the relay click on shortly after I pick up the soldering iron

## Links
[Home Assistant](https://www.home-assistant.io/) - Well worth the $5USD paid subscription. 
[ESPHome](https://esphome.io) - This documentation is some of the best out there, well done to the developers.