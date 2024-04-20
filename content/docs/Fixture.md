---
title: "Fixtures"
date: 2024-04-07T10:57:47+0200
category: "Help"
---

Fixture profiles come from GDTF, [read details here](../gdtffixture).

# Fixture

Fixture represents a GDTF device. This can be a static/moving lighting fixture but also a truss or any other 3D object in a GDTF file.

Listing mode:

![image](https://github.com/open-stage/blender-dmx/assets/3680926/d582d474-a5f6-4cac-9541-87eb5ff2898b)

Edit mode:

![image](https://github.com/open-stage/blender-dmx/assets/3680926/8885b964-1dd3-4c21-a5e7-7e397eff1026)

The `Fixture Panel` selection is synced to the Viewport.

If you delete a fixture on the Viewport, it is deleted from the DMX show and [Groups](../groups) as
well.

## Fixture menu

The fixture menu allows to Add/Edit/Delete a fixture. GDTF files can also be imported here. Full scene can be imported with the `Import MVR Scene`, you can read more about [MVR here](../gdtffixture/#mvr).

![image](../media/fixture_menu.png)



## Add Fixture

![image](../media/add_fixture.png)

- **Name:** Name of the Fixture.
- **GDTF Profile:** Select the GDTF Profile from the BlenderDMX library.
- **DMX Mode:** Select the DMX Mode of the selected GDTF Profile.
- **Universe:** DMX Universe of the Fixture.
- **Address:** DMX Address of the Fixture.
- **Fixture ID:** The fixture ID of the first fixture.
- **Units:** How many fixtures should be created.
- **Increment DMX address:** Whether to increase DMX address when adding multiple devices
- **Increment Fixture ID:** Whether to increase Fixture ID when adding multiple devices
- **Fixture ID:** An ID of the fixture. Currently this is not used in BlenderDMX. It can be a number or text
- **Display beams:** Eevee has limit of 120 beam per scene, so sometimes it is useful to create front facing devices only with the Emitter lens but without a beam
- **Add Target:** When adding for example XYZ_X,Y,Z fixtures, the target is not needed. Also, sometimes the Target is not useful. This allows not to add it.
- **Gel Color:** A subtractive color filter applied to the lamp color. Useful
  for mimicking white balance on lamps.

## Edit Fixture

If `Re-address only` is checked, the GDTF Profile, DMX Mode and Gel Color are not editable, this speeds up the editing as the GDTF profile does not need to be re-evaluated. This option also allows to assign and remove an IES photometric file to the selected fixtures.

![Edit Single Fixture](../media/edit_readress_only.png)

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

When unselecting **Re-address only**:

- **Name:** If you keep the `*`, it keeps fixture names. Otherwise, it appends
  an integer index to the end of the given name for each fixture being edited.
- **GDTF Profile:** If you don't select anything, features remain the same.
  Otherwise, it replaces every selected fixture with the selected profile.
- **DMX Mode:** Same as GDTF Profile.
- **Universe:** Same as GDTF Profile.
- **Address:** The addresses are set starting at the first selected Fixture,
  and growing according to the fixture footprints.
- **Gel Color:** Same as GDTF Profile.


## Remove fixture

You can select fixture(s) and remove them by using the Remove Fixture menu item. There can be situations when the fixture is not possible to select. It can be removed by making the fixture list Editable and then clicking the cross icon:

![image](../media/remove_fixture.png)

## Import IES File/Remove IES File

This allows for more photo-realistic volumetric beam rendering. Example of beams without (left) and with (right) IES:

![image](../media/ies.png)

## GDTF Attributes usage in BlenderDMX

See sections below for details on how are some GDTF attributes applied in
BlenderDMX.

## Colors

### Color Mixing

All supported color mixing attributes (ColorAdd_R, G, B; ColorRGB_Red, Green,
Blue; ColorSub_C, M, Y; ColorAdd_C, M, Y) are linked to the color picker. CMY
is converted to RGB. By default, the color picker is set to white.

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

### Gobo Selection

Gobo1 and Gobo2 are supported. Only one gobo is projected at one moment (no
gobo morphing or two gobos animation). All images from `media` folder are
utilized, so if for example animation wheel image is in there, it is possible
to select it.

### Gobo Rotation

Gobo1Pos and Gobo2Pos are supported. This is done by adding a Blender driver
(`frame * selected value`) to the image Euler rotation. Blender animation
player must be playing.


### Gobo visualization

Eevee has to be used at least once with gobos, for gobos to render in Cycles.
Simply switch the renderer to Eevee and back to Cycles and gobos will show up.
This seems as either some combination of things or a bug in Blender.

In order to see gobo rotation and better gobo projection (Eevee), the animation
player must be in the "Play animation" state. This seems to be a Blender thing
and it means that you cannot do a rendered output of gobo in Eevee. Cycles must
be used for that.

![image](https://github.com/open-stage/blender-dmx/assets/3680926/c507c26d-cc63-4662-a45b-bc96ddf865bf)

In Cycles, beam is rendered as starting from the beam lens, with the width of
the lens diameter. This can make gobo projection slightly blurry. See [details
here](../setup/#beam-lens-diameter-in-cycles). Note: this seems to also depend
on graphics card driver/operating system and so on.

![image](../media/beams.png)

## Strobe

Strobing is supported if the fixture has Shutter1 attribute. Strobe is
currently not keyframeable.

{{% include-html Target.md %}}

{{% include-html Navigation.md %}}

