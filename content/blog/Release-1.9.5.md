---
title: "BlenderDMX Addon 1.9.5 Released"
date: 2025-04-21T22:45:08+0100
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.9.5
---

## Add full support for DMX Breaks

* Allow proper patching of fixtures with multiple DMX entry points (DMX Breaks)
* Centralize GDTF loading to gain speed
* Add possibility to Set Eevee Cutoff distance on selected fixtures
* Accommodate to latest pygdtf changes - use channels directly and so on

There is a migration procedure to make sure older .blend files can be open, but
you will have to use the Fixtures → Edit → Advanced Edit → OK, to have the
fixtures' data to be re-generated.

### Changelog

* Handle incorrect GDTF files during initial import
* Add more strings to translations
* Allow to set Custom Cutoff distance in Eevee
* Handle GDTF files without DMX Breaks. Ensure profiles refresh on import
* Translated using Weblate (Turkish)
* Implement support for DMX Breaks (#256)
* Adjust the Donation section in README
* Ensure that all code authors are mentioned in all files:
* Translated using Weblate (German)
* Translated using Weblate (French)
* Translated using Weblate (Spanish)
* Translated using Weblate (Chinese (Simplified Han script))
* Use directly some pygdtf features for dmx modes/channels info
* Adjust code to use latest pygdtf changes - Rename 'id' to 'attribute' - Handle removed method from pygdtf.utils - Use the pygdtf's context manager
