---
title: "Art-Net"
date: 2024-04-07T10:57:58+0200
category: "Help"
---
> Art-Net universes are enumerated from 0, so first Art-Net universe is 0

You must have at least one Universe set to Art-Net, to be able to enable it.
When enabling Art-Net, ideally, do not change the IP address settings and leave
it at the default 0.0.0.0 .

### Enabling Art-Net

Create Universe, set it to Art-Net, enable Art-Net Input:

![image](../media/enable_artnet.png)

> Note: Art-Net Input can only be enabled if you have at least one Universe set to Art-Net

# Using a console on the same computer

When using an Art-Net source on the same computer, you have to make sure to
start and enable Art-Net **first** in the BlenderDMX Addon.

If running two pieces of Art-Net based software on one computer is not working
for you, then save yourself the trouble and the best is to use another computer
for the sending.

# Checking who/what is using the Art-Net port

On Linux (and perhaps also on macOS) one can check what program (PID/name) is
currently holding the port 6454 open, blocking it. This can be checked by
running the following command in the terminal:

```bash
netstat -aop | grep 6454
```
## Examples

### BlinderKitten

Art-Net related settings in BlenderDMX Addon and in [BlinderKitten](https://blinderkitten.lighting/) DMX console:

Universe settings in BlenderDMX Addon:

![image](../media/artnet_blinderkitten_01.png)

Universe settings in BlinderKitten:

![image](../media/artnet_blinderkitten_02.png)

Fixture patch settings in BlinderKitten:

![image](../media/artnet_blinderkitten_03.png)


### BlenderDMX Addon and QLCplus via Art-Net on the same computer

<video src="../media/artnet.webm" controls="controls" >

