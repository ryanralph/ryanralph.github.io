---
title: 'CNC Machine Summer Project update #0'
id: 78
categories:
  - cnc machine
  - cnc mill
  - Projects
  - raspberry pi
date: 2013-12-17 13:13:22
tags:
---

[caption id="attachment_81" align="aligncenter" width="1024"][![CNC machine electrical components](http://blog.ryanralph.net/wp-content/uploads/2013/12/IMG_20131217_021552058-1024x768.jpg)](http://blog.ryanralph.net/wp-content/uploads/2013/12/IMG_20131217_021552058.jpg) CNC machine electrical components[/caption]

# Overview

So as a project for the summer holidays I decided I'd build a 3 axis CNC machine for the primary purpose of milling PCBs and clear acrylic. After researching multiple different options I thought I had settled on building a [Shapeoko](http://www.shapeoko.com/), running out of funds for the [Shapeoko Mechanical kit](https://www.inventables.com/technologies/desktop-cnc-mill-kit-shapeoko-2) I am still contemplating what my options are.<!--more-->

# Bill of materials (so far):

Here's what I've settled on for the basis of my CNC machine:

*   1 x [tinyG stepper motor/CNC controller](https://synthetos.myshopify.com/products/tinyg)
*   2 x [60mm Computer fans](http://www.ebay.com.au/itm/161132396755?ssPageName=STRK:MEWNX:IT&amp;_trksid=p3984.m1439.l2649) (for cooling the tinyG)
*   1 x [12V Power supply](http://www.ebay.com.au/itm/270931958595?ssPageName=STRK:MEWNX:IT&amp;_trksid=p3984.m1439.l2649)
*   4 x [NEMA17 Stepper motors ](http://www.ebay.com.au/itm/200941636084?ssPageName=STRK:MEWNX:IT&amp;_trksid=p3984.m1439.l2649)(dual gantry axis)
*   4 x [Micro limit/home switches](http://www.ebay.com.au/itm/281113360488?ssPageName=STRK:MEWNX:IT&amp;_trksid=p3984.m1497.l2649)
*   1 x [12V step-down USB power supply](http://www.ebay.com.au/itm/130970751666?ssPageName=STRK:MEWNX:IT&amp;_trksid=p3984.m1439.l2649)
*   1 x [Emergency stop button](http://www.ebay.com.au/itm/161115573460?ssPageName=STRK:MEWNX:IT&amp;_trksid=p3984.m1439.l2649) (mostly because it looks cool)
*   All to be controlled with a raspberry pi.
At this point in time I've tested everything that I have. I was quite surprised by the motors strength and[ holding torque.](http://en.wikipedia.org/wiki/Stepper_motor#Detent_torque) To connect to the tinyg via USB I used the program "minicom". To connect to the tinyg I used the following command

    sudo minicom -b 115200 -o -D /dev/ttyUSB0`</pre>
    and then to move the motors I sent the following Gcode.
    <pre>`g0x50y50z50a50

which should make all the motors move clockwise. Changing the value following the x,y,z or a axes in that string will move the motor to that position which at this point in time has little meaning.

[![12V Power supply with IEC connector](http://blog.ryanralph.net/wp-content/uploads/2013/12/IMG_20131217_021618304-e1387209653458-225x300.jpg)](http://blog.ryanralph.net/wp-content/uploads/2013/12/IMG_20131217_021618304-e1387209653458.jpg)

The power supply didn't come with any wiring so to make do I connected a female IEC plug and can be powered up by a standard 240v computer IEC cable. When I eventually complete this project I intend to house all the electronics in a box and so I may retain this connector or move to a mounted one such as [this one from DX.com](http://dx.com/p/3-pin-diy-ac-power-socket-with-fuse-and-switch-black-5-piece-pcs-148790?).

The above parts will be able to be made into a custom cnc machine or a shapeoko. I'm currently waiting to hear from a friend who is undertaking a similar project but building the machine frame from scratch. Once I can compare his estimated price with the price of a Shapeoko Mechanical kit + $90 Shipping to Australia I will weigh up the pros &amp; cons. Until then....