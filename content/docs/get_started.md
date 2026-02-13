---
title: "Getting Started"
date: 2024-04-07T10:55:44+0200
category: "Help"
---

### Download and Install BlenderDMX Addon

See dedicated [Download page here](/download).

### Important

#### Seeing Blender error messages.

Some operations might take a while, end with an error or produce some
information into the console, it is thus advisable to always observe the
console output.

If you are on Windows, open the system console via Blender - menu - Window -
Open System Console.  If you are on other systems, run Blender from the
terminal, to see the messages: open a terminal app of your computer and start
Blender form the command line. Yo will then see all details and errors being
printed into the terminal.

#### Manual Editing of Fixture Data

Upon `Create New Show` BlenderDMX Addon creates a DMX collection in which the
BlenderDMX data is stored. Fixtures imported from GDTF reside here and these
have their own node trees for them. Manually editing or deleting data from the
DMX collection, in fixtures' geometries or node trees will likely cause the
addon to stop working. Generally, avoid such manual edits.

### Create new show

After enabling the Addon, it shows up at the `3D View` as a `DMX` tab on the
right side, which shows a single panel. If you cannot see the side bar, press
`N`. Start the addon by clicking `Create New Show` in the `DMX` tab.

![image](../media/create_new_show.png)

### Add fixtures

The fixture menu allows to Add/Edit/Remove a fixture.

Select Add:

![image](../media/fixture_menu.png)

In the GDTF Profile - BlenderDMX Addon, select BeskydBeam. Keep the rest as is and
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

Keyframe recording in BlenderDMX Addon is in menu Keyframe Recorder:

- Add Keyframe allows to manually insert keyframes related to the fixture attributes, like intensity, color, gobo, beam...
- Auto Keying turns on Blender internal auto-keying + changes to fixtures attributes (intensity, colors, gobo, beam...) are also recorded.

![image](../media/keyframe_recorder.png)

You can continue to the <a href="../setup" ><i class="fa-solid fa-circle-play"></i>User Guide</a>
