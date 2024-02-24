---
title: "BlenderDMX 1.0.5 Released"
date: 2023-12-17
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.0.5
---

# Network improvements, OpenSoundControl addition, MVR re-import and much more

Several quality of life improvements have been added, like improved fixture editing, dynamic list of network interfaces or added support for MVR re-import (this is huge - now we re-import an MVR scene with changes from other parties). Integration with consoles via OpenSoundControl protocol now sends the fixture selection to a console. Selected fixtures can now be jumped previous/next with Control-Left/Control-Right keyboard keys. Read on for more news.

[BlenderDMX_BlinderKitten_integration.webm](https://github.com/open-stage/blender-dmx/assets/3680926/21036edc-4b7e-4677-912a-29c01b5a86d3)


### 1.0.5

* Set beam type based on Spot/Wash/None beam types as defined in GDTF
* Allow MVR reimport:
    * existing objects/fixtures/trusses... (by UUIDs) will be updated by data
      in MVR
    * new objects... will be added to the scene
    * there is a new internal structure for scene objects, not visible to the
      user at this point
* Add OpenSoundControl (OSC):
    * send fixture selection to consoles
    * allow multiple commands to be sent
    * definition in json
* Network improvements:
    * list of IPs is now dynamic
    * add 0.0.0.0 to the IP list
* Device and group listing and editing:
    * Show number of fixtures in a group
    * Allow to soft fixtures differently
    * Allow incremental Fixture IDs
    * Use original fixture's UUID during fixture edit
    * Improve 'Re-address only' dialog
* Handle errors during fixture adding more gracefully:
    * do not add the fixture to the fixture list
    * remove bad collection
    * show error message
    * allow to remove non-selectable fixtures
* Fix group creation during MVR import
* Apply stored position and rotation only on root geometry
* Use fixture UUIDs instead of names in groups (ensures group validity on fixture
  rename):
    * ensure unique UUIDs in fixtures
    * ensure unique UUIDs in groups
* Add DMX data caching to shortcut render loop to prevent flicker a bit
