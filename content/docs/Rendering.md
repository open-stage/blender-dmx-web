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

You can also see a "fake" beam cone by enabling the "Volume preview", but that is not a real beam:

> BlenderDMX now allows for the Volume preview cones to be displayed on None, only Selected fixture or on All fixtures.

![Beam](../media/beam003.png)

To see the full volumetric beam, you need to use Rendered output and also enable the Volume box:

![Beam](../media/beam004.png)


To prevent flicker, make sure that Play Animation is in the Play state:

![image](https://github.com/open-stage/blender-dmx/assets/3680926/c507c26d-cc63-4662-a45b-bc96ddf865bf)


### Beams

To enable the volumetric beams:

* Click Update Volume Box
* Check Disable Overlays
* Check Enable Volume Scatter
* Set Density to for example 0.1

![Volume](../media/volume.png)

### Tweak Volumetrics

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

![Volumetrics](../media/volumetrics.png)

You can always tweak these settings to your liking, also, check some [manuals and videos on the web](https://duckduckgo.com/?t=ffab&q=eevee+flicker) to see how you can make it look better.

## IES beams

With the [option to select any geometry](../setup#allow-selecting-geometries), one can add IES files to the beam Spot light objects, see [documentation here](https://docs.blender.org/manual/en/latest/render/shader_nodes/textures/ies.html) and some [tutorials on the web](https://duckduckgo.com/?t=ffab&q=blender+ies).

