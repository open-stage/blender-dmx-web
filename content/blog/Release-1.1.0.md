---
title: "BlenderDMX Addon 1.1.0 Released"
date: 2024-01-18
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.1.0
---

# Big MVR-xchange update and many quality of life improvements

MVR-xchange support has been redesigned to follow the MVR Spec more closely, given the fact that BlenderDMX Addon does not export MVR files, making it a data consumer only at this point. LiveDMX view has been optimized and it can now show DMX values realtime without delay. Fixture add/edit has been improved to allow incrementing (or not) fixture IDs and addresses. BlenderDMX Addon now creates a log file for easier reporting.

[Better_LiveDMX.webm](https://user-images.githubusercontent.com/3680926/297882089-de76687e-4245-4359-9535-ddc449ae6739.webm)

### 1.1.0

* MVR-xchange:
    * Add proper listener and sender (client and server) to MVR-xchange, to match the Spec
    * Many other improvements to MVR-xchange
* Logging:
    * Ensure that logger is not initialized multiple times
    * Add logging to file
    * Add filters to allow logging only specific parts of the app
    * Convert most prints() to log
* UI:
    * Speed up LiveDMX view refresh
    * When adding/editing fixtures, allow to (not)increment address/id
    * Set 2D view to Material rather then Solid
    * Reorganize Setup panels
    * Ensure automatic UI refresh for several panels
* GDTF/MVR/Fixtures:
    * Speed up DMX values caching for render loop bypass
    * Scale gobo planes during fixture creation
    * Unzip correctly files with non latin encoding in file names
