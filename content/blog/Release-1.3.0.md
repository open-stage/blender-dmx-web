---
title: "BlenderDMX Addon 1.3.0 Released"
date: 2024-02-23T23:43:42+0100
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.3.0
---

# Gobo support in Cycles, Noise Scatter in Volume box, UI translation


For quality rendering, we needed to ensure that gobos can be rendered in Cycles, this is now done. As beam visibility requires fog/haze and the smooth haze is very boring, Volume now has another setting of Noise Scatter, creating some cloudiness. The UI can now be fully translated. Various small improvements have been done.

### 1.3.0

* Add support for gobos in Cycles
* Add translation of UI
* Add Noise Scatter to Volume box
* Enable programmer only if any fixture is selected
* Small improvements:
    * GDTF download: Better sanitizing of GDTF download file name
    * Handle ArtNet status setting error
    * MVR import: check if file exists before loading it
    * Handle fixtures without dimmer
    * Handle fixtures with gobo but without zoom
