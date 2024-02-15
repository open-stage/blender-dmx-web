---
title: "Create New Show"
date: 2024-02-15T22:01:55+0100
category: "Help"
---
After enabling the Addon, it shows up at the `3D View`, as a `DMX` tab on the
right side, which shows a single panel:

![image](https://github.com/open-stage/blender-dmx/assets/3680926/b7b0e45f-e4f9-4f29-a55b-2ac1c5a3488b)

By clicking `Create New Show`:
- A new `DMX` collection is created on the Scene;
- DMX Data Structures are created on the Blender File;
- All DMX Panels are registered, offering full control of fixtures and
  channels;

When the Blender file is saved, all of the DMX data such as Universes, Fixtures
and Addresses are stored with it. When you open the file, the DMX panels should
already be available.

> :warning: Manipulating the `DMX` collection manually might corrupt the
project file, be careful.

# Setup

![image](https://github.com/open-stage/blender-dmx/assets/3680926/e4d53b9a-e9be-4201-b1ad-9d8fc001fe37)

## Background

A background color. This picker alters the World Shading, by directly altering 
the Color Node attribute.

## Volume

### Preview Volume

Display a semi-transparent cone representing the light beam of the current active fixture. 
It works by enabling Blender's native `Show Cone` feature of Spot Lights. This can be set to None, Selected fixtures and All fixtures.

### Disable Overlays

Don't display light-related overlays on the Viewport. Useful for scenes with 
dozens of lights.

### Create Volume Box

Create a box around the whole scene with a haze - a `Volume Scatter` shader, to simulate
ambient fog/haze.

### Enable Volume Scatter

Toggle the visibility of the Volume Box.

### Density

Density of the `Volume Scatter`, basically the density of fog/haze in the room. Default is 1.0, set it typically
to lower value, like 0.1

## Beam rendering

Read more about [how to render lighting beams](../rendering) in BlenderDMX.

# Extras

## Pause renderer

During GDTF and MVR import and also in 2D View, rendering is paused, to prevent issues and to speed things up. This toggle is here in case it is by accident to re-enabled.

## Display 2D View

Switches the view to the TOP view, hides 3D models of fixtures and shows 2D symbol from GDTF. This 2D is aligned with 3D. Clicking on 2D will make 3D model of selected fixture visible and it can now by positioned and rotated. The 2D symbol will be also positioned and rotated in Z axis.

![image](https://github.com/open-stage/blender-dmx/assets/3680926/a6a0b2e9-4e56-438d-8d9a-072c320f7c71)


## Display Pigtails

Show/Hide the Pigtail - position where the fixture's wiring connections are, typically indicating where back of the fixture is.

## Allow Selecting Geometries

Normally, only Base and Target of the fixture can be selected. This option allows to select and move/rotate... any part of the fixture. This also allows the possibility to add IES files to the beam Spot light objects, see [documentation here](https://docs.blender.org/manual/en/latest/render/shader_nodes/textures/ies.html) and some [tutorials on the web](https://duckduckgo.com/?t=ffab&q=blender+ies).

## Logging

You can enable higher level of logging via this menu. Normally, Errors are displayed, by choosing Warning, Debug or Info you gets more and more details in the console. If you experience issues, it is good to start Blender from a console to see what the logging output shows.


<a href="/docs/user_guide/">Back to User Guide index</a>
