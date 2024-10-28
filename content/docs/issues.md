---
title: "Issues and Solutions"
date: 2024-10-28T15:02:06+0100
---

Try to also look at [Frequently Asked Section (FAQ)](/docs/faq#faq-top).

### Issues

#### Seeing Blender error messages.

Best way to see errors is to open a terminal of your computer and start Blender
form the command line. Yo will then see all details and errors being printed
into the terminal. One can also see details and errors in the error logs (see
[Logging](#logging) below and in the [docs](../setup/#logging).

#### Direct editing of fixtures and their properties

Upon `Create New Show` BlenderDMX Addon creates a DMX collection in which the
BlenderDMX data is stored. Fixtures imported from GDTF reside here and these
have their own node trees for them. Manually editing or deleting data from the
DMX collection, in fixtures' geometries or node trees will likely cause the
addon to stop working. Generally, avoid such manual edits.

#### Edit Fixtures

If gobos are missing or parts of the fixtures got deleted, you can try to use
the Fixtures - Edit Fixtures menu. Most likely you need to use the Advanced
edit, which re-builds the fixtures form GDTF - make sure to have the GDTF files
still imported in BlenderDMX.

#### Remove fixtures

Sometimes fixtures are so damaged that they cannot even be removed via Fixtures
\- Remove menu. You should always be able to remove fixtures in the Fixtures
list. In the Fixtures, check the `Editable` checkbox, then press the X cross on
the fixture to remove it.

#### Language localization

When set to a local language, Blender actually also translates also property
names and so on. If you are constantly in one language this is typically OK,
but if you start a blend file in one language and then switch to another
language, property names are now not possible to be identified by the
BlenderDMX addon.

#### Logging

If BlenderDMX Addon is not working for you at all or you have issues, disable
all other custom enabled addons to check for collision. In BlenderDMX Addon,
set <a href="../setup/#logging">Logging</a> to Debug, this will produce more
information, saving it in the "blenderDMX.log" log file. Replicate the action
leading to the error, then look into the "blenderDMX.log" logfile if you see
anything obvious.

#### Missing gobos and textures

BlenderDMX Addon stores all user data in the Blender defined [user storage
location](https://docs.blender.org/manual/en/latest/advanced/extensions/addons.html#local-storage).
To find the directory, you can use the Setup - Logging - Show logging
directory. This can be an issue if you for example switch between computers.

To preserve the data, you can use the Project data Export/Import function:

- Use `Setup - Export - Export Project data` to save the data to a zip file
- [Download and install](/docs/installation) the addon
- Use `Setup - Import - Import Project data` to load the data from the previously exported zip file

Re-editing fixtures as per above can often help.

### Art-Net

When having issues receiving Art-Net, especially when the sender and BlenderDMX
are on the same computer. You must have at least one Universe set to Art-Net,
to be able to enable it. When enabling Art-Net, ideally, do not change the IP
address settings and leave it at the default 0.0.0.0 . When using an Art-Net
source on the same computer, you have to make sure to start and enable Art-Net
<b>first</b> in the BlenderDMX Addon. If running two pieces of Art-Net based
software on one computer is not working for you, then save yourself the trouble
and the best is to use another computer for the sending.
