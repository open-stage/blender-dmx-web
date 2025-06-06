---
title: "Open Sound Control"
date: 2024-04-07T10:56:53+0200
category: "Help"
---
OpenSoundControl (OSC) is a communication protocol which can allow to send information from BlenderDMX Addon out to other software.

It is used to send fixture selection to other software, like DMX consoles and the current definition ([which can be customized](#defining-osc-commands)) is allowing for nice integration with the [BlinderKitten](http://blinderkitten.lighting/) lighting software.

Two events are hooked into OSC right now:

- fixture selection
- fixture clear


## Fixture selection

`fixture_selection`

Due to limitations of how object selection works (and is understood) in BlenderDMX Addon, fixture selection works only when a fixture is selected in the Fixtures panel or via the Programmer Selection icons.


## Clear fixture selection

`fixture_clear`

The Clear selection icon triggers the fixture clean selection

![image](../media/osc.png)


## Defining OSC commands

The `assets/osc_templates` directory contains a `default.json` file, the commands (`fixture_selection`, `fixture_clear`) can have a list of keys and values which are sent via OSC. The `fixture_selection` command takes a parameter `fixture`, from which various attributes can be used, in the selection case it is a `fixture_id`.

```json
{
  "fixture_selection": [
    {
      "key": "/key/fixture",
      "value": ""
    },
    {
      "key": "/key/{fixture.fixture_id}",
      "value": ""
    }
  ],
  "fixture_clear": [
    {
      "key": "/key/clear",
      "value": ""
    }
  ]
}
```

All OSC handlers are located in file `osc_utils.py`, where the static methods of the `DMX_OSC_Handlers` class define the usage.

