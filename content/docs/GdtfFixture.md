---
title: "GDTF & MVR"
date: 2024-04-07T10:57:39+0200
category: "Help"
---

GDTF and MVR are open standards for the entertainment industry, 
main site [GDTF Share](https://gdtf-share.com), documentation and projects on [GDTF.eu](https://gdtf.eu).

# GDTF
GDTF: The General Device Type Format is an open standard for describing 
devices of the entertainment industry. 

These devices may be lighting fixtures, trusses, distribution boxes, 
media servers, lasers or other devices used in the entertainment industry.

A GDTF Profile includes 3D Models, information about Geometry, DMX channels, 
Color Wheels and a lot of other properties a Lighting Fixture might have.

## Download and Build Profiles

The [GDTF Share](https://gdtf-share.com/) contains profiles from multiple
brands, as well as profiles built by the community. GDTF Share is 
fully [integrated](#gdtf-share-integration-in-blender) into Blender-DMX, allowing 
downloading GDTF profiles directly from Blender-DMX.

There's also a [GDTF Builder](https://fixturebuilder.gdtf-share.com/) available
for creating and editing GDTF Profiles.

## Supported GDTF features in BlenderDMX

BlenderDMX utilizes GDTF files to be able to visualize a device. GDTF files from GDTF Share can be downloaded directly from BlenderDMX. Following GDTF properties are utilized:

- A dynamic fixture object from a GDTF profile, either from
  primitives or custom models from 3DS and GLB mesh files
- GeometryReferences
- BeamGeometry and it's attributes (Lamp Power, Beam Angle, Beam Type)
- LaserGeometry and it's Beam Diameter attribute
- CameraGeometry (and selecting a view through the camera)
- Pigtail geometry (identifying typically back of the fixture)
- 2D SVG symbol
- media images (gobo) from wheels folder
- [Supported GDTF Attributes](#supported-gdtf-attributes)
- [GDTF Share integration](#gdtf-share-integration-in-blender)
- more features as per [pygdtf](https://github.com/open-stage/python-gdtf) library

## Supported GDTF Attributes

Features or properties of GDTF devices, controlled by DMX channels:

- Dimmer (8/16bit)
- Pan (8/16 bit)
- Tilt (8/16bit)
- Shutter (Strobe)
- ColorAdd_R, G, B
- ColorRGB_Red, Green, Blue
- ColorSub_C, M, Y
- Color1, Color2
- ColorMacro1
- Zoom
- Gobo1, Gobo2
- Gobo1Pos, Gobo2Pos
- XYZ_X, Y, Z
- Rot_X, Y, Z

> ChannelFunctions and Physical Values are not implemented at the moment.

> In order to see gobo rotation and better gobo projection, the animation player must be in the "Play animation" state:

![image](https://github.com/open-stage/blender-dmx/assets/3680926/c507c26d-cc63-4662-a45b-bc96ddf865bf)


# MVR

> Do note that when importing MVR files, Blender 4.x can be 10x slower then Blender 3.x .

MVR: The My Virtual Rig file format is an open standard which allows 
programs to share data and geometry of a scene for the entertainment industry.

A scene is a set of parametric objects such as fixtures, trusses, video 
screens, and other objects that are used in the entertainment industry.

## Supported MVR features

- Fixtures (with Address, Focus Points, Fixture Color, Fixture ID...)
- Scene Objects (with Symbols and Symdef...)
- Trusses
- Layers
- Group Objects
- more features as per [pymvr](https://github.com/open-stage/python-mvr) library
- [MVR-xchange Protocol](#mvr-xchange-protocol)

## MVR-xchange Protocol

![image](https://github.com/open-stage/blender-dmx/assets/3680926/135bfaef-8319-470c-86e0-210c068a1e61)


## GDTF Share Integration in Blender

GDTF files can be downloaded directly from Blender:

* Register a free account on [GDTF Share](https://gdtf-share.com/) 
* Fill in username and password into Blender-DMX addon preferences

![Preferences](../media/preferences00.png)

![image](https://github.com/open-stage/blender-dmx/assets/3680926/3da377dd-7b55-4b82-9432-eec19abaecca)


![GDTF Share integration](../media/gdtf_integration.png)

