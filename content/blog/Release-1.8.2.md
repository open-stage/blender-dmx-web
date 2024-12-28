---
title: "BlenderDMX Addon 1.8.2 Released"
date: 2024-12-28T19:44:59+0100
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.8.2
---
# MVR-xchange sending and receiving support

## Translations

Numerous [translations have been
added](https://hosted.weblate.org/projects/blenderdmx/main/). Many thanks to
all contributors.

## GDTF Imports

The [pygdtf library](https://github.com/open-stage/python-gdtf) has received
several improvements.

## MVR-xchange sending and receiving

Previously, only file receiving on MVR-xchange has been available. With the
fixture [export to MVR added this
summer](https://blenderdmx.eu/blog/release-1.7.0/), the sending part of
MVR-xchange has been implemented in this release. It has been tested and
confirmed working between two Linux stations, but the implementation will need
more work as file transfer between machines on Windows still does have some
issues.

## Changelog

See the changelong for more information, or developers can look at [git
log](https://github.com/open-stage/blender-dmx/commits/main/) for full details.

* Update pygdtf to pygdtf-1.0.5.dev8
* Translated using Weblate:
    * (Czech) (origin/main, origin/HEAD) [vanous]
    * (Italian) [Fede Pre]
    * (Tamil) [தமிழ்நேரம்]
    * (Chinese (Simplified Han script)) [大学没毕业]
* MVR-xchange update:
    * Add serving part of MVR-xchange
    * Show date time of commits, ensure mDNX groups have no dots
    * Add search to MVR-xchange panels
    * Change mDNS sub service naming
* Add confirmation dialog Allow selecting geometries
* Improve message of dialog Clear custom data
* Print extension version to the terminal on startup
