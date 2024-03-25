---
title: "Create New Show"
date: 2024-02-15T22:01:55+0100
category: "Help"
---

After enabling the Addon, it shows up at the `3D View`, as a `DMX` tab on the
right side, which shows a single panel:

![image](../media/create_new_show.png)

By clicking `Create New Show`:

- A new `DMX` collection is created on the Scene;
- DMX Data Structures are created on the Blender File;
- All DMX Panels are registered, offering full control of fixtures and
  channels;

When the Blender file is saved, all of the DMX data such as Universes, Fixtures
and Addresses are stored with it. When you open the file, the DMX panels should
already be available.

> Manipulating the `DMX` collection manually might corrupt the
> project file, be careful.

# Setup

![image](../media/setup.png)

## Beam Volume

### Simple Beam

![image](../media/setup_beam_volume.png)

Display a semi-transparent cone representing the light beam of the current
active fixture.  It works by enabling Blender's native `Show Cone` feature of
Spot Lights. This can be set to `None`, `Selected fixtures` and `All fixtures`.

#### Disable Overlays

Don't display light-related overlays on the Viewport. Useful for scenes with
dozens of lights.

### Volume Box


![image](../media/setup_volume_box.png)

### Create/Update Volume Box

Create a box around the whole scene with a haze - a `Volume Scatter` shader, to simulate
ambient fog/haze.

### Enable Volume Scatter

Toggle the visibility of the Volume Box.

### Density

Density of the `Volume Scatter`, basically the density of fog/haze in the room. Default is 0.1 .

### Noise Scale

Noise Scale of the generated fog.

### Beam Lens Diameter in Cycles

![image](../media/setup_beam_diameter.png)

![image](../media/beams.png)

This allows to adjust how beam rendering in Cycles looks when rendering gobos -
whether beam looks really nice and fills the beam lens (`Full width`), but
gobos can be a bit blurry, or, gobos are really sharp, but beam starts in front
of the lens (`Reduced`). If set to `Custom`, one can set the "beam radius pin
sized for gobos" attribute on each light beam to True/False either manually or
via the following quick set buttons:

![image](../media/setup_beam_diameter_custom.png)


## Beam rendering

Read more about [how to render lighting beams](../rendering) in BlenderDMX.

# Viewport

![image](../media/setup_viewport.png)

## Background

A background color. This picker alters the World Shading, by directly altering
the Color Node attribute.
## Pause renderer

During GDTF and MVR import and also in 2D View, rendering is paused, to prevent
issues and to speed things up. This toggle is here in case it needs to be
manually re-enabled.

## Display 2D View

Switches the view to the TOP view, hides 3D models of fixtures and shows 2D
symbol from GDTF. This 2D is aligned with 3D. Clicking on 2D will make 3D model
of selected fixture visible and it can now by positioned and rotated. The 2D
symbol will be also positioned and rotated in Z axis.

![image](https://github.com/open-stage/blender-dmx/assets/3680926/a6a0b2e9-4e56-438d-8d9a-072c320f7c71)

## Display Pigtails

Show/Hide the Pigtail - position where the fixture's wiring connections are, typically indicating where back of the fixture is.

## Allow Selecting Geometries

Normally, only Base and Target of the fixture can be selected. This option allows to select any part of the fixture.

## Logging

![image](../media/setup_logging_level.png)

You can enable increased level of logging via this menu. Normally, `Errors` are
displayed. By choosing `Warning`, `Info` or even `Debug` you get more and more
details in the terminal. If you experience issues, it is good to start Blender
from a terminal to see what the logging output shows and set increased level of
logging.

By selecting the highest level of logging (`Debug`) and setting the Log filter,
one specific parts of the BlenderDMX are logged, like data related to
MVR-xchange protocol, DMX Data or data related to Fixtures.

## Extras

![image](../media/setup_extras.png)

This allows to check if there is newer version of BlenderDMX released.

