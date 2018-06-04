---
title: RMIT University and eduroam wifi on linux
tags:
  - arch
  - arch linux
  - linux
  - RMIT
  - wifi
  - wpa_supplicant
id: 569
categories:
  - Linux
date: 2015-10-24 00:09:06
---

![RMIT University Logo - how to use RMIT wpa_supplicant with arch linux](/images/rmit-university-and-eduroam-wifi-on-linux.png)

Using arch linux and wpa_supplicant is sometimes a pain when you want to do something outside of the norm.<!--more--> Here is my wpa_supplicant.conf for RMIT University and other eduroam wifi hotspots.

```
# wpa_supplicant.conf
# https://gist.github.com/ryanralph/0778a9f65d76429be117
network={
        ssid="RMIT-University"
        key_mgmt=WPA-EAP
        eap=PEAP
        phase2="auth=MSCHAPV2"
        identity="s123456"
        password="MADSECUREPASSWORD HERE"
}
```
For non RMIT based eduroam hotspots just change the SSID.
