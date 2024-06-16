---
title: "BlenderDMX 1.5.1 Released"
date: 2024-06-16T01:50:35+0200
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.5.1
---

![blenderdmx_gobo_logo](https://github.com/open-stage/blender-dmx/assets/3680926/1f4f2bcc-2006-4e6e-8478-bb19b8a7ac1d)

#### 1.5.1

- Fix python import on Win32 platform

#### 1.5.0

# Speed optimizations. Further improvements to GDTF models loading. New and improved default fixture files.

What started as a bunch of small improvements and fixes resulted in a huge code
re-organizing, together with speed optimizations and also with nice
enhancements to GDTF models loading. The Addon has been reworked into an
Extension for Blender 4.2 (in beta as of June 2024) and the new BlenderDMX
extension is now [available on the official online Extension
site](https://extensions.blender.org/add-ons/open-stage-blender-dmx/). The
bundled moving head GDTF now includes zoom and gobos, to make it easier to
start exploring BlenderDMX. New RGB glowing tube GDTF has been bundled in.

* Fix showing fixtures after disabling 2D layout view
* Adding RGB glowing tube BlenderDMX provided device
* Adding Zoom and Gobos to the BlenderDMX provided Beam GDTF file
* Add custom cutoff_distance to lights to make gobos work in Eevee Next
* Remove onDepsgraph - prevents crashes and improves performance
* Big changes in architecture of the python code (split dmx.py from \_\_init\_\_.py, rework import to be all relative, do not use import \*)
* Fix several user visible and invisible issues
* Translated using Weblate (Polish) [WaldiS], (Spanish) [Josman Goncalves Bravo], (German) [Ettore Atalan]
* Loading 3DS with apply transforms enabled for better results
* Apply position of referring geometry to geometry reference
* Create gobo plane only for fixtures with gobo for better performance
* Open shutter at 0 also at 255
* Limit number of colors/gobos to 255

