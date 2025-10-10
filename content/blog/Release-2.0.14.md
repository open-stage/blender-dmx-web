---
title: "BlenderDMX Addon 2.0.14 Released"
date: 2025-10-10T19:54:44+0200
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v2.0.14
---
## Eliminate issue with misplaced beam geometries

We have hopefully fixed the cause for beam and other geometries to sometimes be
placed in wrong location due to the 3D cursor not being at origin. Scanner
(moving mirror) primitive type geometry has been added.

* Update 3DS wheel to 2.8.6
* Add Scanner 1.0 primitive type
* Reset 3D cursor position before GDTF and MVR imports

**Full Changelog**: https://github.com/open-stage/blender-dmx/compare/v2.0.13...v2.0.14
