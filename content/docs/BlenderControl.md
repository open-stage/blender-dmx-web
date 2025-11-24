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


