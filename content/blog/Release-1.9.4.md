---
title: "BlenderDMX Addon 1.9.4 Released"
date: 2025-03-06T22:45:08+0100
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.9.4
---

### Improve control of color mixing of child geometries

Fixtures with multiple levels of sub geometries where control attributes of
color mixing or dimmer are linked to a parent geometry can now be controlled
even if the parent geometry is several layers up the chain.

Auto white calculation is now applied to ColorAdd_W (white emitter), when
selecting colors from the color picker.

With all the above, we also have improved getting correct default values for
DMX channels (the pygdtf library still was using the GDTF 1.1 style of
defaults).

See the changelong for more information, or developers can look at [git
log](https://github.com/open-stage/blender-dmx/commits/main/) for full details.

Changelog:

* Improve getting default values for DMX channels
* Improve detection of parenting geometries for control of beams
