---
title: "Fixtures"
date: 2024-04-07T10:57:47+0200
category: "Help"
---

Fixture profiles come from GDTF, [read details here](../gdtffixture).

# Importing GDTF files

To import an existing local GDTF file, use the `Setup - Import - Import GDTF
Profile`:

![image](../media/gdtf_fixture_import.png)

You can also use the [GDTF Share
Integration](/docs/gdtffixture/#gdtf-share-integration-in-blender) into
BlenderDMX Addon, to download and import the GDTF files provided on the GDTF
Share.

GDTF Profiles imported into the BlenderDMX Addon can then be used via the
menu: [Fixture - Add - GDTF Profile](#add-fixture).


# Fixture

Fixture represents a GDTF device. This can be a static/moving lighting fixture
but also a laser, a truss or any other 3D object in a GDTF file.

Listing mode:

![image](../media/fixtures_listing.png)

Edit mode:

![image](../media/fixtures_edit.png)

Explanation of extra icons:

![image](../media/fixtures_list_explanation.png)

1) Pan/Tilt locked
2) IES Photometrics linked
3) Unsaved changes in the Programmer
4) DMX footprint overlap


The `Fixture Panel` selection is synced to the Viewport.

If you delete a fixture on the Viewport, it is deleted from the DMX show and [Groups](../groups) as
well.

## Fixture menu

The fixture menu allows to Add/Edit/Delete a fixture.

![image](../media/fixture_menu.png)



## Add Fixture

![image](../media/add_fixture.png)

- **Name:** Name of the Fixture.
- **GDTF Profile:** Select the GDTF Profile from the BlenderDMX Addon library.
- **DMX Mode:** Select the DMX Mode of the selected GDTF Profile.
- **Universe:** DMX Universe of the Fixture.
- **Address:** DMX Address of the Fixture.
- **Fixture ID:** The fixture ID of the first fixture.
- **Units:** How many fixtures should be created.
- **Increment DMX address:** Whether to increase DMX address when adding multiple devices
- **Increment Fixture ID:** Whether to increase Fixture ID when adding multiple devices
- **Fixture ID:** An ID of the fixture. Currently this is not used in BlenderDMX Addon. It can be a number or text
- **Display beams:** Eevee has limit of 120 beam per scene, so sometimes it is useful to create front facing devices only with the Emitter lens but without a beam
- **Add Target:** When adding for example XYZ_X,Y,Z fixtures, the target is not needed. Also, sometimes the Target is not useful. This allows not to add it.
- **Gel Color:** A subtractive color filter applied to the lamp color. Useful
  for mimicking white balance on lamps.

## Edit Fixture

If `Advanced edit` is unchecked, the GDTF Profile, DMX Mode and Gel Color are not editable, this speeds up the editing as the GDTF profile does not need to be re-evaluated. This option also allows to assign and remove an IES photometric file to the selected fixtures.

![Edit Single Fixture](../media/edit_simple.png)

- **Universe:** Set DMX Universe
- **Address:** The addresses are set starting at the first selected Fixture
- **Fixture ID:** The fixture ID starting at the first selected Fixture
- **Re-address only** Allows for fast DMX address/universe, fixture id... settings
- **Import IES File** Allows to Import IES File and links it to selected fixtures's beams
- **Remove IES File** Removes IES File from selected fixtures
- **Increment DMX address:** Whether to increase DMX address when editing multiple devices
- **Increment Fixture ID:** Whether to increase Fixture ID when editing multiple devices
If `Re-address only` is un-checked, all options are available and the GDTF Profile is re-evaluated.

![Edit Single Fixture](../media/edit_full.png)

When selecting **Advanced edit**

- **Name:** If you keep the `*`, it keeps fixture names. Otherwise, it appends
  an integer index to the end of the given name for each fixture being edited.
- **GDTF Profile:** If you don't select anything, features remain the same.
  Otherwise, it replaces every selected fixture with the selected profile.
