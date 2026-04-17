---
title: "Programmer"
date: 2024-04-07T10:56:47+0200
category: "Help"
---

## Programmer

![image](../media/programmer.png)

## To use the programmer:

- fixtures must support the corresponding attributes, for example Dimmer or Pan/Tilt.
- when a single type of fixture(s) is selected, only controls supported by the fixture type are visible
- when subfixtures of one fixture type are selected, only controls supported by the subfixtures are visible
- fixtures must be assigned to a Universe called BlenderDMX:

![image](../media/protocols_blenderdmx.png)

![image](../media/fixtures_list.png)

## Programmer Icons

![image](../media/programmer_icons.png)

- Select all
- Invert Selection
- Select every other light
- Select visible (only filtered)
- Deselect all
- Targets to zero - set Targets placement to 0,0,0 of the Scene
- Reset Targets - Reset position of targets of selected fixtures. Allows to place the target at +/- X, Y, Z around the fixture.
- Lock Movement - ignore pan/tilt DMX data - useful if setting position via Target
- Unlock Movement - enable pan/tilt DMX data
- Center View to selected object
- Track Target - enable pan/tilt to be affected by the Target
- Do Not Track Target - ignore Target and prefer DMX data - useful if programming via DMX
- Use Fixture Physical Properties - Use Real World (physical) data as provided by the GDTF file
- Do Not Use Fixture Physical Properties - Use default [physical data provided by BlenderDMX](../fixture/#physical-data), do not use data provided by GDTF file

## Attributes

Following control attributes are available in the Programmer: Dimmer, Color,
Color Wheel, Color Temperature, Pan, Tilt, PanRotate, TiltRotate, Zoom, Iris,
Gobo 1 and 2, Gobo Indexing and Rotation, Shutter/Strobe. BlenderDMX Addon itself
supports [more GDTF attributes](../gdtffixture/#supported-gdtf-attributes).

{{% include-html Subfixtures.md %}}

{{% include-html Target.md %}}

{{% include-html Navigation.md %}}

