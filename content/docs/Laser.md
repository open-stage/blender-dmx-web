---
title: "Lasers"
date: 2024-04-07T10:57:11+0200
category: "Help"
---

BlenderDMX Addon allows to visualize laser devices. The laser fixture definition is
based on [GDTF](../gdtffixture). By creating a custom GDTF, there is a lot of
flexibility of the types of lasers: single beam, multiple beams, zooming, color
changing, different shapes and so on.

The following laser specific GDTF properties are currently utilized for lasers
in BlenderDMX Addon:

- number of laser geometries
- position and rotation of laser geometries
- laser diameter

Other GDTF properties like pan, tilt, zoom, color, dimmer are also used.

Examples:

![image](../media/laser.png)

![image](../media/laser_bloom.png)

Implementation in BlenderDMX Addon is based on [this YouTube
video](https://www.youtube.com/watch?v=akacnNMPK8M). This principle does not
use Blender lights for the laser rays but rather emitter material on a long
thin cylinder, projected from the laser's geometry onto objects which are in a
`Laser collision collection` that must be created and then selected by the
user.

# Setup

## Add laser

Add a Laser fixture by using the `Add Fixture` menu. BlenderDMX Addon comes with a default
Laser included. It is useful to uncheck `Add Target`:

![image](../media/01_add_laser.png)

## Add objects

For the laser beams to appear, add another object or objects, for example a
plane, move it a bit down, so it is below the laser:

![image](../media/02_add_plane.png)

## Add objects to a collision collection

- select this newly added plane and any other object(s) which should be affected by the laser:
- press `m`
- select `Create New Collection`, call it for example `lasers`

![image](../media/02_create_collection.png)

![image](../media/03_add_collection.png)

## Set collision collection on lasers

Go to `Setup` - `Beam Volume` and for `Laser collision collection` select the
collection `lasers`

![image](../media/03_select_collection.png)

## Turn laser on

In Fixtures list, select the laser, set Color, Dimmer, Pan, Tilt... also, set Viewport to Shading. Success!

![image](../media/04_turn_on_laser.png)

## Extras

You can make lasers look better by turning on Bloom:

![image](../media/laser_bloom_only.png)

## Note on Laser collision collection

- You need to have at least one object or bounding box in the `Laser collision
  collection` for the laser beams to be created.
- You need to add any objects which should stop/interact with the laser beam to
  the `Laser collision collection`.
- You can use the `Volume Box` as the bounding box and add it to the Laser
  collision collection.
- After adding any new laser into the show, make sure to go to `Setup` - `Beam
  Volume` - `Laser collision collection` and  select the correct collection.
  This will add this collection as a collision parameter for all lasers in the
  show.
