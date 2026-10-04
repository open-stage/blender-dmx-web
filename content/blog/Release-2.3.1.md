---
title: "BlenderDMX Addon 2.3.1 Released"
date: 2026-10-04T22:05:00+0200
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v2.3.1
---

### 2.3.1

* Added translation using Weblate (Ukrainian) [Ahha]
* Add option to remove a Universe, use Blender style UI for universe adding/removing
* Fix Focus Point on Blender created data, fix UUID assignment, for correct MVR export
* Set SO_REUSEPORT on the Art-Net socket so a console on the same machine can share port 6454
* Initial support for Sinette protocol - a very simple plain data receiver added
* Use non-fixture GDTF data during import from MVR
* Fix emitter dimmer while strobing, cap strobe to fps/2 thanks to @EricNakamura in #363

## New Contributors
* @CristianDeluxe made their first contribution in https://github.com/open-stage/blender-dmx/pull/366

**Full Changelog**: https://github.com/open-stage/blender-dmx/compare/v2.3.0...v2.3.1
