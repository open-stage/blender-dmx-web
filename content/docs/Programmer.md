---
title: "Programmer"
date: 2024-02-15T22:01:55+0100
category: "Help"
---

BlenderDMX comes with a simple programmer, for more precise work [DMX](../dmx) is recommended.

![image](https://github.com/open-stage/blender-dmx/assets/3680926/47cf27c4-e387-432a-a13b-ff223cd0c9a9)

To use the programmer:

- fixtures must support the corresponding attributes, for example Dimmer or Pan/Tilt.
- fixtures must be assigned to a Universe called BlenderDMX:

![image](https://github.com/open-stage/blender-dmx/assets/3680926/b14e2b32-baa8-4327-abfc-b417c9e3310a)

![image](https://github.com/open-stage/blender-dmx/assets/3680926/e0a3061a-fac5-4e40-8de1-8d60ccaed1af)


Following control attributes are available: Dimmer, Color, Pan, Tilt, Zoom, Gobo, GoboPos, Shutter/Strobe.

# Target

Each fixture can also be controlled via "Target" which is a virtual handle that can be manually dragged around in Blender, the head of fixtures will typically follow and point at this target. Other programs (for example Vectorworks) call this "focus point".

![image](https://github.com/open-stage/blender-dmx/assets/3680926/d7f6462b-23c2-4076-8b15-3de7b3615486)

As the Target and DMX or Programmer can interfere with each other (DMX has priority), one can lock the fixtures in place, pointing to the Target by pressing the lock icon. The lock icon is then also displayed in the Fixture list:

![image](https://github.com/open-stage/blender-dmx/assets/3680926/f842fd21-11e2-40ce-a65c-e4ebcd8c82e0)



