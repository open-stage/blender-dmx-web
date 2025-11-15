---
title: "BlenderDMX Addon 2.0.15 Released"
date: 2025-11-15T12:15:07+0100
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v2.0.15
---
## Allow to synchronize the start of DMX recording

When recording DMX as key-frames, it is useful to start the recording in
Blender based on cue timing in the DMX console. The new BlenderControl GDTF
device and support in BlenderDMX allows to trigger the auto-keyframe and the
animation/timeline play state from DMX. See details in the
[documentation](https://blenderdmx.eu/docs/keyframe-animations-recording/#controlling-blender-controls-via-dmx).

* Add initial support to control Blender controls via DMX
* Update pygdtf
* Translated using Weblate (French) [David D]
* Fix device label - use first dmx_break for uni.addr

**Full Changelog**: https://github.com/open-stage/blender-dmx/compare/v2.0.14...v2.0.15
