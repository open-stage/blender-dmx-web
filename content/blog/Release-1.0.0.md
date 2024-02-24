---
title: "BlenderDMX 1.0.0 Vanilla Released"
date: 2023-03-04
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.0.0-vanilla
---

## Release Info

**Version:** v1.0.0
**Name:** Vanilla
**Contributors:** @vanous, @kasparsj 

This is the first major release of BlenderDMX, it includes a lot of new features and improvements. It definitely brings a lot to the table, so have fun with it and please report any bugs you find on the Discord server.

Special thanks for @vanous for the dedication.

## Change Log

### 🪄 New Features:
- Load glTF models
- Initial Zoom support
- Initial ColorSub_C/M/Y support
- Pigtail settings
- Show DMX channel count in list of DMX Modes
- Live DMX Table
- Pixel Control
- Initial MVR support
- Initial sACN support

### 🪲 Bugfixes:
- Render method moved to a Timer, to avoid segfaults
- Avoid running atexit handler
- Improved error handling
- Fix crash when loading DMX Macros
- Fix ColorAdd_R/G/B support
- Improved error handling
- Fix off-by-one error of ArtNet

### 🔨 Technical Improvements:
- Improved pygdtf library
- Improved logging
- Refactored model loading
