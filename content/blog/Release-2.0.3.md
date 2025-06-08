---
title: "BlenderDMX Addon 2.0.3 Released"
date: 2025-06-08T15:17:13+0200
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v2.0.3
---
### Add Initial Support for a Light-bulb Like Devices

* Add initial support for DMX controlled bulb light like devices
* Use model of geometry reference if provided
* Update pygdtf to 1.2.5
  * Handle parsing of incorrect DmxValue values
  * Return default FixtureType if ElementTree.fromstring fails on malformed XML
