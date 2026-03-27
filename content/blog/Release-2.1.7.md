---
title: "BlenderDMX Addon 2.1.7 Released"
date: 2026-03-27T19:55:13+0100
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v2.1.7
---
## Improve Color Handling

The original simple color addition has been updated to mixing in linear RGB for additive colors and to multiplicative transmission in linear RGB for subtractive colors. Color Wheels are now mixed together, controlling RGBA, RGBL fixtures from within Blender has been improved, and when there no gobo and no iris, the beam is now clean. See full changelog below.

* Ensure undistored beam output when no iris and no gobo are used
* Improve colormixing:
    * Emitter mixing: additive-style mixing in linear RGB, bounded with screen blending. This is now used for RGB/RGBW/RGBA/RGBAL/...
    * Filter mixing: multiplicative transmission in linear RGB. This is now used for color wheel, CMY result, CTC/CTO/CTB, and gel.
    * Make color wheels work when RGB is at 0
    * Set non RGB to default to 0 - makes RGBA, RGBL fixtures color mixing to work when controlling only from Blender's color picker
    * Multiple colorwheels are now mixed together
    * Improve color wheel slot handling
    * Use color data from filter if linked to a wheel slot
* Fix some not working virtual channels
* Adjust GDTF Share data receiving to keep fixtures list intact if server returns empty list
* Add info to startup about pygdtf and pymvr versions
* Update translations
    * Swedish - Daniel Nylander
    * Chinese (Simplified Han script) - 大学没毕业
    * Spanish - Francisco Serrador

**Full Changelog**: https://github.com/open-stage/blender-dmx/compare/v2.1.6...v2.1.7
