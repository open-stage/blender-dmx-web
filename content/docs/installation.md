---
title: "Installation"
date: 2024-04-07T10:55:50+0200
---
This page is deprecated, go to [Download page](/download).

Make sure you have installed [Blender](https://www.blender.org/download/) 3.4
or higher, 4.2 and newer is recommended to have all features.

To preserve data during addon update, see the [Updating procedure](/docs/updating).

For Blender from version 3.4 to version 4.1, see the instructions below. For
Blender 4.2 Beta, use the [BlenderDMX
Extension](https://extensions.blender.org/add-ons/open-stage-blender-dmx/).

### BlenderDMX Addon installation

<ol>
   <li id="version"> Download the zip file from the <a href="/download">Download</a> page.
   <li> Open Blender
   <li> Edit → Preferences → Add-ons → Install
   <li> Select the downloaded zip file
   <li> To enable the addon, go to Edit → Preferences → Add-ons, search for "DMX" and toggle the checkbox on.
   <li> The addon is then placed in the Sidebar. The Sidebar can be displayed/hidden by pressing N or by clicking onto the small arrow on the side:
</ol>


![Sidebar hidden](../media/sidebar_hidden.png)
![Sidebar visible](../media/sidebar_visible.png)

You can continue to the <a href="../get_started" ><i class="fa-solid fa-truck-fast"></i> Getting Started Guide</a> or to the <a href="../setup" ><i class="fa-solid fa-circle-play"></i> User Guide</a>.

![Install](../media/install.gif)


<script type="module">
    let download = $("#version");
    $.get("https://api.github.com/repos/open-stage/blender-dmx/releases/latest", (data) => {
            download.html(
              `From the <a href="/download">Download</a> page, download the <a href="${data.assets[0].browser_download_url}">${data.assets[0].name}</a>
              `);

    });
</script>

