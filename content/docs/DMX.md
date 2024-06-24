---
title: "DMX512"
date: 2024-04-07T10:57:52+0200
category: "Help"
---

DMX 512 is a method to control entertainment devices. It works by sending 512
channels either over RS485 or over Ethernet network via protocols like
[ArtNet](../artnet) or [sACN](../sacn). When DMX is sent over Ethernet, each
group of 512 channels is called a Universe. You can read more about [DMX512 on
the web](https://duckduckgo.com/?q=DMX512). 

Each controlled device requires certain number of DMX channels - these numbers
are given by the manufacturer of the device, each channel then typically
controls one feature of the device, for example dimmer, horizontal panoramic
movement (pan) or vertical tilting movement (tilt) and so on. Each channel can
carry 8bits of information, that is a value between 0-255. Sometimes, more
precise control is needed, in that case multiple (typically two) channels are
used to form 16bits - being able to carry value between 0-65535.

In order to control or visualize devices a description of what device features
are mapped to what DMX channels is needed, this is where [GDTF comes
in](../gdtffixture).

## DMX Addressing

As the DMX512 contains 512 channels, it can for example control up to 512
Dimmers. Each Dimmer will have it's own address (1-511). If the device is for
example LED fixture with RGB channels (3 channels) one can control 512/3 = 170
RGB fixtures. Each fixture will be addressed in such a way that it's channels
are not overlapping with other fixtures, so for example: 1, 4, 7... More
complex devices require more channels. If the dimmer or RGB control requires
16bit channels, then 2 channels per each function (dimmer, red, green, blue)
are needed.

Each device needs a DMX address, this is the "starting" DMX channel of the DMX
signal. If more universes of DMX are used, a Universe number is also required.
If more devices are given the same DMX address, they will react together and
cannot be controlled separately. This is sometimes wanted in order to save DMX
addresses on the DMX console.

## DMX Universes and DMX Protocols in BlenderDMX

A Universe is a group of 512 DMX channels. BlenderDMX supports the following
protocols to control the devices:

- BlenderDMX contains a simple [Programmer](../programmer) for Dimmer, Pan, Tilt, Colors, Zoom and Strobe, universe counting starts from 0.
- [sACN](../sacn) protocol counts universes from 1, thus the first universe is 1, second 2...
- [Art-Net](../artnet) protocol counts universes from 0, thus the first universe is 0, second 1...

## BlenderDMX DMX driver for Blender

ℹ️  *when using the Programmer in BlenderDMX, there is no need to set this driver up to control BlenderDMX's lighting fixtures as patched fixtures receive DMX automatically.*

The BlenderDMX addon provides a custom DMX driver for Blender, allowing to use
received DMX values and use them as input for any Blender property. To utilize
this feature, `#bdmx(universe,channels(s))` keyword can be used, `universe` is
desired universe, `channel` is an address and it can either be a single one for
8 bit value or multiple, for 16, 24, 32... bit values.

So to receive 8bit value from universe 1, address 20, this is the syntax:
`#bdmx(1, 20)`:

![image](https://github.com/open-stage/blender-dmx/assets/3680926/15fccec8-58dd-4a9d-b3d4-e0744aed20db)


To receive a 16bit value from universe 2, address 30 and 31, this is the
syntax: `#bdmx(2, 30, 31)`. 

![image](https://github.com/open-stage/blender-dmx/assets/3680926/ec17099b-e8db-4c20-9019-d0d67eafab25)

The channels can be in any order, depending on how the console is sending it,
for example `#bdmx(1, 21, 20)`:

In order to see 3D objects being animated through this driver, the animation
player must be in the "Play animation" state:

![image](https://github.com/open-stage/blender-dmx/assets/3680926/c507c26d-cc63-4662-a45b-bc96ddf865bf)




