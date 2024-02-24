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
                <div class="uk-card-body" id="latest_release">
              <h3 class="uk-card-title uk-margin-remove-bottom">Latest Release</h3>
                    <p class="uk-margin-small" id="latest_release">
                    Download BlenderDMX.
                        <div class="uk-margin-medium-top">
                            <a href="https://github.com/open-stage/blender-dmx/releases/latest" class="uk-button uk-button-large uk-button-primary uk-width-expand uk-margin-small-bottom"><i class="fa-solid fa-download"></i> Go to release page</a>
                        </div>
                    </p>
                </div>
            </div>
        </div>
        <div>
            <div class="uk-card uk-card-default">
                <div class="uk-card-body" id="">
              <h3 class="uk-card-title uk-margin-remove-bottom">Installation Instructions</h3>
                    <p class="uk-margin-small">
                    Need help with the installation?
                        <div class="uk-margin-medium-top">
                            <a href="/docs/installation" class="uk-button uk-button-large uk-button-secondary uk-width-expand uk-margin-small-bottom"><i class="fa-solid fa-circle-question"></i> See instructions here</a>
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
            return total += parseInt(item.assets[0].download_count)
        }, 0)

            team.html(
              `<h3 class="uk-card-title uk-margin-remove-bottom">Latest Release</h3>
                    <p class="uk-margin-small" id="latest_release">
<h5 style="display:inline">Version:</h5> ${data[0].name}
</br>
<h5 style="display:inline">Name:</h5> ${data[0].body.split("\n")[0].replace("# ", "")}
</br>
<h5 style="display:inline">Released:</h5> ${new Date(data[0].assets[0].created_at).toDateString()}
</br>


<h5 style="display:inline">Downloads:</h5> Total: ${total_downloads} Latest: ${data[0].assets[0].download_count}
                        <div class="uk-margin-medium-top ">
                            <a href="${data[0].assets[0].browser_download_url}" class="uk-button uk-button-large uk-button-primary uk-width-expand uk-width-auto@m uk-margin-small-bottom"><i class="fa-solid fa-download"></i> Download</a>
                            <a href="https://github.com/open-stage/blender-dmx/releases/latest" class="uk-button uk-button-large uk-button-secondary uk-width-expand uk-width-auto@m uk-margin-small-bottom"><i class="fa-brands fa-github"></i> Go to release page</a>
                        </div>
                    </p>
              `);

    });
</script>
