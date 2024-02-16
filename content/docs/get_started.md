---
title: "Getting Started"
date: 2024-02-14T18:01:29+0100
category: "Help"
---
### Download and Install BlenderDMX

See dedicated [installation page here](../installation).


### Create new show

After enabling the Addon, it shows up at the `3D View`, as a `DMX` tab on the
right side, which shows a single panel. Start the addon by clicking `Create New Show`.

![image](https://github.com/open-stage/blender-dmx/assets/3680926/b7b0e45f-e4f9-4f29-a55b-2ac1c5a3488b)


### Add fixtures

The fixture menu allows to Add/Edit/Delete a fixture. 

![image](https://github.com/open-stage/blender-dmx/assets/3680926/e48ae529-640a-432d-856d-947e7eb50339)

![image](../media/fixture_add.png)

### Setup beams

Make beams visible via menu Setup → Beam Volume → Create Volume box, to simulate
ambient fog/haze. Make sure to change Viewport to Viewport Shading".

![Volume](../media/volume.png)

### Move and control the fixture

Select the fixture in the Fixtures list

![image](../media/fixture_list.png)

In the Programmer, set color, put dimmer to 1, move pan and tilt:

![image](../media/fixture_programmer.png)

Success! Your first lighting beam fixture:

![image](../media/fixture_preview.png)
### Record keyframe


- Add Keyframe allows to manually insert keyframes related to the fixture attributes, like intensity, color, gobo, beam...
- Auto Keying turns on Blender internal auto-keying + changes to fixtures attributes (intensity, colors, gobo, beam...) are also recorded.

![image](https://github.com/open-stage/blender-dmx/assets/3680926/4ede8b00-1a7a-4387-8145-edf67ef25ece)

You can continue to the <a href="../setup" ><i class="fa-solid fa-circle-play"></i> Setup</a>.
