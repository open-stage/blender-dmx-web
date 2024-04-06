---
title: "Rendering"
date: 2024-02-15T22:01:55+0100
category: "Help"
---

### Beam

BlenderDMX is generating two styles of light output. The lense is rendered as an emitter material and the beam is rendered as a spot light.

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

### Tweak Volumetrics in Eevee

(This is in right side panel, under Render)

* Set start/end to smaller values. This depends on camera, so you need to experiment. 
    * Start: 1m
    * End: 20m
* Tile size: 2px
* Samples: 128
* Distribution: 0.1

- **Start/end:** smaller values will make it more performant
- **Tile size:** nice rendering but more compute demanding
- **Samples:** bigger number makes it better but much more compute demanding

#### Eevee

To prevent flicker, make sure that Play Animation is in the Play state:

![image](https://github.com/open-stage/blender-dmx/assets/3680926/c507c26d-cc63-4662-a45b-bc96ddf865bf)

#### Cycles

In Cycles, beam is rendered as starting from the beam lens, with the width of the lens diameter. This can make gobo projection slightly blurry. See [details here](../setup/#beam-lens-diameter-in-cycles).

![image](../media/beams.png)

### Lasers

Implementation of lasers in BlenderDMX does not use Blender lights for the
laser rays but rather emitter material on a long, thin cylinder, projected from
the laser's geometry onto objects which are in a `Laser collision collection`
that must be created and then selected by the user. See [Laser article](../laser)
for more details.



