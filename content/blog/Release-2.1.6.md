---
title: "BlenderDMX Addon 2.1.6 Released"
date: 2026-02-03T21:52:48+0100
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v2.1.6
---
## Extend channels resolution parsing

As some fixtures in the GDTF Share now come up with channels with resolution more then 16bit, ensure that these can be parsed without failing, while downscaling them to 16bit or 8bit, depending on usage. Make the internal Programmer to control Pan/Tilt as 16bit, for precise positioning inside Blender.

* Fix volumetric beam toggle
* Rename BlenderDMX fixture profiles to new set of names
* Use fixture name if fixture short name is not available
* Ensure correct MVR-xchange protocol data commands when requesting a commit
* Channels resolution:
    * Pan/Tilt control from local Programmer is now 16bit for precise positioning
    * Expand the dmx channel size to deal with 24/32bit channels, update pygdtf to 1.4.4
* Translated using Weblate (Chinese (Simplified Han script)) [大学没毕业]
* Translated using Weblate (Czech)

**Full Changelog**: https://github.com/open-stage/blender-dmx/compare/v2.1.5...v2.1.6
