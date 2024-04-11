---
title: "sACN"
date: 2024-04-07T10:55:55+0200
category: "Help"
---

Unlike Art-Net, sACN does not require the DMX source and the DMX receivers (a
console and BlenderDMX) to be on the same IP range or anything. No dedicated
loopback interface, no complicated setup.

> sACN universes are enumerated from 1, so first sACN universe is 1

### Enabling sACN

Create Universe, set it to sACN, enable sACN Input:

![image](../media/enable_sacn.png)

> Note: sACN Input can only be enabled if you have at least one Universe set to sACN

### Patch the fixture to the same universe

![image](https://github.com/open-stage/blender-dmx/assets/3680926/17aaa53b-af50-4e71-86e4-bf8ad10cf82c)


### BlenderDMX with Chamsys via sACN on the same computer

<video src="https://github.com/open-stage/blender-dmx/assets/3680926/6bd6d33f-532a-424f-a537-093870913d14" controls="controls" >

