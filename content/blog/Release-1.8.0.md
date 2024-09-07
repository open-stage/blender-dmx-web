---
title: "BlenderDMX 1.8.0 Released"
date: 2024-09-07T23:45:39+0200
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.8.0
---
# Support for second gobo wheel, iris, continuous pan/tilt, CTC and more

This release contains support for new attributes (Gobo2, Iris, CTC, CTO, CTB, PanRotate, TiltRotate) and more. The Shader three had to be completely re-organized and gobo loading needed to be refactored. There is a migration procedure in place, but very likely, older .blender files will not project gobos correctly. **Re-editing GDTF fixtures might be needed.** It is also possible that previously recorded keyframe animations will not work right away and will need re-adjustments. Sorry for the inconvenience.

Complex fixtures can now be controlled via the new Subfixtures menu, allowing precise selection of fixtures' geometries and controlling of only attributes attached to these geometries.

**Do note, that the second gobo and iris only work in Blender 4.2 and up.**

Changelog:

* Updated translations
* Add support for pan/tilt rotation, add GDTF fixture with continuous rotation
* Add support for Iris
* Add support for Gobo 2 and for Gobo1/Gobo2 combined gobo projection
* Add support for static gobos (Gobo(n) without Gobo(n)Pos or Rot)
* Add support for CTC
* Add display device label also in 3D
* Add subfixture based controlling
* Programmer: show fixture type name if multiple selection is one gdtf type
* Fix: Ensure working Pan/tilt control for fixtures without target
* Fix: Fix keyframe cleaning after addition of PSN
* Fix: Adjust share profile path after changes for custom user data path
* Fix: Ensure that World - Scene - Background exists
