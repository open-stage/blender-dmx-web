---
title: "BlenderDMX Addon 1.9.1 Released"
date: 2025-01-18T18:50:06+0100
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.9.1
---
## MVR-xchange - Internet-Based Implementation re-writen to pure websockets

Our [last release](/blog/release-1.9.0/) added support for the non-local
version of MVR-xchange. For that, not only was the MVR-xchange implemented into
the BlenderDMX Addon, but a coordinating server had to be written from scratch.
The plan was to re-write the server, to clean up the code and make it more
efficient and only during the re-write I have discovered that the
implementation, based on the socket.io foundations is not the same as if done
in pure websockets. This release (1.9.1) is thus a re-write to websockets.
There is not difference on the user facing side, except that the address to the
MVR-xchange server must start with a websockets scheme wss, rather then https.

For more details about the MVR-xchange Internet version and about the testing
server, read the [blog post for v1.9.0](/blog/release-1.9.0/).

{{< uuid >}}

Report your findings in the [BlenderDMX Discord](https://discord.gg/FQVVyc45T9).

## Changelog

See the changelong for more information, or developers can look at [git
log](https://github.com/open-stage/blender-dmx/commits/main/) for full details.
