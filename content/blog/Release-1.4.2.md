---
title: "BlenderDMX Addon 1.4.2 Released"
date: 2024-04-21T22:27:10+0200
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.4.2
---
# Workflow improvements based on feedback of dryHeat from Discord

Many small and big workflow improvements have been implemented, from improved keyframe storing (indicate fixtures with modified state, save only fixtures with changed data, allow saving only selected fixtured), through indication of DMX patching collision, manual pushing of Programing Panel when render is paused for improved speed, new tool to reset Targets to different axis, deselection by choosing a group... possibility to export/import custom data, to prevent data loss during addon updates, and lots more, see changelog below for full details.

* Provide a way to export and import custom data from/to the Addon
* Remove Blender files of old models from the Addon
* Improve keyframing:
    * only keyframe fixtures with changed data
    * allow keyframing only selected fixtures
    * indicate unsaved state in fixtures list
* Show DMX Footprint and indicate if address is colliding in Fixtures list
* Allow fixtures deselection by groups
* Allow the Programmer data to be Applied manually when render is paused
  for speedup of response on large setups
* Add icon to re-set Targets, with a selection of axis
* Italian version is now fully translated
* Ensure programmer is populated with fixture's data also when selected by
  shortcuts
* Ensure that color is applied to fixtures with color wheel but without
  other color mixing
* List GDTF files without at signs @ in filename
* Handle gobo (not)loading for GDTFs without images
* Fix dimmer jumping over time
* Add support for ColorAdd_C,M,Y
* Add support for Gobo(n)PosRotate

