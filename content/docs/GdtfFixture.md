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

The [GDTF Share](https://gdtf-share.com/) is the central distribution platform
for GDTF files. GDTF Share is fully
[integrated](#gdtf-share-integration-in-blender) into Blender-DMX, allowing
downloading and import of GDTF profiles directly from BlenderDMX Addon.

The [GDTF Builder](https://fixturebuilder.gdtf-share.com/) allows creating and
editing GDTF Profiles.

## Supported GDTF features in BlenderDMX Addon

BlenderDMX Addon utilizes GDTF files to be able to visualize a device. Local GDTF files can be [imported](/docs/fixture/#importing-gdtf-files) into BlenderDMX Addon, or files from the GDTF Share can be [downloaded directly](#gdtf-share-integration-in-blender) from BlenderDMX Addon. Following GDTF properties are utilized:

- A dynamic fixture object from a GDTF profile, either from primitives or
  custom models from 3DS and GLB mesh files
- GeometryReferences (thus correct DMX footprint and kinematic chain)
- DMX Breaks (each DMX Break can be patched to it's own address)
- BeamGeometry and its attributes (Lamp Power, Beam Angle, Beam Type) by using
  SpotLight
- BeamGeometry and its attributes as PointLight if the Beam Angle is set to
  360° or if Beam Angle is > 180° and the device does not have a Zoom
  attribute.
- LaserGeometry and it's Beam Diameter attribute
- CameraGeometry (and selecting a view through the camera)
- Pigtail geometry (identifying typically back of the fixture)
- 2D SVG symbol
- media images (gobo) on each Gobo Wheel
- [Supported GDTF Attributes](#supported-gdtf-attributes)
- [GDTF Share integration](#gdtf-share-integration-in-blender)
- more features as per [pygdtf](https://github.com/open-stage/python-gdtf)
  library

## Supported GDTF Attributes

Features or properties of GDTF devices, controlled by DMX channels:

- Dimmer (8/16bit)
- Pan (8/16 bit)
- Tilt (8/16bit)
- PanRotation
- TiltRotation
- PanMode
- TiltMode
- PanTiltMode
- Shutter1
- Shutter1Strobe
- ColorAdd_R, G, B
- ColorRGB_Red, Green, Blue
- ColorSub_C, M, Y
- ColorAdd_C, M, Y
- ColorAdd_W, WW, CW (White, Warm White, Cold White)
- ColorAdd_RY, GY, UV (Amber, Lime, UV)
- CTC, CTO, CTB (Color Temperature Control)
- Iris
- Color1, Color2, Color3
- ColorMacro1
- Zoom
- Gobo1, Gobo2
- Gobo1Pos, Gobo2Pos
- Gobo1PosRotate, Gobo2PosRotate
- XYZ_X, Y, Z
- Rot_X, Y, Z


# Physical Properties

## The following currently supported GDTF Attributes now utilize physical measurements from both Channel Functions and Channel Sets:

* Pan, Tilt, PanRotate, TiltRotate
* Zoom, Iris
* CTC, CTB, CTO
* Shutter1, Dimmer, ShutterStrobe
* Color1, Color2, Color3, ColorMacro1
* Gobo1, Gobo1Pos, Gobo1PosRotate
* Gobo2, Gobo2Pos, Gobo2PosRotate

### Current limitations:

* Acceleration and time for the movement is not utilized yet (so for example
  Pan or Tilt can move unrealistically fast).
* Strobing should be improved for short "flashes", rather then "blinks".
* Combining multiple colors on a single device needs to be improved (for
  example using RGB and CTO at the same time).

### Enhancements thanks to using physical properties:

* Selecting colors on ColorWheels or gobos on GoboWheels uses
correct Wheel Slots.
* Some behavior of the device can be conditionally affected by a value of
multiple channels (for example Gobo Indexing and Gobo Rotation, Pan and
PanRotation or Zoom ranges) and this is supported by utilizing the Mode
dependency (Mode Masters) feature of GDTF.

Read this section about usage and Implementation [details of GDTF Attributes in
BlenderDMX Addon](/docs/fixture/#gdtf-attributes-usage-in-blenderdmx-addon).

# MVR

MVR: The My Virtual Rig file format is an open standard which allows programs
to share data and geometry of a scene for the entertainment industry.

A scene is a set of parametric objects such as fixtures, trusses, video
screens, and other objects that are used in the entertainment industry.

## Supported MVR features

### Import

- Fixtures (with Address, Focus Points, Fixture Color, Fixture ID...)
- Scene Objects (with Symbols and Symdef...)
- Trusses
- Layers
- Classes
- Group Objects
- some more features as per [pymvr](https://github.com/open-stage/python-mvr)
  library
- [MVR-xchange Protocol](#mvr-xchange-protocol)

### Export

- Fixtures (with Address, Focus Points, Fixture Color, Fixture ID...) are
  exported onto a single layer

## MVR-xchange Protocol

![image](../media/mvr_xchange.png)

[MVR-xchange protocol](https://gdtf.eu/mvr/mvr-spec/xchange/) allows you to
exchange MVR files with other network applications that support MVR-xchange,
such as other instances of BlenderDMX or [Production
Assist](https://www.production-assist.com/).

### Internet version

Internet version of MVR-xchange requires a wss:// address of a coordinating
server. This address defines a group of stations coordinating together.

* **Sharing MVR Files**: Any station that wants to receive MVR files from you
  can connect to the same group address station. When you share a version,
  connected stations will be notified and can choose to fetch the MVR file from
  your station and apply it to their scene.

### Local version

Local version of the MVR-xchange uses only local network and local discovery
for the stations.

* **Group Cooperation**: Stations must cooperate within the same group. You can
  name the group as you prefer, but please use only basic Latin characters. The
  group name is determined by the station you are connecting to. When you
  establish a connection with another station, your group will automatically
  change to match the group name of the station you are connecting to.

* **Station Discovery**: Your BlenderDMX Addon station will automatically
  discover any stations in any groups and can connect to them. This enables you
  to receive MVR files from stations you connect to. When a connected-to
  station shares an MVR file, you will be notified and can fetch the file to
  apply it to your scene.

* **Sharing MVR Files**: Any station that wants to receive MVR files from you
  can connect to your station. When you share a version, connected stations
  will be notified and can choose to fetch the MVR file from your station and
  apply it to their scene.

## GDTF Share Integration in Blender

GDTF files can be downloaded directly from Blender:

- Register a free account on [GDTF Share](https://gdtf-share.com/)
- Fill in username and password into Blender-DMX addon preferences

![Preferences](../media/preferences00.png)

![image](../media/gdtf_share_details.png)

![image](../media/gdtf_share_credentials.png)

Update the GDTF Share index will refresh the list of available profiles. Each
profile can be downwloaded by clicking on the download icon:

![GDTF Share integration](../media/gdtf_integration.png)

# Common Questions and Answers:

## After MVR import, GDTF fixtures have IDs and DMX but their bodies are not visible in 3D

This depends on how you are doing the MVR export in Vectoworks, gMA3, Capture
or other software. For example Capture never provides any useful GDTFs, only
place-holders. Vectorworks provides useful GDTFs if you previously load them to
VW and link them to each VW symbol. To fix this issue, you can use the Edit
fixture function of BlenderDMX Addon: after the MVR import to BlenderDMX Addon, edit all
fixtures → uncheck the Re-address only and choose GDTF files for each fixture.

## Why do fixtures from GDTF have different features, like Gobo or Color and some not?

GDTF is a format to describe real world devices, meaning that there are real
lights out there which some manufacturer produces and which people use on real
stages. Some of them are simple with just a lamp, some have colors, others may
have gobos and pan/tilt and so on. If you don't care about this, you can choose
any fixture. See also the next question.

## Is there a difference between Spot and Wash fixtures in BlenderDMX Addon?

Yes. BlenderDMX Addon supports Spot, Wash, Beam, Linear Strips, MultiPixel, Front
Facing and other devices, including Lasers. Spots have a hard beam edge, and if
they contain gobos, their projection is supported. Washes have a smooth blend
on the beam. Narrow parallel beam angles aligned with the front beam lens (beam
fixtures) are also supported. Pixel devices can be pixel controlled and any
device can be set to not contain volumetric beam to only provide front facing
color mixing or strobing.
