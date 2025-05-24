---
title: "BlenderDMX Addon 2.0.1 Released"
date: 2025-05-24T08:07:40+0200
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v2.0.1
---
## Small re-adjustments after the big 2.0 release

Fixture channel-functions and channel-set processing now has an initial caching system to eliminate some of the the small penalty added by using the real-world physical properties for the fixture. Both the color picker and the pan/tilt fader handling has been improved to eliminate spontaneous value drifting on selecting/unselecting fixtures. BlenderDMX Addon provided GDTF profiles have been revised - several were updated and improved, some were removed (they remain in the GDTF Share should they be needed, along with many much better ones).

* Improve migration from older blend files
* Unify programmer defaults
* Fix gobo indexing angle calculation
* Update packaged fixture profiles:
    - keep only BlenderDMX created profiles
    - improve the default profiles with more data
    - provide RGBW/RGBA versions
    - REMOVED some files like rotating beam or source4, they exist in the GDTF
      Share
* Add per-channel caching to render()
* Save and apply XML provided offset to pan/tilt geometrie
* Map pan, tilt, color picker to DMX RGB/CMY correctly and without drifting

**Full Changelog**: https://github.com/open-stage/blender-dmx/compare/v2.0.0...v2.0.1
