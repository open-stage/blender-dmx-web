---
title: "BlenderDMX Addon 1.4.1 Released"
date: 2024-04-13T12:55:42+0200
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.4.1
---

# Initial support for Color Wheels

Color Wheels (GDTF attributes Color1, Color2 and ColorMacro1) are now
supported. If CMY/RGB color is used together with a ColorWheel, these colors
will be added together. An important handling of GDTF and MVR XML files has
been implemented to ensure broader compatibility.

* Handle XML files with null byte at the end
* Add support for Color Wheels (Color1, Color2, and ColorMacro1 GDTF attributes)

