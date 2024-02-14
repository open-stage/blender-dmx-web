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
                        <div class="uk-margin-medium-top">
                            <a href="https://github.com/open-stage/blender-dmx/releases/latest" class="uk-button uk-button-secondary"><i class="fa-solid fa-download"></i> Go to release page</a>
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
                            <a href="/docs/installation" class="uk-button uk-button"><i class="fa-solid fa-circle-question"></i> See instructions here</a>
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
    $.get("https://api.github.com/repos/open-stage/blender-dmx/releases/latest", (data) => {
            team.html(
              `<h3 class="uk-card-title uk-margin-remove-bottom">Latest Release</h3>
                    <p class="uk-margin-small" id="latest_release">
<h5 style="display:inline">Version:</h5> ${data.name}
</br>
<h5 style="display:inline">Name:</h5> ${data.body.split("\n")[0].replace("# ", "")}
                        <div class="uk-margin-medium-top">
                            <a href="${data.assets[0].browser_download_url}" class="uk-button uk-button-secondary"><i class="fa-solid fa-download"></i> Download</a>
                            <a href="https://github.com/open-stage/blender-dmx/releases/latest" class="uk-button uk-button"><i class="fa-brands fa-github"></i> Go to release page</a>
                        </div>
                    </p>
              `);

    });
</script>
