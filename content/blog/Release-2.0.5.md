---
title: "BlenderDMX Addon 2.0.5 Released"
date: 2025-06-16T22:31:46+0200n
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v2.0.5
---

# Initial support for multi-station MVR-xchange

This update extends the local (TCP) implementation of the MVR-xchange protocol
to allow exchange of MVR files in a group of stations.

* MVR-xchange - initial support for multiple connections
* Progress of Swedish translation by Daniel Nylander
* Set all protocols as disabled when a blender file is being open
* Add option to Beam setting to disable Temporal Reprojection in Eevee
* Ensure that fixture can always be removed from the list of fixtures even if
  the fixture had been damaged by manual edits
