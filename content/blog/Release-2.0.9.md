---
title: "BlenderDMX Addon 2.0.9 Released"
date: 2025-08-20T22:21:48+0200
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v2.0.9
---
* MVR:
    - Initial support more MVR objects during import, like VideoScreens,
      Projectors, and Support
    - Add some MVR import/export filter options
    - Improve layers import and export, to keep original fixture layer
      assignment and layer names, especially useful for round-trip cooperation
    - Initial support for fixture direct parenting - direct MVR parent is now
      set as a Blender parent
    - Handle MVRs with empty fixture GDTF mode
    - Handle some occasionally missing structures in MVR
    - MVR-xchange:
        - Speed up packets packing/unpacking
        - Fix header unpacking to unsigned int values
    - Improvements to the pymvr library, update BlenderDMX to use the latest
      version 1.0.1
* Optimize rendering for incoming signals (PSN, sACN, Art-Net)
* Added more translated strings (German, French, Portuguese, Czech)
