---
title: '3d Printer Prusa i3 build log #0'
tags:
  - 3d printer
  - 3d printing
  - projects
  - prusa i3
  - reprap
id: 273
categories:
  - 3d printer
  - 3d printing
  - Projects
  - prusa i3
  - reprap
date: 2015-04-11 01:15:02
---

[caption id="attachment_274" align="aligncenter" width="814"]![](http://blog.ryanralph.net/wp-content/uploads/2015/04/IMG_20150410_1234142-2048x984.jpg) Still missing a few things[/caption]

&nbsp;

I've decided to get into the 3d printing space and decided to build a reprap P[rusa i3](http://reprap.org/wiki/Prusa_i3). Based on community feedback it seems like a good solid printer for a first timer as well as relatively accessible in terms of acquring parts. I've spent a fair bit of time trawling ebay and aliexpress in order to pick up all the parts. Hopefully I can keep the total sub $500.<!--more-->

This post will be my list of parts I've bought, how much they cost me in $AUD, not necessarily a complete BOM. I will try and keep it up to date and <del>strike out</del> things I haven't used.

## Rods

*   2x Smooth rod Ø8x320 mm - Purchased as a kit from [Fabricature](http://www.fabricature.com.au/home/5-8mm-smooth-rod-set.html) $30
*   2x Smooth rod Ø8x350 mm
*   2x Smooth rod Ø8x370 mm
*   2x Threaded rod M5x300 mm- Purchased as a kit from [Fabricature](http://www.fabricature.com.au/home/9-threaded-rod-pack.html) $17
*   4x Threaded rod M10x210 mm
*   2x Threaded rod M10x380 mm
**section cost:** $37

## Movement

*   12x Linear LM8UU bearing - [Aliexpress](http://www.aliexpress.com/wholesale?catId=100004738&amp;initiative_id=AS_20150705191436&amp;SearchText=lm8uu) ~$12
*   2x 5mm-5mm coupler - [Aliexpress](http://www.aliexpress.com/item/20pcs-lot-3D-printer-Stepper-Motor-Flexible-Coupling-Coupler-Shaft-Couplings-5-mm-5mm-25-mm/1906345631.html) ~$3
*   10x 623ZZ bearing - [Aliexpress](http://www.aliexpress.com/item/10PCS-Miniature-Radial-Ball-Bearings-3x10x4mm-623ZZ-for-RC-Car-Practical-E-CH/1883811211.html) ~$3
*   5x 608ZZ bearing - [Aliexpress](http://www.aliexpress.com/item/5-pcs-ABEC-7-Deep-groove-ball-bearing-608ZZ-8X22X7-mm-bearing-steel-608-ZZ-skating/32262758570.html) ~$2.50
*   5x Nema17 stepper motors - [learcnc](http://www.ebay.com.au/itm/LearCNC-5x38mm-Nema17-Stepper-Motor-RepRap-CNC-Prusa-Arduino-RAMPS-3D-Printer-/200941639918?pt=LH_DefaultDomain_15&amp;hash=item2ec90e18ee) $70
*   2m GT2 belt - [Aliexpress](http://www.aliexpress.com/item/2Pcs-20-GT2-6-GT2-Pulley-And-2m-GT2-6mm-Open-GT2-Belt-for-3D-printer/2013340116.html) ~$5
*   2x GT2 Pulleys - comes with belt
**section cost: **$95.50

## Heatbed

*   PCB Heatbed - [Aliexpress](http://www.aliexpress.com/item/3D-Printer-Parts-MK2B-Heatbed-LED-Resistor-Cable-100K-ohm-Thermistors-PCB-Heated-Bed-White-Red/32268174955.html) ~$12
*   Glass plate - [Aliexpress](http://www.aliexpress.com/item/Free-shipping-3d-printer-ReprapMK2-Borosilicate-glass-for-headbed-size-213-200-3mm/1313851457.html) ~$19
*   Kapton tape - [Aliexpress](http://www.aliexpress.com/item/Free-shipping-width-50mm-rapid-prototyping-three-dimensional-printer-makerb-reprap-heat-resistant-tape-high-quality/802337815.html) ~$10
*   20x 100k Thermistor - [Aliexpress](http://www.aliexpress.com/item/20pcs-Lot-Thermistor-NTC-MF52AT-100K-3950-100K-B-Value-3950-1-Free-Shipping-YXSMDZ1758/32269217776.html) ~$3
*   Binder clips - Already had some
**section cost: **$44

## Electronics

*   1x RAMPS 1.4 + 1x Arduino mega + 4x pololu drivers - [Aliexpress](http://www.aliexpress.com/item/1pcs-Mega-2560-R3-for-arduino-1pcs-RAMPS-1-4-Controller-5pcs-A4988-Stepper-Driver-Module/1609138057.html) ~$26
*   3x Endstops - [Aliexpress](http://www.aliexpress.com/item/Endstop-Switch-Kit-For-CNC-3D-Printer-RepRap-Makerbot-Prusa-RAMPS1-4/32265951397.html) ~$5
*   RAMPS LCD - [Aliexpress](http://www.aliexpress.com/item/3D-printer-reprap-smart-controller-Reprap-Ramps-1-4-2004LCD-control/2044279389.html) ~$15 (I had a dispute with the seller of the one I bought cause he didn't include the "smart adapter + cables", knocked price down to about $7.50 after refund. The link is to a different seller)
*   RAMPS LCD "smart adapter" - [Aliexpress](http://www.aliexpress.com/item/Smart-Adapter-for-3D-Printer-Ramps-2004-LCD-controller-2pcs-20cm-Dupond-Calbe-Wire-Line-FZ0322/1966576840.html) ~$5 (not necessary if you buy as a kit)
*   1x Power Supply (12V)  - thought I had one and turns out it was 24V 10A which isn't quite suitable Went with the 30A one from [aliexpress](http://www.aliexpress.com/item/DC-12V-2A-5A-8-5A-10A-15A-20A-30A-Switch-Power-Supply-Adapter-Transformer-AC/32315016017.html) ~$35
**section cost: **$81

## Hardware

I bought a lot, probably too much. I definitely doubled up on some stuff which I've left off the total.

### Washers

*   30 x M3 washers (6 for Z motor mounts 2 for Y belt mount, 8 for bed mount to PCB) - [Aliexpress](http://www.aliexpress.com/item/Authentic-304-stainless-steel-flat-washer-washer-screw-bolts-Rose-Accessories-M3-7-0-5mm-30/1866629339.html) ~$2.50
*   10 x M8 washers (X and Y idlers)  - [ebay](http://www.ebay.com.au/itm/161008508781?_trksid=p2060353.m2749.l2649&amp;var=460166594012&amp;ssPageName=STRK%3AMEBIDX%3AIT) ~$1.50
*   40 x M10 washers (y frame) - [ebay](http://www.ebay.com.au/itm/161008508781?_trksid=p2060353.m2749.l2649&amp;var=460166594013&amp;ssPageName=STRK%3AMEBIDX%3AIT) ~$4
*   20 x M4 flat washers - [Masters](https://www.masters.com.au/) $2

### Nuts

*   4 x M3 nyloc nuts (bed mount to PCB) - [aliexpress](http://www.aliexpress.com/item/Low-price-1-piece-Metric-M3-201-Stainless-Steel-Hex-Head-Nylon-Insert-Lock-Jam-Stop/1986593775.html) ~$2
*   20 x M5 nuts (Z axis drive nuts) - [Bunnings](http://www.bunnings.com.au/) ~$3
*   10 x M8 nyloc nuts (X and Y idlers) - [Bunnings](http://www.bunnings.com.au/) ~$3
*   40 x M10 nuts (y frame) - [Bunnings](http://www.bunnings.com.au/) ~$13.50
*   10 x M4 nuts (for extruder) - [aliexpress](http://www.aliexpress.com/item/Low-price-1-piece-Metric-M4-Corrosion-Resisting-Stainless-steel-Nuts/1986378478.html) ~$1.50
*   50 x M3 nuts - [aliexpress](http://www.aliexpress.com/item/Low-price-1-piece-Metric-M3-Corrosion-Resisting-Stainless-steel-Nuts/1986271831.html) ~$2.50

### Bolts

*   20 x M3 x 8mm socket cap bolts (6 for Z motor mounts, 2 for Y motor mounts) - [ebay](http://www.ebay.com.au/itm/131303547918?_trksid=p2060353.m2749.l2649&amp;var=430600215065&amp;ssPageName=STRK%3AMEBIDX%3AIT) ~$1.50
*   20 x M3 x 10mm socket cap bolts ( 2 for Y belt mount, 10 for Z rod holder to i3 frame ) - [ebay](http://www.ebay.com.au/itm/131303547918?_trksid=p2060353.m2749.l2649&amp;var=430600215066&amp;ssPageName=STRK%3AMEBIDX%3AIT) ~$1.50
*   20 x M3 x 20mm bolts (bed mount to PCB)  - [ebay](http://www.ebay.com.au/itm/131303547918?_trksid=p2060353.m2749.l2649&amp;var=430600215070&amp;ssPageName=STRK%3AMEBIDX%3AIT) ~$2
*   50 x M3 x 14mm socket cap bolts - [aliexpress](http://www.aliexpress.com/item/Low-price-1-piece-Metric-Thread-M3-14mm-Stainless-Steel-Hex-Socket-Bolt-Screws/2002296562.html) $4
*   5 x M8 x 30mm bolts ( X and Y idlers) - [ebay](http://www.ebay.com.au/itm/361161108587?_trksid=p2060353.m2749.l2649&amp;var=630513141156&amp;ssPageName=STRK%3AMEBIDX%3AIT) ~$5
*   2 x M4 x 50mm bolts + nuts (extruder, couldn't find socket cap bolts. Hope it's ok)  - [Masters](https://www.masters.com.au/) $2
*   10 x M4 20mm bolts - [Ebay](http://www.ebay.com.au/itm/161229738851?_trksid=p2060353.m2749.l2649&amp;var=460278418978&amp;ssPageName=STRK%3AMEBIDX%3AIT)  ~$1.50
*   10 x m3 60mm socket cap bolt - [aliexpress](http://www.aliexpress.com/item/10PCS-M3x60mm-M3-60mm-3mm-60-STAINLESS-STEEL304-A2-Socket-Cap-Allen-Head-Screw-din912-fastener/32291327183.html) $13

### Other hardware

*   4 x M3 8mm standoffs (bed spacer above Y carriage to bed)  - [ebay](http://www.ebay.com.au/itm/221706842514?_trksid=p2060353.m2749.l2649&amp;ssPageName=STRK%3AMEBIDX%3AIT) ~$3
*   4 x M3 8mm grub screw - [aliexpress](http://www.aliexpress.com/item/Low-price-1-piece-M3-8mm-Head-Hex-Socket-Set-Grub-Screws-Metric-Threaded-Cup-Point/2012671258.html) ~$1.50
*   2 x M8 grub screw (for extruder + a spare for good measure) - [aliexpress](http://www.aliexpress.com/item/Low-price-1-piece-M8-20mm-Head-Hex-Socket-Set-Grub-Screws-Metric-Threaded-Cup-Point/2012776292.html) ~$1.50
**section cost:** $72

Definitely should have considered a kit instead of hardware individually. That said now I have plenty of spare stuff to use for other stuff, not a complete waste.

## Core parts

*   Hotend - [Aliexpress](http://www.aliexpress.com/item/FreeShipping-Long-distance-3D-Printer-J-head-Hotend-for-1-75mm-3-0mm-E3D-Bowden-Extruder/2041826923.html) ~$12 (Will be buying a much better non-clone hotend in the very near future)
*   Frame - sourced locally $??
*   Printed parts (prusa i3 rework + extruder) - [Ebay](http://www.ebay.com.au/sch/sonyapardue2013/m.html?_nkw=&amp;_armrs=1&amp;_ipg=&amp;_from=) ~$55 on special
*   Extruder - included in printed parts
**section cost:** $67

## Other

*   Hobbed bolt - [Aliexpress](http://www.aliexpress.com/item/2pcs-lot-3-D-printer-accessory-Wade-s-extruder-hobbed-bolt-reprap-M8-wire-feed-teeth/1564323966.html) ~$3
*   springs for [anti-backlash z axis](https://www.thingiverse.com/thing:694575) mod -  [Aliexpress](http://www.aliexpress.com/item/10pcs-lot-3-D-printer-accessory-feeder-spring-for-Ultimaker-Makerbot-Wade-extruder-nickel-plating-1/1830997495.html) ~$2.50
*   2x 40mm fan - [Ebay](http://www.ebay.com.au/itm/281489819644?_trksid=p2060353.m2749.l2649&amp;ssPageName=STRK%3AMEBIDX%3AIT) ~$3
*   bed springs - [Ebay](http://www.ebay.com.au/itm/251311542351?_trksid=p2060353.m2749.l2649&amp;ssPageName=STRK%3AMEBIDX%3AIT) ~$4
*   Hotend bracket - [Ebay](http://www.ebay.com.au/itm/141563289751?_trksid=p2060353.m2749.l2649&amp;ssPageName=STRK%3AMEBIDX%3AIT) ~$3
*   E-stop switch  - [Ebay](http://www.ebay.com.au/itm/NC-N-C-Emergency-Stop-Switch-Push-Button-Mushroom-Push-Button-4Screw-Terminal-BY-/200991693247?pt=LH_DefaultDomain_15&amp;hash=item2ecc09d9bf) ~$2
*   2x spare pololu drivers - [Aliexpress](http://www.aliexpress.com/item/1pc-Reprap-Stepper-Driver-pololu-A4988-stepper-motor-driver-module-with-aluminum-heat-sink-for-ramps/32296096239.html) ~$3
*   Timing belt tensioners - [Aliexpress](http://www.aliexpress.com/item/Free-shipping-3D-printer-accessories-Timing-Belt-Tensioner-Spring-RepRap-3D-Printer-Ultimaker-MendelMax-Prusa/2010865548.html) ~$5 (not necessary but I want to experiment)
*   Wiring kit - [AliExpress](http://www.aliexpress.com/wholesale?catId=0&amp;initiative_id=SB_20150923213146&amp;SearchText=ramps+wiring) ~$7
*   Cable ties - Have plenty on hand varying sizes is good, more colours is better.
*   Cable management - [ebay](http://www.ebay.com.au/itm/141125136332?var=440214632089) ~$2
**section:** $35.50

**Grand total: **$432 before frame

## Conclusion

There definitely needs to be room in the budget for another hotend and potentially in the future nicer smooth rods. I think with the parts I've purchased I should have a better (and cheaper) prusa i3 than any of the kits available in Australia or any of the international kits + postage.

&nbsp;

### Acknowledgements

[http://reprap.org/wiki/JBFromOZ#JBFromOZ.27s_recommended_i3_Build](http://reprap.org/wiki/JBFromOZ#JBFromOZ.27s_recommended_i3_Build)

[https://www.reddit.com/r/shittykickstarters/comments/2xctsf/35k_for_a_3d_printer_no_you_dont_get_the_printer/cozlwix](https://www.reddit.com/r/shittykickstarters/comments/2xctsf/35k_for_a_3d_printer_no_you_dont_get_the_printer/cozlwix)