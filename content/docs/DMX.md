---
title: "DMX512"
date: 2024-04-07T10:57:52+0200
category: "Help"
---

DMX 512 is a method to control entertainment devices. It works by sending 512
values (these values are called channels, each value (each channel) is a digit
between 0 and 255). These channels are sent either over RS485 or over Ethernet
network via protocols like [sACN](../sacn) or [ArtNet](../artnet). When DMX is
sent over Ethernet, each group of 512 channels is called a Universe.

Each controlled device requires certain number of DMX channels, each channel
then typically controls one feature of the device, for example dimmer,
horizontal panoramic movement (pan) or vertical tilting movement (tilt) and so
on. The layout of which channel controls which feature are decided and given by
the manufacturer of the device.

Each channel can carry 8bits of information, that is a value between 0-255.
Sometimes, more precise control is needed, in that case multiple (typically
two) channels are used to form 16bits - being able to carry value between
0-65535.

In order to control or visualize devices, a description of what device features
are and how they are mapped to DMX channels is needed, this is where [GDTF
comes in](../gdtffixture).

## DMX Addressing

Each fixture needs to have a DMX address. This address is a starting value from
which the fixture will be receiving data from the DMX stream and the amount of
received data depends on the amount and type of controllable parameters of the
fixture. Different types of fixtures typically have different amount of
controllable parameters, thus different amount of required DMX channels (often
called "DMX footprint"). The addresses thus need to be spaced in such a way
that the fixtures and their DMX footprints do not overlap.

As the DMX512 contains 512 channels, it can for example control up to 512
single channel based devices. A Dimmer is a good example of a device which
needs just a single channel to be controlled. Each Dimmer will have it's own
address (1-512). If the device is for example LED fixture with RGB colors, each
color will be one channel, then this fixture will need 3 channels and one can
control up to 170 RGB fixtures on one DMX line (512 total possible channels / 3
channels required by the fixture = 170 fixtures possible to control
individually over one DMX line). Each fixture will be addressed in such a way
that it's channels are not overlapping with other fixtures, so for example: 1,
4, 7, 10, 13...  More complex devices require more channels, thus more
spaced-out addressing.

This was a very quick introduction. You can read more about [DMX512 on the
web](https://duckduckgo.com/?q=DMX512). 

## DMX Universes and DMX Protocols in BlenderDMX Addon

A Universe is a group of 512 DMX channels. BlenderDMX Addon supports the following
protocols to control the devices:

- BlenderDMX Addon contains a built-in [Programmer](../programmer) for Dimmer, Pan,
  Tilt and [more](../programmer#attributes), universe counting starts from 0.
- [sACN](../sacn) protocol counts universes from 1, thus the first universe is
  1, second 2...
- [Art-Net](../artnet) protocol counts universes from 0, thus the first
  universe is 0, second 1...

## BlenderDMX Addon DMX driver for Blender

ℹ️  *There is no need to set this driver up to control patched lighting 
fixtures as patched fixtures receive DMX automatically.*

The BlenderDMX Addon provides a custom DMX driver `#bdmx` for Blender,
allowing to use received DMX values and use them as input for any Blender
property. To utilize this feature, `#bdmx(universe,channels(s))` keyword can be
used, `universe` is desired universe, `channel` is an address and it can either
be a single one for 8 bit value or multiple, for 16, 24, 32... bit values.

So to receive 8bit value from universe 1, address 20, this is the syntax:
`#bdmx(1, 20)`:

![image](../media/driver_8.png)


To receive a 16bit value from universe 2, address 30 and 31, this is the
syntax: `#bdmx(2, 30, 31)`. 

![image](../media/driver_16.png)

The channels can be in any order, depending on how the console is sending it,
for example `#bdmx(1, 21, 20)`:

In order to see 3D objects being animated through this driver, the animation
player must be in the "Play animation" state:

![image](../media/player_play.png)

See [Recording #bdmx
driver](../keyframe-animations-recording/#recording-bdmx-driver) for
information on how the driver data can be recorded to keyframes and then played
back.


