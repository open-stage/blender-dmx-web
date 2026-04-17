---
title: "Create New Show"
date: 2024-04-07T10:56:29+0200
category: "Help"
---

## Seeing Blender error messages.

Some operations might take a while, end with an error or produce some
information into the console, it is thus advisable to always observe the
console output.

If you are on Windows, open the system console via Blender - menu - Window -
Open System Console.  If you are on other systems, run Blender from the
terminal, to see the messages: open a terminal app on your computer and start
Blender from the command line. You will then see all details and errors printed
to the terminal.

## Manual Editing of Fixture Data

Upon `Create New Show` BlenderDMX Addon creates a DMX collection in which the
BlenderDMX data is stored. Fixtures imported from GDTF reside here and these
have their own node trees for them. Manually editing or deleting data from the
DMX collection, in fixtures' geometries or node trees will likely cause the
addon to stop working. Generally, avoid such manual edits.
After enabling the Addon, it shows up at the `3D View`, as a `DMX` tab on the
right side, which shows a single panel:

## New Show

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

![image](../media/setup_beam_volume.png)

### Simple Beam

Display a semi-transparent cone representing the light beam of the current
active fixture. It works by enabling Blender's native `Show Cone` feature of
Spot Lights. This can be set to `None`, `Selected fixtures` and `All fixtures`.


#### Disable Beam Outlines

Don't display light-related overlays on the Viewport. Useful for scenes with
dozens of lights.

### Viewport Denoising

Denoise image using temporal reprojection (can leave some ghosting).

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

### Multiply Beams Intensity

![image](../media/multiply_beam_intensity.png)

Allows to make beams more (value bigger then 1) or less (value smaller then 1)
bright to quickly test various intensity settings.

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

### Custom Cutoff Distance

![image](../media/custom_cutoff_beam_distance.png)

Distance at which the influence of the light will be set to 0. Value bigger
then 23 will break gobo rendering in Eevee Next. Select desired fixtures and
press the button to apply the value.

> NOTE: Read more about [how to render lighting beams](../rendering) in BlenderDMX Addon.

## Laser collistion collection

[See Laser](/docs/laser)

## Custom Cutoff Distance

Eevee Next tries to automatically calculate the clip start/clip end based on
the maximum projection (Cutoff) distance. This automatic calculation causes
gobos to stop working, thus the Cutoff distance is set to 23m in BlenderDMX
Addon which allows the gobo projection to work. If longer beam projection is
needed, the cutoff can be adjusted manually.

![image](../media/cutoff_custom_distance.png)

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

![image](../media/display_device_label.png)

Shows a label with Device name/DMX address/Fixture ID above the device in 2D or 3D.

## Display Pigtails

Show/Hide the Pigtail - position where the fixture's wiring connections are,
typically indicating where back of the fixture is.

## Allow Selecting Geometries

Normally, only Base and Target of the fixture can be selected. The `Allow
Selecting Geometries` option allows to select any part of the fixture. The
BlenderDMX Addon uses a DMX collection in which the BlenderDMX data is stored.
Fixtures imported from GDTF reside here and have own node trees in there.
Manually editing or deleting data from the DMX collection, in fixtures'
geometries or node trees will likely cause the addon to stop working.
Generally, avoid such manual edits. If you break a fixture or its collection,
the BlenderDMX Addon might stop working correctly, and even Fixture → Edit
might stop working. You can [force-delete fixture via the Fixture
list](../fixture/#force-delete-fixture).

## Logging

![image](../media/setup_logging_level.png)

You can enable increased level of logging via this menu. Normally, only
`Errors` are logged (displayed in the terminal and written to a log file). By
choosing `Warning`, `Info` or even `Debug` you get more and more details. If
you experience issues, it is good to start Blender from a terminal to see what
the logging output shows and set increased level of logging.

You can also further filter the logging by selecting the highest level of
logging (`Debug`) and setting the Log filter, to only log specific parts of the
BlenderDMX Addon, like data related to MVR-xchange protocol, DMX Data or data related
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
  zip file, for a later Import or when sharing the .blend file with someone.
- MVR export of the complete scene including the fixtures and scene objects.

NOTE: Gobo images, MVR 3D models, MVR textures and so on must be kept within
the addon directory. The [Setup - Export/Import Project data](#import) allows
to Export/Import project data.

## Extras

![image](../media/setup_extras.png)

### Clear Project Data

Clears the assets directory.

### Copy data from addon to user directory

Copy custom data from BlenderDMX addon directory to BlenderDMX extension user
directory.

### Remove DMX from blend file

Remove DMX from the Blender showfile

### User Guide

Opens this documentation in web browser.
