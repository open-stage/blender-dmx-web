---
title: "BlenderDMX Addon 2.0.2 Released"
date: 2025-05-30T17:50:20+0200
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v2.0.2
---
### Allow fixture edits while preserving addressing

This release adds the ability of device editing while preserving DMX address,
universe and/or the Fixture ID. Strobing is now really flashing and not
blinking as before. When Cleaning project data, old BlenderDMX profiles are now
being removed. MVR export/import has been improved.

#### Changelog

* Update pygdtf to 1.2.4
* Sync Shutter1Strobe to the programmer
* Make Shutter1Strobe flashing, not pulsing
* Ensure that DMX breaks's address/universe are overflowing 512
* Export MVR with breaks from 0, set universe 0 as 1
* Fix programmer values after clear
* Clear any selection prior to fixture edit/mvr import
* Add option to not modify Fixture_ID and Address during Edit
* Ensure that color defined close to GDTF default white is interpreted as full white
* Remove and re-copy BlenderDMX provided files when Cleaning project data

**Full Changelog**: https://github.com/open-stage/blender-dmx/compare/v2.0.1...v2.0.2
