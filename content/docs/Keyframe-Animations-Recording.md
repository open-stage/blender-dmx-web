---
title: "Keyframe recording"
date: 2025-11-15T11:15:00+0100
category: "Help"
---
<style>
.dmx-table table {
  border-collapse: collapse;
  width: 100%;
}

.dmx-table th, .dmx-table td {
  border: 1px solid #000;
  padding: 6px 8px;
}

.dmx-table td:nth-child(2),
.dmx-table th:nth-child(2) {
  text-align: center;
}
</style>

BlenderDMX Addon allows recording keyframes from external DMX like [ArtNet](../artnet) or [sACN](../sacn) and also from the included [Programmer](../programmer).

### Keyframe Recorder

![image](../media/keyframe_recorder.png)

- Add Keyframe allows to manually insert keyframes related to the fixture attributes, like intensity, color, gobo, beam...
- Auto Keying turns on Blender internal auto-keying + changes to fixtures attributes (intensity, colors, gobo, beam...) are also recorded.
- Keyframe only selected fixtures (not for autokeying) allows to record keyframes only for selected fixtures.

### Recording DMX

To record external DMX, turn on Auto Keying, start DMX source and set the animation to the Play Animation state :play_or_pause_button: 

### Delete keyframes

- Delete from selected fixtures
- Delete from all fixtures

These buttons allow to quickly delete all keyframes from selected/all fixtures.

### Recorded data

Recorded data can be seen in the timeline, make sure to uncheck `Only Show
Selected`.  The `Only Show Selected` is only affecting visibility of the data,
keyframing of selected/unselected (fixtures) is controlled by the BlenderDMX
[Keyframing settings](#keyframe-recorder).

![image](../media/keyframe_list.png)

The keyframed data no longer have any DMX information in them and thus cannot
be converted back to DMX. For example: when you set (via DMX) intensity and
color on RGB/CMY and/or on color wheel, and/or on CTO, Blender will typically
record this as a keyframe with one info (rgb color) and there's no way to
deconstruct it back to what was RGB, what was color wheel and what was dimmer.

### Recording \#bdmx driver

Object with \#bdmx driver can be recorded to keyframes, but in order to play
the animation, the \#bdmx driver must be removed or disabled. As disabling it
does not seem to be possible in Blender, BlenderDMX Addon adds extra options to
the Keyframe recording panel.

This allows object with the driver to be either Recorded or Played back:

![image](../media/keyframe_driver_options.png)

### Controlling Blender controls via DMX

When recording DMX, it is useful to be able to remotely control Blender's
Auto-keying and also the animation/timeline play state. There is a special
BlenderControl fixture included in the BlenderDMX addon and [available in GDTF
Share](https://gdtf-share.com/userPage.php?name=BlenderDMX&page=Revisions&fixtureId=33474).
To control Blender's controls, patch the BlenderControl fixture into BlenderDMX
and into your DMX console. See [DMX chart of the
BlenderControl](/assets/BlenderControl_DMX_Chart.pdf).

![image](../media/blender_control.png)

#### Playmode allows to set the state of the animation player:

<div class="dmx-table">

| Function        |   DMX    |
|-----------------|:--------:|
| No Function     |    0     |
| Pause           |  50 - 99   |
| Rewind and Play | 100 - 149  |
| Play <<         | 150 - 199  |
| Play >>         | 200 - 255  |

</div>

#### Recording allows to enable/disable the auto-keying:

<div class="dmx-table">

| Function           | DMX       |
| -------------      | :-------: |
| No Function        | 0         |
| Recording Disabled | 1 - 128   |
| Recording Enabled  | 129 - 255 |

</div>

#### World background color

The RGB and Dimmer allow to set (and also to be keyframed) the Worlds background.

<div class="dmx-table">

| Function           | DMX     |
| -------------      | :-----: |
| No Function        | 0       |
| Color, Dimmer      | 1 - 255 |

</div>

#### Notes:

BlenderDMX Addon provides a UI to set Background color in
[Setup](/docs/setup/#viewport). Blender itself also provides UI in the World
panel. When changing background via DMX or via [Programmer](/docs/programmer/),
the changes are synchronized to the UI, but when changing the background via
any of the UI, changes are not synchronized to the DMX/Programmer.

The BlenderControl DMX channels have No Function at DMX 0, to allow to not
affect Blender from DMX/Programmer at all.


