---
title: "BlenderDMX Addon 2.0.17 Released"
date: 2025-11-23T10:00:30+0100
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v2.0.17
---
## Add support for Blender 5

Only a few small missed touch ups were required for Blender 5 compatibility.
Btw, Blender's new Color Temperature for light objects is not utilized in
BlenderDMX, we rather use our own Color Temperature calculation which is
working for both Eevee and Cycles.

* Avoid using IDProperties for Preferences, this is required in Blender 5
* Remove optimisation for color updates to fix mixing for fixtures with only
  color wheel and without CMY/RGB/CTO

**Full Changelog**: https://github.com/open-stage/blender-dmx/compare/v2.0.16...v2.0.17
