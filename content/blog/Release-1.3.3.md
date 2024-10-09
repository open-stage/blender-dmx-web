---
title: "BlenderDMX Addon 1.3.3 Released"
date: 2024-03-12T23:18:22+0100
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.3.3
---

# Fix render when pan/tilt was locked to target

When pan/tilt were locked to Target, other attributes like zoom or color were
not visualized correctly, this is now fixed. Add support for indirect color
mixing attributes - ColorRGB_Red/Green/Blue.

* Add support for ColorRGB_Red/Green/Blue color attributes
* Bug fix pan/tilt lock
