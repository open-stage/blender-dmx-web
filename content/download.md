---
title: Download
menu:
  main:
    weight: 1
---

<div class="uk-container">
    <div class="uk-grid uk-grid-match uk-child-width-1-2@m uk-text-small" uk-grid>
<div>
            <div class="uk-card uk-card-default">
                <div class="uk-card-body" id="extension">
              <h3 class="uk-card-title uk-margin-remove-bottom">Official Extension site for Blender 4.2 and newer</h3>
                    <p class="uk-margin-small">
                    To install BlenderDMX Addon, continue to the Blender Extension site and click the Get Add-on button.
                        <div class="uk-margin-medium-top">
                            <a href="https://extensions.blender.org/add-ons/open-stage-blender-dmx/" class="uk-button uk-button-large uk-button-secondary uk-width-expand uk-margin-small-bottom"><i class="fa-solid fa-download"></i>Download</a>
                        </div>
                    </p>
                </div>
            </div>
        </div>
        <div>
            <div class="uk-card uk-card-default">
                <div class="uk-card-body" id="latest_release">
              <h3 class="uk-card-title uk-margin-remove-bottom">Manual install for Blender 4.1 and older</h3>
                    <p class="uk-margin-small" id="latest_release">
                    Download old addon for Blender 4.1 and older.
                        <div class="uk-margin-medium-top">
                            <a href="https://github.com/open-stage/blender-dmx/releases/latest"> Go to release page</a>
                        </div>
                    </p>
                </div>
            </div>
        </div>    
        <div>
        </div>
    </div>
</div>

<script type="module">
    let team = $("#latest_release");
    $.get("https://api.github.com/repos/open-stage/blender-dmx/releases", (data) => {

        let total_downloads = data.reduce(function(total, item, index){
            return total + item.assets[0].download_count
        }, 0)

            team.html(
              `<h3 class="uk-card-title uk-margin-remove-bottom">Legacy add-on for Blender 4.1 and older</h3>
                    <p class="uk-margin-small" id="latest_release">
<h5 style="display:inline">Version:</h5> ${data[0].name}
</br>
<h5 style="display:inline">Name:</h5> ${data[0].body.split("\n")[0].replace("# ", "")}
</br>
<h5 style="display:inline">Released:</h5> ${new Date(data[0].assets[0].created_at).toDateString()}
</br>


Total releases: ${data.length}, Total downloads: ${total_downloads}, Latest release downloads: ${data[0].assets[0].download_count}
</br>
Zipped addon:                            <a href="${data[0].assets[0].browser_download_url}" >Download zip</a>
                    </p>
              `);

    });
</script>
