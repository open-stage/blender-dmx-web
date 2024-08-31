---
title: "Getting Started"
date: 2024-04-07T10:55:44+0200
category: "Help"
---
### Download and Install BlenderDMX

See dedicated [Download page here](/download).


### Create new show

After enabling the Addon, it shows up at the `3D View`, as a `DMX` tab on the
right side, which shows a single panel. Start the addon by clicking `Create New Show`.

![image](../media/create_new_show.png)


### Add fixtures

The fixture menu allows to Add/Edit/Remove a fixture.

Select Add:

![image](../media/fixture_menu.png)

In the GDTF Profile - BlenderDMX, select Moving Beam. Keep the rest as is and
click OK:

![image](../media/fixture_add.png)

### Setup beams

Make beams visible via menu Setup → Beam Volume → Create Volume Box, to simulate
ambient fog/haze. Make sure to change Viewport to Viewport Shading:

![Volume](../media/volume.png)

### Move and control the fixture

Select the fixture in the Fixtures list:

![image](../media/fixture_list.png)

In the Programmer, set color, put dimmer to 1, move pan and tilt:

![image](../media/fixture_programmer.png)

Success! Your first lighting beam fixture:

![image](../media/fixture_preview.png)

The rendered volumetric beam can be made much nicer, see <a
href="../rendering/" >Beam Rendering.</a> for more information.

### Record keyframe

Keyframe recording in BlenderDMX is in menu Keyframe Recorder:

- Add Keyframe allows to manually insert keyframes related to the fixture attributes, like intensity, color, gobo, beam...
- Auto Keying turns on Blender internal auto-keying + changes to fixtures attributes (intensity, colors, gobo, beam...) are also recorded.

![image](../media/keyframe_recorder.png)

You can continue to the <a href="../setup" ><i class="fa-solid fa-circle-play"></i> User Guide</a>


