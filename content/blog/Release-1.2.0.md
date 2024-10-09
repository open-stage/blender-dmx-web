---
title: "BlenderDMX Addon 1.2.0 Released"
date: 2024-02-11
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.2.0
---

# Keyframe Animation and DMX recording to Keyframes support added

This update is adding the missing feature of BlenderDMX Addon: keyframe based animations. Auto Keying can record sACN or Art-Net basedDMX, but also manually adjusted properties via programmer. Where needed, keyframes can be inserted with Add Keyframe button. Key frames can be deleted via dedicated Delete Keyframes from selected or from all fixtures. Native Blender key framing, sets, insertion, deletion and so on also works.

> :wrench: Gobo loading from GDTF had to be changed in non-compatible way. To upgrade an existing blender file to make gobos working again, edit Fixture(s) with gobos - re-load GDTF files: Fixtures → Edit, uncheck Re-address only.

### 1.2.0

* :film_strip:  Initial keyframing support with Auto Keying and Manual Keyframe insert
* :bulb:  Add new default 2D symbol based on BlenderDMX Addon logo
* :desktop_computer: Use BlenderDMX Addon's own Art-Net OEM code in ArtPollReply
* :ballot_box_with_check:  Select multiple fixtures in Fixture list with Shift
* :arrows_counterclockwise:  Add button to request latest version of an MVR scene from MVR-xchange
