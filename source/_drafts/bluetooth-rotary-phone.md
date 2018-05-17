---
title: DIY Bluetooth Rotary phone
tags:
  - arduino
  - bluetooth
  - project
  - projects
id: 346
categories:
  - arduino
  - bluetooth
  - Projects
  - Ramblings
---

[caption id="attachment_357" align="aligncenter" width="300"]![Bell rotary telephone goes bluetooth](http://blog.ryanralph.net/wp-content/uploads/2015/06/edited-IMG_20150324_091636-300x225.jpg) Bell rotary telephone goes bluetooth[/caption]

The idea was to create a bluetooth rotary phone module that can be plugged in using the regular RJ-11 plug and require no modification of the internal phone circuitry

## Generating a ringing tone

DC-DC boost converter

555 timer to generate 20Hz [calculator #1](http://www.ohmslawcalculator.com/555-astable-calculator) + [calculator #2](http://houseofjeff.com/555-timer-oscillator-frequency-calculator/)

Take output of 555 timer and put it through a [transistor NOT gate](http://www.dummies.com/how-to/content/electronics-projects-how-to-create-a-transistor-no.html). Take output from 555 and inverted output from the NOT gate to the SN754410NE H bridge driver IC

Output from each of the "motor" pins from the IC go to the phone ringer solenoid.

Only turn on when arduino says to.

&nbsp;

## Bluetooth Audio + GPIO

RN-52 handles sending/receiving audio

&nbsp;

## Arduino Logic

Listen for GPIO output from RN-52 when the mobile phone is ringing.

Interpret Rotary dialer and place calls. Also would like to implement a speed dial.

No bluetooth rotary phone is complete without bluetooth rotary phone bluetooth rotary phone