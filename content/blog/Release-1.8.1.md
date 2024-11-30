---
title: "BlenderDMX Addon 1.8.1 Released"
date: 2024-11-30T14:20:10+0100
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.8.1
---
# Blender 4.3 now supported, Updated pygdtf/pymvr, Drivers keyframe recording

## Translations

Numerous translations have been added. Many thanks to all contributors.

## MVR and GDTF Imports

The pygdtf and pymvr libraries have received several improvements. These,
together with some other changes in BlenderDMX Addon, should further improve
GDTF and MVR imports.

MVR Import can now be adjusted to utilize (or not) Focus Points as device Targets.

## Blender 4.3 support

SVG imports and some other documented and undocumented changes to the Blender
API had to be handled to support the 4.3 release of Blender.

## Key-frame recording and playback of \#bdmx drivers

There are new options to allow recording of \#bdmx drivers. In order to re-play
them, the drivers need to be disabled, which is not easily supported in Blender
but a workaround has been found and implemented.

## Remove BlenderDMX Addon from a .blend file

A new option in Setup - Extras: "Remove DMX from blend file" tries to clean up
BlenderDMX Addon device specific data from a .blend file.

## Other changes

* Ensure that gobos and iris work without zoom (again)
* Add keymap preference screen


## Changelog

See the changelong for more information, or developers can look at [git
log](https://github.com/open-stage/blender-dmx/commits/main/) for full details.

* Translated using Weblate (Tamil, Literary Chinese, Chinese Chinese (Simplified Han script), Polish, Spanish, Turkish)
* Handle some essential MVR import errors
* Add MVR Target import option
* Update pygdtf and pymvr - improve imports of GDTF and MVR files
* Add support for Blender 4.3
* Add possibility to record objects with #bdmx drivers and disable/enable them to allow playback/rendering
* Add 'Remove DMX from blend file' option
* Ensure that gobos and iris work without zoom (again)
* Add keymap preference screen
