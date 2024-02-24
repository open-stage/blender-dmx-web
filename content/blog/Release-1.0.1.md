---
title: "BlenderDMX 1.0.1 Released"
date: 2023-09-17
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.0.1
---

## Release Info

### Version: v1.0.1

The main feature of this release is much improved MVR Import which now supports loading of complete scene, including Focus Points, Colors, Trusses and other scene objects. Fixes include handling volume box (loading and material), sACN receiving, Live DMX display and more.


## Changelog:

* Improved MVR import:
  * Import Focus Points and Fixture Color
  * Import Scene Objects
  * Import Trusses
  * Handle incomplete MVR files
* Fix issues due to empty material
* Enable camera selection
* Improve logging
* Fix Live DMX logic
* Ignore packets with dmxStartCode set
* Add support for migrations of older BlenderDMX file versions
* Process deeper GeometryReference trees
