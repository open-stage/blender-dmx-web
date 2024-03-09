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

Each fixture can also be controlled via "Target" which is a virtual handle that
can be manually dragged around in Blender, the head of fixtures will typically
follow and point at this Target. Other programs (for example Vectorworks) call
this "focus point".

![image](https://github.com/open-stage/blender-dmx/assets/3680926/d7f6462b-23c2-4076-8b15-3de7b3615486)

If the fixture has a pan and tilt, the Target and DMX from console or from the
Programmer can interfere with the Target (DMX has priority). One can lock the
fixtures in place, pointing to the Target by pressing the lock icon. If you
have adjusted focusing of the fixture by dragging the Target, pan and tilt are
automatically set to the locked state. The lock icon is then also displayed in
the Fixture list:

![image](../media/fixtures_locked.png)

Fixtures can be locked/unlocked via the icons in the Programmer:

![icons](../media/selection.png)

If you have just a single fixture selected, pan/tilt lock is indicated in the
Programmer and one can unlock it by clicking the unlock icon:

![image](../media/single_fixture_locked.png)

You can also add the fixture to the scene without a Target at all. This is
useful if the fixture doesn't have a beam, doesn't have pan/tilt and so on. To
do so, Add Fixture and uncheck the Add Target. If the fixture has pan/tilt, it
can be controlled directly by DMX or Programmer, not by following the Target.

## Selecting multiple fixtures in the Fixtures List

You can use `Shift` to select multiple fixtures.

## Selection icons in Programmer

You can use these selection icons in the programmer to:

![Edit Multiple Fixture](../media/selection.png)

- Select All
- Invert Selection
- Select Every Other Light
- Select Visible Lights Only (only filtered)
- Deselect All
- Targets to zero - places Targets to the center of the 3D space
- Lock Movement - locks movement to ignore pan/tilt data
- Unlock Movement