- **DMX Mode:** Same as GDTF Profile.
- **Universe:** Same as GDTF Profile.
- **Address:** The addresses are set starting at the first selected Fixture,
  and growing according to the fixture footprints.
- **Gel Color:** Same as GDTF Profile.


## DMX Addressing

Each fixture needs to have a DMX address. This address is a starting value from
which the fixture will be receiving data from the DMX stream and the amount of
received data depends on the amount and type of controllable parameters of the
fixture. Different types of fixtures typically have different amount of
controllable parameters, thus different amount of required DMX channels (often
called "DMX footprint"). The addresses thus need to be spaced in such a way
that the fixtures and their DMX footprints do not overlap. See more details
about [DMX here](../dmx).


## Remove fixture

You can select fixture(s) and remove them by using the Remove Fixture menu item. There can be situations when the fixture is not possible to select. It can be removed by making the fixture list Editable and then clicking the cross icon:

![image](../media/remove_fixture.png)

## Import IES File/Remove IES File

This allows for more photo-realistic volumetric beam rendering. Example of beams without (left) and with (right) IES:

![image](../media/ies.png)

## GDTF Attributes usage in BlenderDMX Addon

See sections below for details on how are some GDTF attributes applied in
BlenderDMX Addon.

## Colors

### Color Mixing

All supported color mixing attributes (ColorAdd_R, G, B; ColorRGB_Red, Green,
Blue; ColorSub_C, M, Y; ColorAdd_C, M, Y, Amber, Lime, UV, White, WarmWhite,
CoolWhite) are linked to the color picker. CMY is converted to RGB. By default,
the color picker is set to white.


### Color Temperature Control (CTC)

CTO, CTC and CTB are used to adjust color temperature from 1100K to 12000K. 

### Color Wheels

Supported attribures (Color1, Color2, ColorMacro1) are linked to the Color
Wheel selection.

### Color Mixing and Color Wheels together

If Color Mixing is not at White and a Color Wheel is used, the colors are added
together and the resulting color is applied to the projected beam. The current
implementation is very basic. When later re-selecting a fixture and setting the
Programmer, the previously calculated resulting color is applied to the color
wheel.

## Gobos

Upon loading GDTF files, gobos must be converted to Blender's image sequence,
in order to be possible to keyframe them. Image sequences cannot be saved into
the blender file, this means that in order for the gobos to work, GDTF files
must be kept within the addon directory.

### Gobo Selection

Gobo1 and Gobo2 are supported. All images are available on both gobo wheels.
All images from `media` folder are utilized, so if for example animation wheel
image is in there, it is possible to select it.

### Gobo Rotation

Gobo1Pos, Gobo2Pos and Gobo1PosRotate, Gobo2PosRotate are supported. This is
done by adjusting angle (for static indexing) and adding a Blender driver
(`frame * selected value`) to the image Euler for rotation. Blender animation
player must be playing.

### Gobo visualization

Eevee has to be used at least once with gobos, for gobos to render in Cycles,
otherwise pink color is rendered instead of images.  Simply switch the renderer
to Eevee and back to Cycles and gobos will show up.  This seems as either some
combination of things or a bug in Blender.

In Cycles, beam is rendered as starting from the beam lens, with the width of
the lens diameter. This can make gobo projection slightly blurry. See [details
here](../setup/#beam-lens-diameter-in-cycles).

![image](../media/beams.png)

## Strobe

Strobing is supported if the fixture has Shutter1 attribute. Strobe is
currently not keyframeable.

## Continuous pan/tilt rotation

PanRotation/TiltRotation attributes are used to provide continuous pan/tilt
rotation. Blender animation player must be playing to see the rotation. If you
want just one axis to be moving, the other axis can be locked (unlocked) via
the provided Lock/Unlock icons.

**NOTE:**: After pressing the lock/unlock icon, you must change the pan or tilt
value once for the lock to be activated.

![image](../media/pan_tilt_rot.png)

{{% include-html Target.md %}}

{{% include-html Subfixtures.md %}}

{{% include-html Navigation.md %}}

