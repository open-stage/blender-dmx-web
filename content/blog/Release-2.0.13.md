---
title: "BlenderDMX Addon 2.0.13 Released"
date: 2025-09-21T22:07:41+0200
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v2.0.13
---
## Improved Programmer state storing

Previously, upon reopening a scene, the fixtures' programming was lost, unless
a keyframe was stored or DMX values were saved in an external DMX controller -
this update adds automatic remembering of the internal Programmer state to keep
the programing. Color Temperature channel has been added to the default
MovingBeam fixture.

* Add CTO to MovingBeam
* Store Programmer values (last DMX frame) to .blend file
* Ensure clean class unregistration

**Full Changelog**: https://github.com/open-stage/blender-dmx/compare/v2.0.12...v2.0.13
