---
title: "BlenderDMX Addon 2.1.4 Released"
date: 2026-01-17T13:53:42+0100
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v2.1.4
---
## Fixture Names and Major MVR Import/Export Improvements

Previously, fixture names relied on Blender’s structural Name property, which requires all names to be unique. While this is useful in other contexts, it is not suitable for device naming. This has now been resolved by introducing a dedicated fixture-name property within BlenderDMX.

Additionally, fixture labels in the 3D Viewport can now be defined using Blender’s Text property, allowing full customization. Unlike object names, Text values are not required to be unique, making this a more flexible option for labeling.

MVR import has been significantly improved, resulting in correct handling of sub-referenced symbols, along with fixes to symbol scaling, positioning, and duplicated UUIDs. During MVR import, several fixture properties—such as Protocols, Networks, and Connections—are now stored directly in the .blend file and are preserved during MVR export.

As 3D objects are exported as modern GLB files, the MVR GLB export process has also been improved to prevent compatibility issues.

* Add option for device label as 3D Text
* Add Name + Fixture ID to 2D Label to allow proper device labels
* Rework Fixture Name to be not dependent on Blender's requirements for unique
  name
* Fix broken fixture edit - add missing import
* Handle issues with SVG loading
* More strings translated to Chinese (Simplified Han script) by 大学没毕业
* MVR Import:
    * Handle MVR files with duplicated UUIDs
    * Handle non-invertible parent matrices
    * Traverse down nested symbols
    * Ensure correct object symbol scaling
* MVR Import/Export:
    * Store protocols for round-tripping
    * Store networks for round-tripping
    * Store connections for round-tripping
    * Improve GLB export
    * Ensure layers with same name are exported only once

**Full Changelog**: https://github.com/open-stage/blender-dmx/compare/v2.1.3...v2.1.4
