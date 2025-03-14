## Target and Pan/Tilt

Each fixture can also be controlled via "Target" which is a virtual handle that
can be manually dragged around in Blender, the head of fixtures will typically
follow and point at this Target. Other programs (for example Vectorworks) call
this "focus point".

![image](../media/target.png)

If the fixture has a DMX controllable pan and tilt, the DMX from console or
from the Programmer can interfere with the Target (DMX has priority). One can
lock the fixtures in place, by pressing the lock icon. The lock icon is then
also displayed in the Fixture list:

![image](../media/fixtures_locked.png)

Fixtures can be locked/unlocked via the icons in the Programmer:

![icons](../media/selection.png)

If you have just a single fixture selected, pan/tilt lock is indicated in the
Programmer and one can unlock it by clicking the unlock icon:

![image](../media/single_fixture_locked.png)

You can also add the fixture to the scene without a Target at all. To do so,
Add Fixture and uncheck the Add Target. If the fixture has DMX controllable
pan or tilt, it can be controlled directly by DMX.
