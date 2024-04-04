---
title: "Lasers"
date: 2024-04-04T09:55:28+0200
category: "Help"
---

BlenderDMX allows to visualize laser devices. The laser fixture definition is
based on GDTF, as for all other fixtures. By creating a custom GDTF, there
is a lot of flexibility of the types of lasers... single beam, multiple beams,
zooming, color changing, different shapes and so on.

The following laser specific GDTF properties are currently utilized for lasers:

- number of laser geometries
- position and rotation of laser geometries
- laser diameter

Other GDTF properties like pan, tilt, zoom, color, dimmer... are also used.

Examples:

![image](../media/laser.png)

![image](../media/laser_bloom.png)

Implementation in BlenderDMX is based on [this YouTube
video](https://www.youtube.com/watch?v=akacnNMPK8M) and it does not use beams
for the laser rays but rather emitter material on a cylinder, projected from
the laser base onto objects which are in a "Laser collision collection", which
must be created and then selected by the user.

# Setup

## Add laser

Add a Laser fixture by using the Add Fixture menu. BlenderDMX comes with a default
Laser included. It is useful to uncheck "Add Target":

![image](../media/01_add_laser.png)

## Add objects

Add another object or objects, for example a plane:

![image](../media/02_add_plane.png)

## Add objects to a collision collection

- select object(s) which should be affected by the laser
- press m
- Create New Collection and confirm, call it for example "lasers"

![image](../media/02_create_collection.png)

![image](../media/03_add_collection.png)

## Set collision collection on lasers

Go to Setup - Beam Volume and for Laser collision collection select this collection "lasers"

![image](../media/03_select_collection.png)

## Turn laser on

In Fixtures list, select the laser, set Color, Dimmer, Pan, Tilt... also, set Viewport to Shading.

![image](../media/04_turn_on_laser.png)

## Extra

You can make lasers look better by turning on Bloom in Eevee:

![image](../media/05_enable_bloom.png)

If you select a color where for example red and blue is used, you can make the
bloom being in different color then is the laser, for more interesting effect.

![image](../media/laser_bloom.png)

