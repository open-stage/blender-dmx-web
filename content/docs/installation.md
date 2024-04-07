---
title: "Installation"
date: 2024-04-07T10:55:50+0200
category: "Help"
---

Make sure you have installed [Blender](https://www.blender.org/download/) 3.4 or higher. Version 4.x is supported but do note that when importing MVR files, Blender 4.x can be 10x slower then Blender 3.x .


### BlenderDMX installation
<ol>
   <li id="version"> Download the zip file from the <a href="https://github.com/open-stage/blender-dmx/releases/latest">latest release</a> page.
   <li> Open Blender
   <li> Edit → Preferences → Add-ons → Install
   <li> Select the downloaded zip file
   <li> To enable the addon, go to Edit → Preferences → Add-ons, search for "DMX" and toggle the checkbox on.
</ol>

You can continue to the <a href="../get_started" ><i class="fa-solid fa-truck-fast"></i> Getting Started Guide</a> or to the <a href="../setup" ><i class="fa-solid fa-circle-play"></i> User Guide</a>.

![Install](../media/install.gif)


<script type="module">
    let team = $("#version");
    $.get("https://api.github.com/repos/open-stage/blender-dmx/releases/latest", (data) => {
            team.html(
              `From the <a href="https://github.com/open-stage/blender-dmx/releases/latest">latest release</a> page, download the <a href="${data.assets[0].browser_download_url}">${data.assets[0].name}</a>
              `);

    });
</script>

