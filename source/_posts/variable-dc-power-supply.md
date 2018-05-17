---
title: Variable DC Power Supply Build
tags:
  - power supply
  - project
  - projects
id: 312
categories:
  - power supply
  - Projects
  - Ramblings
date: 2015-06-30 10:00:29
---

[caption id="attachment_324" align="aligncenter" width="672"]![Power supply front panel: voltage adjust and current limit potentiometer knobs somewhere between China and AU](http://blog.ryanralph.net/wp-content/uploads/2015/06/edited-IMG_20150617_220515-e1434684259498.jpg) front panel: voltage adjust and current limit potentiometer knobs somewhere in transit between China and AU[/caption]

So I've wanted a reliable bench power supply for a long time and it's always been on the "to-do" list. As I've learned more and more about electronics I've considered building one at different stages and now I've finally done it.<!--more-->

## Planning

Originally I'd planned to build a power supply from an old ATX supply [like](http://www.makeuseof.com/tag/how-to-make-a-bench-power-supply-from-an-old-atx-psu/) [many](http://makezine.com/projects/computer-power-supply-to-bench-power-supply-adapter/) [have](http://www.wikihow.com/Convert-a-Computer-ATX-Power-Supply-to-a-Lab-Power-Supply) [done](http://www.instructables.com/id/ATX--%3E-Lab-Bench-Power-Supply-Conversion/) [before](https://www.youtube.com/watch?v=z2oSFpKh_Uw). In order to set this up with binding posts with a safe clearance was not going to be possible with the spare ATX supply I have. This also made the idea of adding an LM317 into the ATX supply to get ~12V adjustable was not going to happen without constructing a completely new enclosure.

[caption id="" align="aligncenter" width="497"][![Converted ATX bench power supply](http://lowpowerlab.com/wp-content/uploads/2013/01/ATX_bench_supply_finished_labels.jpg)](http://lowpowerlab.com/blog/2013/01/18/simple-atx-bench-power-supply/) Converted ATX bench power supply[/caption]

After realising this wasn't going to work, I explored the option of using LM7805 and similar LM78xx fixed linear regulators to give myself a number of fixed DC voltages to play with.  During this phase I learned about the LM317 variable linear regulator and was convinced a combination of an LM317 variable voltage with some fixed voltages (5V, 9V and 12V)  was the way to go. This never eventuated partially due to the current limitations of these linear regulators and partially due to my hate of perfboard/prohibitive cost of PCB manufacture.

[caption id="" align="aligncenter" width="360"][![LM317 variable voltage supply, image from electronics-lab.com. Click to see the LM317 calculator](http://www.electronics-lab.com/articles/LM317/LM317.gif)](http://www.electronics-lab.com/articles/LM317/) LM317 variable voltage supply, image from electronics-lab.com[/caption]

Just this semester we've been learning about buck/boost converters (having only studied buck converters in the past) and in researching DC-DC converters I came across the [LTC3780](http://lmgtfy.com/?q=LTC3780) which I've finally gone ahead and built a power supply from.

[caption id="" align="aligncenter" width="300"][![LTC3780 module](http://ecx.images-amazon.com/images/I/51cLKt543pL._SX300_.jpg)](http://ecx.images-amazon.com/images/I/51cLKt543pL._SX300_.jpg) LTC3780 module[/caption]

Utilising the Buck/Boost configuration allows for stepping up and down from the input voltage supplied to the module. Other reasons this module has been selected is that it allows control of the output current using a trimpot as well as just a generally higher limit on the current output when compared to the LM series voltage regulators limited to 1A.

## Parts

*   [LTC3870 module](http://www.ebay.com.au/itm/251768965445?_trksid=p2060353.m2749.l2649&amp;ssPageName=STRK%3AMEBIDX%3AIT) - $25
*   [12V "led strip"power supply](http://www.ebay.com.au/itm/281631151355?_trksid=p2060353.m2749.l2649&amp;ssPageName=STRK%3AMEBIDX%3AIT) - $10
*   [Voltmeter/Ammeter combo](http://www.aliexpress.com/item/DC-3-5-30V-0-50A-Dual-LED-Digital-Volt-meter-Ammete-Voltage-AMP-Power-free/1603140893.html) - $5
*   Binding posts for banana Jacks (I already had some [black](http://aud.dx.com/product/jtron-4mm-binding-post-jack-for-banana-plug-test-probe-connector-black-10-pcs-961386164)/[red](http://aud.dx.com/product/jtron-4mm-binding-post-jacks-for-banana-plug-test-probe-connector-red-10-pcs-961386465)) - $1.20
*   [500k Potentiometer](http://www.ebay.com.au/itm/250939933959?_trksid=p2060353.m2749.l2649&amp;ssPageName=STRK%3AMEBIDX%3AIT) - $1.00
*   [200k Potentiometer](http://www.ebay.com.au/itm/250939934330?_trksid=p2060353.m2749.l2649&amp;ssPageName=STRK%3AMEBIDX%3AIT) - $1.00
*   [Potentiometer knobs](http://www.ebay.com.au/itm/141544409464?_trksid=p2060353.m2749.l2649) - $0.40
*   [IEC 240V input &amp; switch ](http://www.ebay.com.au/itm/141544409464?_trksid=p2060353.m2749.l2649)- $2.00
*   [Enclosure](http://www.jaycar.com.au/Enclosures-%26-Panel-Hardware/Plastic-Boxes/Instrument/Pro-Quality-Instrument-Case---200-x-160-x-70mm/p/HB5912) - $15.00
*   [fuse holder](http://www.ebay.com.au/itm/New-5Pcs-Black-AC-15A-125V-Screw-Cap-Panel-Mounted-5-x-20mm-Fuse-Holder-/221551511558?pt=LH_DefaultDomain_15&amp;hash=item33957fc806) (already had one) - $0.40
**Total cost: **$61.00

## Construction

[gallery ids="329,328,327,326,341"]

Assembling this power supply was not difficult in the slightest. The modular nature of this power supply means that it was essentially wiring together the individual components.  Most of the assembly time was spent using the rotary tool to shape out the front/back panel holes. As can be seen from the above photos

It should also be noted that the voltmeter/ammeter that I purchased was slightly different to the one in the picture and did not require an external shunt. To wire the meter

## Accuracy

The voltmeter is a few hundred mV out when the voltage is lower (0-15V) above this can be up to 1V out at the higher end of the scale (20-28V). My measurements can be seen in the following photos.

[gallery ids="339,332,331,337,338,336,335,334,320,318"]

It's not the best or cheapest or most well constructed power supply out there but it's good enough for me right now.