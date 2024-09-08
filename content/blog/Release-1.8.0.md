---
title: "BlenderDMX 1.8.0 Released"
date: 2024-09-07T23:45:39+0200
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.8.0
---
# Support for second gobo wheel, iris, continuous pan/tilt, CTC and more

## Second gobo, iris, continuous movement

This release contains support for new attributes (Gobo2, Iris, CTC, CTO, CTB,
PanRotate, TiltRotate) and more. Gobo 1, Gobo 2 and Iris can all be used
together, for combined projection like in the real world. The color system
(mixing, color wheel and color temperature control) mixes all parts together in
an additive fashion.

## Compatibility with .blender files created in older versions of BlenderDMX


Upon opening a .blender file created in older BlenderDMX, there is a warning
popup and a message in the Setup panel. This is because the Shader three had to
be completely re-organized and gobo loading needed to be refactored. There is a
migration procedure in place, but very likely, older .blender files will not
project gobos correctly. **Re-editing fixtures in the Fixtures list might be
needed.** See [section below](#re-building-fixtures-from-gdtf-files) for the
simple to perform procedure.

It is also possible that previously recorded keyframe animations will not work
right away and will need re-adjustments. Sorry for the inconvenience.

## Subfixtures

Complex fixtures can now be controlled via the new Subfixtures menu, allowing
precise selection of fixtures' geometries and controlling of only attributes
attached to these geometries.

## Re-building fixtures from GDTF files

To re-build fixtures from their GDTF files, you can do the following:

- go to *Fixtures list*, select a fixture (or more)
- in the *Fixtures menu*, select *Edit*
- In the Edit screen, check *Advanced edit*
- Press OK. Depending on the size of your file and the amount of fixtures, this
  can take a few minutes.

This will work as long as you still have the original GDTF files located in the
BlenderDMX addon. If you get an error, best is to close the .blender file
without saving, re-open it, first import the required GDTF files (Setup -
Import - Import GDTF Profile) and then re-edit the fixtures. In the Advanced
Edit screen, you can also select the GDTF Profile and DMX Mode, to update the
fixture to a new or different GDTF.

## Blender 4.1 and older

Supporting older Blender is becoming harder and harder:

- The second gobo and iris only work in Blender 4.2 and up, thanks to the new
  Eevee renderer. This means that even with a lot of work on backwards
  compatibility, some features are not available in the older Blender anymore.
- The structure of the legacy addon (used in Blender 4.1 and older) is very
  different then the Extensions used in Blender 4.2 and up, which means
  individual development for addon and for the extension (as if dual
  development for Eevee and Cycles wasn't already hard enough).
- Looking at the downloads count, it is very obvious that most people
  have moved onto Blender 4.2.

This all means that future development of BlenderDMX will most likely focus
mostly on Extension for Blender 4.2 and up.

## Changelog

See the changelong for more information, or developers can look at [git
log](https://github.com/open-stage/blender-dmx/commits/main/) for full details.

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
