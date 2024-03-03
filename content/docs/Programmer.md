---
title: "Programmer"
date: 2024-02-15T22:01:55+0100
category: "Help"
---

BlenderDMX comes with a simple programmer, for more precise work [DMX](../dmx) is recommended.

![image](../media/programmer.png)

## To use the programmer:

- fixtures must support the corresponding attributes, for example Dimmer or Pan/Tilt.
- fixtures must be assigned to a Universe called BlenderDMX:

![image](../media/protocols_blenderdmx.png)

![image](../media/fixtures_list.png)


Following control attributes are available: Dimmer, Color, Pan, Tilt, Zoom, Gobo, GoboPos, Shutter/Strobe.

## Target

Each fixture can also be controlled via "Target" which is a virtual handle that can be manually dragged around in Blender, the head of fixtures will typically follow and point at this target. Other programs (for example Vectorworks) call this "focus point".

![image](https://github.com/open-stage/blender-dmx/assets/3680926/d7f6462b-23c2-4076-8b15-3de7b3615486)

As the Target and DMX or Programmer can interfere with each other (DMX has priority), one can lock the fixtures in place, pointing to the Target by pressing the lock icon. The lock icon is then also displayed in the Fixture list:

![image](../media/fixtures_locked.png)

You can also add the fixture and uncheck the Add target. The pan/tilt then will be controlled directly, not by following the Target.


## Selecting multiple fixtures in the Fixtures List

You can use `Shift` to select multiple fixtures. You can also use these selection icons in the programmer to:

![Edit Multiple Fixture](../media/selection.png)

- Select All
- Invert Selection
- Select Every Other Light
- Select Visible Lights Only (only filtered)
- Deselect All
- Targets to zero - places Targets to the center of the 3D space
- Lock Movement - locks movement to ignore pan/tilt data
- Unlock Movement
