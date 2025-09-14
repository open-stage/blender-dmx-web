---
title: "BlenderDMX Addon 2.0.12 Released"
date: 2025-09-14T21:22:55+0200
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v2.0.12
---
## Improved imports of MVR and 3DS

This release brings several under the hood improvements, together with updated
libraries for 3DS (io-scene-3ds) and MVR (pymvr) libraries, which in turn
ensure more correct imports and data processing.

* Skip migrations when creating a new scene for less verbose console output
* Added Vwx logo to MVR-xchange UI
* Updated pymvr library to 1.0.4
* Improved FocusPoint import from MVR:
    - import geometries attached to Focus Points
    - ensure correct position
    - add classing to be able to hide these geometries
* Ensure correct symbols processing and tagging, for future export
* Uploaded 3DS wheel version 2.8.0
* Updated BlenderDMX@LED_PAR_64 to fix strobing
* Russian translation update (Alex Nadzharov and Yurt Page)

**Full Changelog**: https://github.com/open-stage/blender-dmx/compare/v2.0.11...v2.0.12
