---
title: "sACN"
date: 2024-04-07T10:55:55+0200
category: "Help"
---

Unlike Art-Net, sACN does not require the DMX source and the DMX receivers (a
console and BlenderDMX Addon) to be on the same IP range or anything. No dedicated
loopback interface, no complicated setup.

> sACN universes are enumerated from 1, so first sACN universe is 1

### Enabling sACN

Create Universe, set it to sACN, enable sACN Input:

![image](../media/enable_sacn.png)

> Note: sACN Input can only be enabled if you have at least one Universe set to sACN

### Patch the fixture to the same universe

![image](../media/edit_uni.png)


### BlenderDMX Addon with Chamsys via sACN on the same computer

<video src="../media/sacn.webm" controls="controls" >

