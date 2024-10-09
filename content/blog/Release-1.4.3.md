---
title: "BlenderDMX Addon 1.4.3 Released"
date: 2024-05-04T08:22:38+0200
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.4.3
---
# Fix crash on Intel macOS, Add Device label to 2D view

Thanks to @Bartel-C8, we have now identified the source of crash on Intel macOS :tada:. Devices can now show Device name, or DMX address, or Fixture ID in the 2D layout view. Project data can now not only be exported/imported but also completely cleared out (erased). Several small but important things were fixed.

* Fix Intel Mac crashing on Create New Show - remove unnecessary setup class unregistration
* Display device label (name, id, or dmx) in 2D
* Rework 'Re-address only' to 'Advanced edit' for clarity
* Add Clear Project data button to clear the addon directory
* Add development related 'Reload BlenderDMX Addon' button to Extras
* Update translations
* Reload profiles after data clearing or loading
* Fix Volume box migration - prevent always deleting volume box on file load
* Fix gobo projection for fixtures without zoom
* Fix 'Clear/Clear all' in Programmer
* Fix ColorPicker when mixing single unit
