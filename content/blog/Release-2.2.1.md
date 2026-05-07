---
title: "BlenderDMX Addon 2.2.1 Released"
date: 2026-05-07T21:13:56+0200
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v2.2.1
---
## Progressive MVR Import

Importing MVR files - especially large ones - can take some time. This update adds real-time progress feedback and allows the import to be cancelled at any moment by pressing Escape. Because the import process runs in multiple stages, cancelling early may leave some objects unfinished or not yet in their final positions.

* Rework MVR import to progressive, allowing canceling during import
* Translated using Weblate:
    * Indonesian, Arif Budiman
    * Chinese, Simplified Han script, 大学没毕业
    * Swedish, bittin1ddc447d824349b2

**Full Changelog**: https://github.com/open-stage/blender-dmx/compare/v2.2.0...v2.2.1
