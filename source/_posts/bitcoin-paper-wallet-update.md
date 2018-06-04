---
title: Bitcoin Paper Wallet Printer Update
tags:
  - bitcoin
  - linux
  - project
  - python
  - raspberry pi
id: 205
categories:
  - bitcoin
  - Projects
  - python
  - raspberry pi
date: 2014-08-13 07:29:11
---

![DIY Piper mounted in hobby box](/images/bitcoin-paper-wallet-update.jpg)
So I said I'd be back with an update on my DIY Piper bitcoin wallet printer and here is a quick rundown.<!--more-->

I've added all my changes to the git repo I set up at [github](https://github.com/ryanralph/DIY-Piper). Since the previous post I've completed the basic circuit to allow for power/status LEDs, a remember/forget switch, shutdown button and importantly the print button. If anyone is interested I can provide a breakdown of the circuit used.

Some changes since last time and tips:
-Changed all relative file paths to exact
-use /dev/urandom to source randomness instead of /dev/random
-symbolically linked vanitygen to /usr/bin ($ sudo ln -s /home/pi/DIY-Piper/vanitygen /usr/bin)
-Forced the pi to autologin and execute scripts by editing /etc/inittab and /etc/profile (info sourced from [here](http://www.opentechguides.com/how-to/article/raspberry-pi/5/raspberry-pi-auto-start.html)

It's not pretty, it's definitely not beautiful but it's mine and it's working.
