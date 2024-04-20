## Target and Pan/Tilt

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

You can also add the fixture to the scene without a Target at all. To do so,
Add Fixture and uncheck the Add Target. If the fixture has pan/tilt, it can be
controlled directly by DMX or Programmer, not by following the Target.
