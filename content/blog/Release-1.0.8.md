---
title: "BlenderDMX Addon 1.0.8 Released"
date: 2024-01-06
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.0.8
---

# Gobo support :tada: 

After much of trials and research, initial gobo support has been added. For rotation, the Blender Animation player must be in the Play state. Gobos from GDTF are utilized, these can be indexed and continuously rotated. **Makers**: you can now be creative and add for example iris support. 

Breaking change: The BlenderDMX Addon driver for blender has been renamed to `#bdmx`. This is to make the (still very young) [driver simpler](/docs/dmx/#blenderdmx-addon-dmx-driver-for-blender).



## 1.0.8

* Initial GOBO from GDTF support with indexing and rotation
* Updating bdmx driver syntax to #bdmx
* Programmer improvements (name/count of selection, fixture specific control)
* Add on-line version check into Extras
* If no fixture is selected, select first/last on Ctrl-Right/Left
* MVR-xchange improvements and custom icons
* Hide/show positions in Fixtures edit list

