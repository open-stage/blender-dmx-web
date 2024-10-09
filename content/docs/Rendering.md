---
title: "Rendering"
date: 2024-04-07T10:56:42+0200
category: "Help"
---

### Beam

BlenderDMX Addon is generating two styles of light output. The lense is rendered as an emitter material and the beam is rendered as a spot light.

The default 3D view viewport shading in Blender is Solid, you cannot see neither the emmiter nor the beam:

![Beam](../media/beam001.png)

In order to see the lense (emitter), you need to enable Material Preview:

![Beam](../media/beam002.png)

You can also see a "fake" beam cone by enabling the "Volume preview", but that
is not a real beam. This allows to be set on None, only Selected fixture or on
All fixtures.

![Beam](../media/beam003.png)

To see the full volumetric beam, you need to use Rendered output and also enable the Volume box:

![Beam](../media/beam004.png)

### Volumetric Beams

To enable the Volumetric beams:

* Click Update Volume Box
* Check Disable Overlays
* Check Enable Volume Scatter
* Set Density to for example 0.1

![Volume](../media/volume.png)

#### Eevee

##### Tweak Volumetrics in Eevee

This is in right side panel, under Render - Volumes:

* Set start/end to smaller values. This depends on camera, so you need to experiment. 
* Resolution
* Steps
* Distribution

#### Cycles

In Cycles, beam is rendered as starting from the beam lens, with the width of
the lens diameter. This can make gobo projection slightly blurry. See [details
here](../setup/#beam-lens-diameter-in-cycles).

![image](../media/beams.png)

### Lasers

Implementation of lasers in BlenderDMX Addon does not use Blender lights for the
laser rays but rather emitter material on a long, thin cylinder, projected from
the laser's geometry onto objects which are in a `Laser collision collection`
that must be created and then selected by the user. See [Laser article](../laser)
for more details.



