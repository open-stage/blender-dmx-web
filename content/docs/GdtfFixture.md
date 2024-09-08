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
- PanRotation
- TiltRotation
- Shutter1 (used for Strobing in BlenderDMX)
- ColorAdd_R, G, B
- ColorRGB_Red, Green, Blue
- ColorSub_C, M, Y
- ColorAdd_C, M, Y
- ColorAdd_W, WW, CW (white, warmwhite, cold white)
- ColorAdd_RY, GY, UV (amber, lime, uv)
- CTC, CTO, CTB (color temperature control)
- Iris
- Color1, Color2
- ColorMacro1
- Zoom
- Gobo1, Gobo2
- Gobo1Pos, Gobo2Pos
- XYZ_X, Y, Z
- Rot_X, Y, Z

> ChannelFunctions and Physical Values are not implemented at the moment.

Read this section about usage and Implementation [details of GDTF Attributes in
BlenderDMX](/docs/fixture/#gdtf-attributes-usage-in-blenderdmx).

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

![image](../media/mvr_exchange.png)


## GDTF Share Integration in Blender

GDTF files can be downloaded directly from Blender:

* Register a free account on [GDTF Share](https://gdtf-share.com/) 
* Fill in username and password into Blender-DMX addon preferences

![Preferences](../media/preferences00.png)

![image](../media/gdtf_share_credentials.png)


![GDTF Share integration](../media/gdtf_integration.png)

## After MVR import, GDTF fixtures have IDs and DMX but their bodies are not visible in 3D

This depends on how you are doing the MVR export in Vectoworks, gMA3, Capture
or other software. For example Capture never provides any useful GDTFs, only
place-holders. Vectorworks provides useful GDTFs if you previously load them to
VW and link them to each VW symbol. To fix this issue, you can use the Edit
fixture function of BlenderDMX: after the MVR import to BlenderDMX, edit all
fixtures → uncheck the Re-address only and choose GDTF files for each fixture.


## Why do fixtures from GDTF have different features, like Gobo or Color and some not?

GDTF is a format to describe real world devices, meaning that there are real
lights out there which someone physically built and uses on real stages. Some
of them are simple with just a lamp, some have colors, others may have gobos
and pan/tilt and so on. If you don't care about this, you can choose any
fixture. See also the next question.


## Is there a difference between Spot and Wash fixtures in BlenderDMX?

Yes. BlenderDMX supports Spot, Wash, Beam, Linear Strips, MultiPixel, Front
Facing and other devices, including Lasers. Spots have a hard beam edge, and if
they contain gobos, their projection is supported. Washes have a smooth blend
on the beam. Narrow parallel beam angles aligned with the front beam lens (beam
fixtures) are also supported. Pixel devices can be pixel controlled and any
device can be set to not contain volumetric beam to only provide front facing
color mixing or strobing.
