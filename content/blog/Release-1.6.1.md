---
title: "BlenderDMX Addon 1.6.1 Released"
date: 2024-07-06T10:52:28+0200
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.6.1
---

#### 1.6.1

# Support additional additive colors: Amber, Lime, UV, White, WW, CW

NRGSille has helped to include updated version of the 3DS file importer. This, together with import parameters adjustment, results in better import of GDTF and MVR files with 3DS models. New additive colors like White, Amber or Lime are now supported.

* Add icon 'Center to selected' to Programmer
* Add icon 'Clear mixing colors' to Programmer
* Add support for additive mixing: Amber, Lime, UV, White, WW, CW
* Update io_scene_3ds to LTS version and adjust GDTF and MVR to this LTS version
* Show error and a traceback on load3DS error
* Ensure that fixtures can be removed even if their data is broken
* Add RGB versions of the provided source4 fixtures
