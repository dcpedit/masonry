<p align="center">
  <img src="https://i.imgur.com/Gbr6AGb.png" width="350"/>
</p>

# Masonry Keyboard

Inspired by [Bruce the Keyboard](https://www.jlw-kb.com/products/bruce-the-keyboard-the-pcb), this is a 12 column version with a less aggressive stagger.

Schematic for the STM32F072 integration was taken from Sleepdealer's [OSFRL project](https://github.com/Sleepdealr/OSFRL)

<img src="https://i.imgur.com/gqx2FZW.jpeg">

Here are the supported layouts:
[Keyboard Layout Editor](http://www.keyboard-layout-editor.com/#/gists/711e40adc1aee2aae4437fc2fe2fa7aa)

<img src="https://i.imgur.com/1glctV2.png" width="350">

## Ordering PCBs from JLCPCB

<img src="https://i.imgur.com/aYG5wqO.jpeg" width="350">
<img src="https://i.imgur.com/cKCbLxw.jpeg" width="350">

The files needed for https://jlcpcb.com are located in the production folder:

* `pcb/production`

Once `pcb.zip` has been uploaded, you can continue with the selected default options. You can optionally change the solder mask color, which changes the final color of your PCB.

When using their assembly service, you will need to upload the following files separately:

* `bom.csv`
* `positions.csv`

These files were all generated with Fabrication Toolkit for KiCad: https://github.com/bennymeg/Fabrication-Toolkit

## Stacked Acrylic Case

<img src="https://i.imgur.com/esxFbJ7.jpeg" width="350">
<img src="https://i.imgur.com/V5y3ilx.jpeg" width="350">
<img src="https://i.imgur.com/Wzzb6x3.png" width="350">

Case file is in the `assets` folder.

### Parts List
| Description | Qty | Notes |
| ----------- | --- | ----- |
| 3mm acrylic | 7 | Qty = number of case layers
| 1.5mm acrylic | 1 | Switch plate
| M3x20mm chicago bolt | 6 | [Link](https://www.aliexpress.us/item/2251832451307213.html)
| M3x10mm chicago bolt | 1 | [Link](https://www.aliexpress.us/item/2251832451307213.html)
| M3x6mm screw | 1 - 6 | [Link](https://www.aliexpress.us/item/2255800885711092.html)
| M2x4mm round standoff | 7 | [Link](https://www.aliexpress.us/item/2251832782591461.html)
| M2x3mm screw | 7 | [Link](https://www.aliexpress.us/item/2255800480170108.html)
| M2x4mm screw | 7 | [Link](https://www.aliexpress.us/item/2255800480170108.html)
| 1mm EVA foam | 1 | Case foam
| 1.5mm EVA foam | 1 | Switch plate foam, [link](https://www.aliexpress.us/item/3256804208838525.html)
| 2mm EVA foam | 1 | Switch plate foam
| MX Switch | 38 - 44 |
| Adhesive rubber feet | 4 

Keycap sizes will depend on the layout you're building (refer to KLE layout above).  Blank uniform-profile keycaps works really great for this keyboard since the keys have a vertical orientation.  I found my blank XDA PBT keycaps on AliExpress.  The specific ones I use in my build were purchased [here (1u - 2u)](https://www.aliexpress.us/item/3256804203440964.html) and [here (3u)](https://www.aliexpress.us/item/3256801190573750.html).

| Keycap | Qty |
| ------ | --- |
| 1u | 18 - 28
| 1.25u | 8
| 1.5u | 4
| 1.75u | 4
| 2u | 0 - 4
| 3u | 0 - 2

### Assembly

The M3 hardware is for the keyboard case.  The shorter M3 fastener goes above the USB connector.  You will need to use a wafer head (flat) screw on the bottom to keep the port clear for the USB cable.  You can optionally use the same M3x6mm wafer head screws for the entire bottom of the case instad of the chicago bolt ones, which is what I did for my build.

The M2 hardware is to fasten the PCB to the case.  The M2x3mm screws go on the bottom, and the M2x4mm screws go on the top (PCB side), with the M2x4mm standoff extending through the bottom of the case.  The PCB is essentially floating vertically, but is held up by the 1mm case foam.  Below is simple diagram of how everything fits together.

<img src="https://i.imgur.com/EWZpSj6.png" width="350">

### Firmware

QMK/VIA source:
https://github.com/qmk/qmk_firmware/tree/master/keyboards/dcpedit/masonry
