---
title: "Fixtures"
date: 2024-02-15T22:01:55+0100
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

The fixture menu allows to Add/Edit/Delete a fixture. GDTF files can also be imported here. Full scene can be imported with the `Import MVR Scene`, you can read more about [MVR here](GdtfFixture#mvr).

![image](https://github.com/open-stage/blender-dmx/assets/3680926/e48ae529-640a-432d-856d-947e7eb50339)



## Add Fixture

![image](https://github.com/open-stage/blender-dmx/assets/3680926/6593f146-b99b-4ec1-b62d-4879ba34a962)

- **Name:** Name of the Fixture. Should be unique on the show.
- **GDTF Profile:** Select the GDTF Profile from the BlenderDMX library.
- **DMX Mode:** Select the DMX Mode of the selected GDTF Profile.
- **Universe:** DMX Universe of the Fixture. It should exist on the `DMX >
  Universes Panel` in order for DMX to work properly.
- **Address:** DMX Address of the Fixture.
- **Gel Color:** A subtractive color filter applied to the lamp color. Useful
  for mimicking white balance on lamps.
- **Units:** How many fixtures should be created.
- **Fixture ID:** An ID of the fixture. Currently this is not used in BlenderDMX. It can be a number or text
- **Display beams:** Eevee has limit of 120 beam per scene, so sometimes it is useful to create front facing devices only with the Emitter lens but without a beam
- **Add Target:** When adding for example XYZ_X,Y,Z fixtures, the target is not needed. Also, sometimes the Target is not useful. This allows not to add it.

## Edit Fixture

When editing, if a single Fixture is selected, the Edit Menu works exactly like
the Add Menu, without the `Units` parameters. As the editing can take a lot of time
(the full GDTF needs to be re-evaluating) if choose `Re-address only`, only the Fixture ID, Universe and Address will be changed.

![Edit Single Fixture](../media/blenderdmx-beta-fixture3.png)

If multiple fixtures are selected, there are a few differences:

![Edit Multiple Fixtures](../media/blenderdmx-beta-fixture4.png)

- **Universe:** Set DMX Universe
- **Address:** The addresses are set starting at the first selected Fixture
- **Fixture ID:** The fixture ID starting at the first selected Fixture
- **Re-address only** Allows for fast DMX address/universe, fixture id... settings
- **Import IES File** Allows to Import IES File and links it to selected fixtures's beams
- **Remove IES File** Removes IES File from selected fixtures
- **Increment DMX address:** Whether to increase DMX address when editing multiple devices
- **Increment Fixture ID:** Whether to increase Fixture ID when editing multiple devices

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


## Import IES File/Remove IES File

![image](../media/ies.png)

## Navigation between fixtures

You can use `Ctrl-Left` / `Ctrl-Right` to go between fixtures (Previous/Next).

## Selecting multiple fixtures in the Fixtures List

You can use `Shift` to select multiple fixtures. You can also use these selection icons in the programmer to:

![Edit Multiple Fixture](../media/selection.png)

- Select All
- Invert Selection
- Select Every Other Light
- Select Visible Lights Only (only filtered)
- Deselect All
