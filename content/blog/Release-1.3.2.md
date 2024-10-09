---
title: "BlenderDMX Addon 1.3.2 Released"
date: 2024-03-10T22:07:19+0100
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.3.2
---

# Pan/Tilt control and animation enhancements

Pan and Tilt control and animating has been improved by adding pan/tilt auto-lock after adjusting Target of fixtures. Target can now be selected via (Ctrl-Shift Left/Right) shortcut. Multiple pan/tilt per fixture can now be controlled (add fixtures without Target and control them via DMX). Improved logging and several bug fixes. Improvements to fixture editing, addressing and IES status indication.

* Improve pan/tilt controlling and animating:
    * Support multiple pan/tilt geometries for fixtures without Target
    * Set Ignore pan/tilt DMX (lock target) after using Target to set
      position, to allow programming keyframes by Target
    * Indicate pan/tilt lock and provide quick unlock in programmer
    * Ensure that keyframes are saved when programming position by Target
* Provide shortcut to select prev/next Target (Ctrl-Shift-Left/Right)
* Improve logging during addon initialization
* Fix fixture addressing procedure
* Add minimal required Blender version message to Setup panel
* Add links to documentation
* Add Rotation to the list of editable fixture's columns
* Indicate IES by an icon in fixture's name

