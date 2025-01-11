---
title: "BlenderDMX Addon 1.9.0 Released"
date: 2025-01-11T09:22:48+0100
category: "Releases"
author: vanous
link: https://github.com/open-stage/blender-dmx/releases/tag/v1.9.0
---
## MVR-xchange - Internet-Based Implementation

Working on a lighting project and sharing data with other designers can be
supercharged with the MVR-xchange protocol.

After [implementing the local version](/blog/release-1.8.3/) of the
[MVR-xchange protocol](https://gdtf.eu/mvr/mvr-spec/xchange/), which is
suitable for local networks, this release of the BlenderDMX Addon adds an
initial implementation of the internet-wide MVR-xchange. It allows cooperation
between parties in different locations. It requires a publicly accessible
coordination server, which is now available for testing purposes on
[BlenderDMX.eu](/).

### BlenderDMX Testing MVR-xchange Server

BlenderDMX.eu provides a test server for the MVR-xchange and will offer it for
a few weeks to test and confirm the MVR-xchange implementation in the
BlenderDMX Addon.

You should NOT share private data via the server. The data is not publicly
visible or available, but it is visible to the operators of the server. We will
not share the data, but we want to be sure that a random mistake will not
result in private data exposure.

### Privacy information disclosure of the MVR-xchange coordination server

We save the provided MVR file - it is a function of the server to receive the
MVR file and to distribute it in the same group to other clients who request
this file. We log IP addresses in order to prevent abuse of the system. We
clean the data (the MVR files and the logs) weekly.

### Privacy of the MVR-xchange groups on BlenderDMX server

Groups in MVR-xchange on BlenderDMX.eu are organized via subdomains, where each
domain is a very long string in the form of a UUID v4. There is no
authentication, as the randomness of the UUID guarantees
([discussion](https://security.stackexchange.com/questions/53458/is-it-safe-to-rely-on-uuids-for-privacy))
that the chances of someone randomly guessing a v4 UUID are infinitesimally
small. It's so tiny that it's not worth serious consideration, as it would take
about 103 trillion guesses if the UUID creation is truly random. The choice of
the group to be an UUID is our implementation choice, it could potentially be
any string, but UUIDs contribute to robustness of system.

You can get a random group to be filled into the BlenderDMX Addon settings here:

{{< uuid >}}

Report your finding in the [BlenderDMX Discord](https://discord.gg/FQVVyc45T9).

## List of changes

* MVR-xchange - initial websockets implementation
* Fix SVG import on some systems [Lily Hopkins]
* Translated using Weblate (Chinese (Simplified Han script))

## Changelog

See the changelong for more information, or developers can look at [git
log](https://github.com/open-stage/blender-dmx/commits/main/) for full details.
