---
title: "BlenderDMX Addon 2.0.8 Released"
date: 2025-07-26T23:11:03+0200
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v2.0.8
---
# Improved Art-Net 4 compatibility

As Art-Net 4 no longer supports broadcasting of DMX values, the BlenderDMX
Addon must ensure to correctly advertise required DMX universes, in order to
receive DMX from Art-Net 4 transmitters. [Michael
Wigard](https://github.com/miwig) has deeply investigated this and improved the
ArtPollReply, to conform to the specification.

MVR Export has been improved by eliminating a bug which could cause data to be
duplicated during subsequent exports. The Python GDTF and MVR libraries have
received a huge overhaul and are now included. Clearing Programmer should now
result in fixtures to be set to their default values (if only one fixture type
is being selected). When adding new fixtures to the scene, they should now have
correct, default values from the very beginning.

Changelog:

* Prevent MVR persistence during export, to eliminate duplication during export
* Update to latest pygdtf and pymvr libraries
* Improvements to Art-Net 4 compatibility, thanks to Michael Wigard
* Ensure that Programmer Clear sets the fixtures to default values
* Ensure that fixture is set to default and rendered after being added to the
  scene
