---
title: "Keyframe recording"
date: 2024-04-07T10:57:27+0200
category: "Help"
---

BlenderDMX Addon allows recording keyframes from external DMX like [ArtNet](../artnet) or [sACN](../sacn) and also from the included [Programmer](../programmer).

### Keyframe Recorder

![image](../media/keyframe_recorder.png)

- Add Keyframe allows to manually insert keyframes related to the fixture attributes, like intensity, color, gobo, beam...
- Auto Keying turns on Blender internal auto-keying + changes to fixtures attributes (intensity, colors, gobo, beam...) are also recorded.

To record external DMX, turn on Auto Keying, start DMX source and set the animation to the Play Animation state :play_or_pause_button: 

### Delete keyframes

- Delete from selected fixtures
- Delete from all fixtures

These buttons allow to quickly delete all keyframes from selected/all fixtures.

### Recorded data

Recorded data can be seen in the timeline, make sure to uncheck `Only Show Selected`.

![image](../media/keyframe_list.png)

The keyframed data no longer have any DMX information in them and they cannot be converted back to DMX.

### Recording \#bdmx driver

Object with \#bdmx driver can be recorded to keyframes, but in order to play
the animation, the \#bdmx driver must be removed or disabled. As disabling it
does not seem to be possible in Blender, BlenderDMX Addon adds extra options to
the Keyframe recording panel.

This allows object with the driver to be either Recorded or Played back:

![image](../media/keyframe_driver_options.png)

