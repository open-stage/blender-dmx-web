---
title: "BlenderDMX Addon 2.0.0 Released"
date: 2025-05-18T11:45:46+0200
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v2.0.0
---
## Support for GDTF real-world physical properties

The data provided in the [GDTF](https://gdtf-share.com/) files includes not
only 3D models, gobo images... or the necessary DMX control descriptions, but
it additionally contains measurements of movement ranges, beam angles, rotation
speeds, and other physical parameters. This release of [BlenderDMX
Addon](https://blenderdmx.eu/) adds initial support for utilizing these
measurements on supported visualized device properties, transforming it from a
"nice effects generator" into a lighting visualizer representing real lighting
fixtures behavior.

### The following currently supported GDTF Attributes now utilize physical measurements from both Channel Functions and Channel Sets:

* Pan, Tilt, PanRotate, TiltRotate
* Zoom, Iris
* CTC, CTB, CTO
* Shutter1, Dimmer, ShutterStrobe
* Color1, Color2, Color3, ColorMacro1
* Gobo1, Gobo1Pos, Gobo1PosRotate
* Gobo2, Gobo2Pos, Gobo2PosRotate

### Current limitations:

* Acceleration and time for the movement is not utilized yet (so for example
  Pan or Tilt can move unrealistically fast).
* Strobing should be improved for short "flashes", rather then "blinks".
* Combining multiple colors on a single device needs to be improved (for
  example using RGB and CTO at the same time).

### Enhancements thanks to using physical properties:

Using the physical properties brings also further enhancement in visualization,
for example when selecting colors on ColorWheels or gobos on GoboWheels now
uses correct Wheel Slots. Strobing has been reworked to use Blender' "driver"
feature, using the "frame" of the animation playback with correct strobing
speed.  Some behavior of the device can be conditionally affected by a value of
multiple channels (for example Gobo Indexing and Gobo Rotation, Pan and
PanRotation or Zoom ranges) and this is supported by utilizing the Mode
dependency (Mode Masters) feature of GDTF.

Being able to represent lighting devices more correctly should enhance the
usefulness of BlenderDMX Addon for the generation of high-quality renders,
particularly with the Blender Cycles renderer and we hope that future
developments in Blender's [Eevee
Next](https://code.blender.org/2024/07/eevee-next-generation-in-blender-4-2-lts/)
will improve the real-time visualization of many volumetric beams.

Speed up improvements should also be done in the Addon, as this  initial
support for utilization of the physical parameters in BlenderDMX Addon does
introduce some rendering speed penalty, so future improvements and data caching
will be useful.

## Other improvements:

* Programming movement via Pan/Tilt/PanRotate/TiltRotate sometimes collides
  with the "follow Target" feature. New option to ignore the Target on selected
  fixtures allows to have more control during programming.
* When zooming in to smaller diameter, the intensity is now being increased,
  further mimicking real world behavior. 

## Updating:

After updating BlenderDMX and opening .blend files created in older versions,
GDTF fixtures need to be re-edited in the Advanced mode: select fixture, go to
Fixtures → Edit → Advanced edit, make sure a correct GDTF profile is selected,
click OK.

## For more details, see the changelog for this 2.0.0 release:

* Add support for ChannelFunctions and ChannelSets with their Physical From,
  Physical To and WheelSlotIndex:
    * Add this support to following GDTF Attributes:
        * Pan, Tilt, PanRotate, TiltRotate, Zoom
        * CTC, CTB, CTO, Iris
        * Shutter1, Dimmer, ShutterStrobe
        * Color1, Color2, Color3, ColorMacro1
        * Gobo1, Gobo1Pos, Gobo1PosRotate
        * Gobo2, Gobo2Pos, Gobo2PosRotate
    * Add support for Mode Masters
    * Add optional BlenderDMX defined default Physical From/To values
* Reworked Shutter/Dimmer - removed complex code
* Added compensation of intensity when zooming
* Adjusted and separated color related code
* Add support for PanMode, TiltMode, and PanTiltMode GDTF Attributes
* Add support for emitter models with multiple materials
* Add option to ignore Target during programming
* Fix DMX breaks during MVR import
* Fix color import during MVR import
* Re-add address/universe option when editing multiple fixtures
* Fix GDFT processing
   * Mark empty manufacturer
   * Handle some importing errors
* Fix DMX Breaks processing on fixtures

## What's Changed via PRs

* Initial support for ChannelFunctions and Physical From-To by @vanous in https://github.com/open-stage/blender-dmx/pull/262
* Shutter/dimmer as keyframable physical values. Zoom intensity compensation. by @vanous in https://github.com/open-stage/blender-dmx/pull/263
* Gobo physical values by @vanous in https://github.com/open-stage/blender-dmx/pull/264
* Add support for channel sets by @vanous in https://github.com/open-stage/blender-dmx/pull/265
* Release v2.0.0 by @vanous in https://github.com/open-stage/blender-dmx/pull/266

**Full Changelog**: https://github.com/open-stage/blender-dmx/compare/v1.9.6...v2.0.0
