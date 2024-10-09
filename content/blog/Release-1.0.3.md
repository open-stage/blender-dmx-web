---
title: "BlenderDMX Addon 1.0.3 Released"
date: 2023-11-25
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.0.3
---

# Faster MVR imports, 2D planning view, improved 3D models loading

This version comes with added Blender 4.x compatibility, although Blender 3.6 is still much faster and thus recommended to be used. Speaking of speed...MVR import has been much sped up, there is a new 2D view which is using SVG from GDTF (if provided and if not provided it adds a default symbol). Many improvements to MVR import, to 3D models import and also to the overall app. Added support for XYZ fixtures.


### 1.0.3

* MVR Improvements:
  * Add FixtureID, CustomId... from MVR to Fixture
  * Create groups from MVR, migrate groups from str([]) to json
  * Clean up unused MVR collections after MVR import
  * Add UUID to fixtures and groups

* GDTF Improvements:
  * Handle models composed of multiple parts

* App improvements:
  * Add initial support for 2D symbols and 2D TOP planning view
  * Speed up MVR import - fix GDTF collection caching, cache also MVR imported objects
  * Converted Primitives to glb to ensure compatibility with Blender 4.x
  * Increment data version and provide migration
  * Remove fixture from groups when deleting fixture
  * Display revision in fixture listing
  * Create new World in case it is missing
  * Allow centering selected fixture's Targets
  * Handle time during fixture edit processing (prevent errors)
  * Check for existence of Dimmer for fixtures without dimmer (prevent errors)
  * Add possibility to make fixture geometries selectable
  * Display Volume cone on all lights when enabled
  * Add generix XYZ fixture to BlenderDMX Addon
  * Add support for XYZ Z,Y,Z and Rot X,Y,Z attributes and for devices without target
