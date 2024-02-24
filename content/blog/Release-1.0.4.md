---
title: "BlenderDMX 1.0.4 Released"
date: 2023-12-03
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.0.4
---

# Pixel color control bug fix plus a bunch of other features

Originally a bug fix for pixel devices color control, this release brings other improvements like support for devices without tilt, 16bit channels or additional Color picker in the Programmer. But a whole lot of work on other features went into this release, see the change log for more details.

### 1.0.4
* Fixing a color control bug with pixel devices like Spiider
* Fix tilt movement when fixture is on the floor
* More attributes are now applied (only) for correct geometries (RGB, XYZ
  position and rotation, dimmer)
* Extending Volume preview settings to now have the possibility to see the fake
  beam cone for None, Selected fixtures or All fixtures
* Adding RGB based color picker to the existing color picker in Programmer
* Support for movement control of fixtures with pan only (without tilt)
* Initial support for 16bit channels for smoother behavior: pan, tilt, dimmer
* Group selection can now be additive (as before) or exclusive (only selected
  group)
* Allow freezing of pan/tilt movement to current position (for example after
  Target adjustment). Indicated by LOCK icon in Fixture list
* GDTF Share password in Preferences now masked with \*\*\*\*\*
* Fixture ID in Fixture list is now displayed only if not empty
