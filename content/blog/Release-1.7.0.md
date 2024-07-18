---
title: "BlenderDMX 1.7.0 Released"
date: 2024-07-18T00:26:59+0200
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.7.0
---

#### 1.7.0

# Add Initial MVR Export

New MVR Export allows export of fixtures (only fixtures, no other 3D objects
yet) with their patching info, color and focus points, into a single layer,
which is sufficient to move the patch from BlenderDMX to consoles like
[BlinderKitten](https://blinderkitten.lighting/).

* Initial MVR export - fixtures and focus points on one layer
* Ensure fixture name is unique when importing from MVR
* Fix dimmer if only one beam geometry exists
