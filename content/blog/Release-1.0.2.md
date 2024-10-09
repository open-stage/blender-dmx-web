---
title: "BlenderDMX Addon 1.0.2 Released"
date: 2023-11-14
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.0.2
---

## Release Info

### Version v1.0.2

Problem with localized Blender when applying material to the volumetric beams should be solved. MVR import has been much improved - previously missing objects are now being imported, textures for 3D objects are now extracted from the MVR and are used with the 3D files. GDTF import has been made more resilient. Fixture profiles management has been improved together with added support for importing GDTF files from GDTF Share ( https://gdtf-share.com ). To use this feature, register an account on the GDTF Share site and set these credentials in Blender-DMX addon preferences, see small manual [here](/docs/gdtffixture/#gdtf-share-integration-in-blender).


# Changelog:

* MVR improvements:
  * Add collections for GroupObjects and Layers
  * Support group object list
  * Process child lists of MVR objects
  * Apply scaling of 3D objects in correct order
  * Load textures for 3D models
* Fixture profiles management:
  * Backport local and GDTF Share file management and import from development branch
  * Add GDTF Share integration (can be used with username/password from gdtf-share.com)
  * Improve local profiles handling
  * Do not require Blender restart after GDTF profiles import
* Improve GDTF parsing
* Fix issue with localize structures by requesting localized versions of strings
