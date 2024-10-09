---
title: "BlenderDMX Addon 1.3.1 Released"
date: 2024-03-03T12:52:23+0100
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.3.1
---

# IES Photometrics support and Beam Lens rendering improvements in Cycles

IES Photometrics import and assignments to spot light allows for more photo-realistic volumetric beam rendering. With this, more detailed beam lens settings has been added to allow further [enhancing the rendering quality for beam rendering with gobo projection](https://blenderdmx.eu/docs/setup/#beam-lens-diameter-in-cycles).

* Add support to import IES photometrics and apply them to beams in Cycles
* Allow changing beam lens diameter for Cycles, based on global or per fixture settings
* Set hidden objects as hidden also for renderer
* Make more items translatable, disable automatic translation for Fixture controls
* Add version checks on start for Python, Blender, and for the BlenderDMX Addon
