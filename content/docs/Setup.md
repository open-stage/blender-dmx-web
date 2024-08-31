---
title: "Create New Show"
date: 2024-04-07T10:56:29+0200
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
active fixture. It works by enabling Blender's native `Show Cone` feature of
Spot Lights. This can be set to `None`, `Selected fixtures` and `All fixtures`.

#### Disable Beam Outlines

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

## Pause Renderer

During GDTF and MVR import and also in 2D View, rendering is paused, to prevent
issues and to speed things up. This toggle is here in case it needs to be
manually re-enabled.

## Display 2D View

Switches the view to the TOP view, hides 3D models of fixtures and shows 2D
symbol from GDTF. This 2D is aligned with 3D. Clicking on 2D will make 3D model
of selected fixture visible and it can now by positioned and rotated. The 2D
symbol will be also positioned and rotated in Z axis.

![image](../media/2d_view.png)

## Display Device Label

Shows a label with device name/DMX address/Fixture ID above te device in 2D or 3D.

## Display Pigtails

Show/Hide the Pigtail - position where the fixture's wiring connections are,
typically indicating where back of the fixture is.

## Allow Selecting Geometries

Normally, only Base and Target of the fixture can be selected. This option
allows to select any part of the fixture.

## Logging

![image](../media/setup_logging_level.png)

You can enable increased level of logging via this menu. Normally, only
`Errors` are logged (displayed in the terminal and written to a log file). By
choosing `Warning`, `Info` or even `Debug` you get more and more details. If
you experience issues, it is good to start Blender from a terminal to see what
the logging output shows and set increased level of logging.

You can also further filter the logging by selecting the highest level of
logging (`Debug`) and setting the Log filter, to only log specific parts of the
BlenderDMX, like data related to MVR-xchange protocol, DMX Data or data related
to Fixtures.

If you experience some issues or crashes, try to increase the logging level to
`Debug` and replicate the action leading to the error, then look into the
terminal and into the "blenderDMX.log" logfile if you see anything obvious.
Eventually, take the error message or the full blenderDMX.log log file and ask
in the <strong><a rel="me" href="https://discord.gg/FQVVyc45T9"><i
class="fa-brands fa-discord" aria-hidden="true"></i> Discord</a> </strong>
group.

## Import

![image](../media/setup_import.png)

- GDTF files can also be imported via `Import GDTF Profile` or via Blender -
  File - Import. You can read more about [GDTF here](../gdtffixture/).
- Full scene can be imported with the `Import MVR Scene`, or via Blender - File
  \- Import. You can read more about [MVR here](../gdtffixture/#mvr).
- `Import Project data` - project data (GDTF files, gobos, MVR textures and so
  on) can be Imported from previously Exported zip file with Project data.

## Export

![image](../media/setup_export.png)

- Project data (GDTF files, gobos, MVR textures and so on) can be Exported to a
  zip file, for a later Import.
- MVR export currently supports expoting fixtures.

## Extras

![image](../media/setup_extras.png)

## Clear Project Data

Clears the assets directory.

## User Guide

Opens this documentation in web browser.
