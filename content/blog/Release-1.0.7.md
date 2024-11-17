---
title: "BlenderDMX Addon 1.0.7 Released"
date: 2023-12-28
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.0.7
---

# New Fixture list and editing, Improved Universe and Network Protocols settings

Setting up Network protocols like Art-Net could sometimes be challenging, this release is improving the setting process by providing more helpful messages, better error and timeout handling. The Fixture list has been re-done by using Blender's scrolling list which offers better user experience, in-place editing, filtering and so on.

### 1.0.7

* New Fixture UI List:
    * Better scrolling and filtering
    * In-place editing of some attributes
    * New editing of XYZ position transforms
* Indicate that Blender 3.4 and higher is required
* Improvements to MVR-xchange:
    * Support for MVR_COMMIT message
    * Rewrite of the protocol code
* Add custom namespace driver for Blender, to use DMX for general animations of
  any 3D objects in Blender, see [wiki](/docs/dmx/#blenderdmx-addon-dmx-driver-for-blender) for details
* Improved Network DMX protocols:
    * Separate sACN from Art-Net
    * Improve Art-Net handling (ArtPoll, error messages, timeout)
    * Universe setting made clearer
