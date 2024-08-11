---
title: "BlenderDMX 1.7.5 Released"
date: 2024-08-11T09:37:12+0200
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.7.5
---

* Allow using user writable directory associated with an extension (extension only)
* Show fixture name in Align panel if it is a selected active object
* Fix count of selected fixtures in Programmer, Align, and other panels
* Ensure that the beam has full diameter at the lense in Cycles for Blender 4.1 and up
* MVR import:
    * Deselect all objects before import to prevent issues
    * Add support for MVR classing to show/hide MVR classes
* GDTF import:
    * Add constraints for multiple heads and yokes
    * Apply transformation after joining the objects
    * Check dimensions with safer method
    * Allow import of existing files
    * Use DMX break overwrite only for Geometry References
    * Transfer root geometry attribute to children for complex fixtures
    * Improved creating constraints and removed pixel factor
* Import_3ds: Fix texture color
* Increase time for collection auto-creation in import/export dialogs
* Update translatable language strings
* Add testing files download and basic testing scripts
