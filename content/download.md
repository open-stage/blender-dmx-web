---
title: Download
menu:
  main:
    weight: 1
  footer2:
    name: Download
    weight: 3
    params:
      icon: fa-download
---

<div class="uk-container">
    <div class="uk-grid uk-grid-match uk-child-width-1-2@m uk-text-small" uk-grid>
        <div>
            <div class="uk-card uk-card-default">
                <div class="uk-card-body">
                    <h3 class="uk-card-title uk-margin-remove-bottom">Get Add-on</h3>
                    <p class="uk-margin-small">
                    Install BlenderDMX directly from the repository below or use the manual download options.
                    </p>
                    <div class="uk-margin-medium-top">
                      {{< latest_release_asset repo="open-stage/blender-dmx" label="Drag and Drop into Blender" class="uk-button uk-button-large uk-button-secondary uk-width-expand uk-margin-small-bottom" draggable="true" button="true" repository="https://blenderdmx.eu/api/v1/extensions/index.json" blender_version_min="4.2.0" >}}
                    </div>
                    <div>Drag & drop into Blender will add the BlenderDMX.eu repository for easy install and automatic updates of the BlenderDMX extension. Select the "Check for updates at Start". (Online Access must be allowed). After adding the repo, you can then Install the extension via menu - Preferences - Get Extensions, or Enable the extension via menu - Preferences - Get Add-ons. It is named <strong>DMX</strong>.</div>
                     <details class="uk-margin-small-top" open>
                      <summary class="uk-link-text">Video</summary>
                      <p class="uk-margin-small-top">
                        {{< video "../docs/media/enable_blenderdmx_repo1.mp4" "../docs/media/enable_blenderdmx_repo1.mp4" >}}
                      </p>
                    </details>
                    <details class="uk-margin-small-top">
                      <summary class="uk-link-text">Manual install</summary>
                      <p class="uk-margin-small-top">
                        You can manually <a id="manual-download-link" href="#">download</a> and install the Add-on without the automatic updates. <a href="/docs/extension-help/">Install from Disk</a> help page.
                      </p>
                    </details>
                    <details class="uk-margin-small-top">
                      <summary class="uk-link-text">Manual repository setup</summary>
                      <p class="uk-margin-small">
                        Blender 4.2 and newer can install BlenderDMX directly from this site by adding the BlenderDMX repository. It happens automatically upon drag&drop into Blender, but you can also do it manually:
                      </p>
                      <ol class="uk-list uk-list-decimal uk-margin-small">
                        <li>In Blender, open <strong>Edit &rarr; Preferences &rarr; Get Extensions &rarr; Repositories</strong>.</li>
                        <li>Click <strong>+</strong> to add a new repository.</li>
                        <li>Paste this URL into the repository field.</li>
                        <li>Select the "Check for updates at Start".</li>
                        <li>Press Create</li>
                      </ol>
                      <div class="uk-margin-small-top uk-flex uk-flex-middle uk-flex-nowrap">
                        <input
                          id="repo-url"
                          class="uk-input uk-form-small"
                          type="text"
                          readonly
                          value="https://blenderdmx.eu/api/v1/extensions/index.json"
                          aria-label="BlenderDMX repository URL"
                          style="border-top-right-radius: 0; border-bottom-right-radius: 0;"
                        />
                        <button
                          id="copy-repo-url"
                          class="uk-button uk-button-default uk-button-small"
                          type="button"
                          aria-label="Copy repository URL"
                          title="Copy repository URL"
                          style="margin-left: -1px; border-top-left-radius: 0; border-bottom-left-radius: 0; box-shadow: none;"
                        >
                          <i class="fa-solid fa-copy"></i>
                        </button>
                      </div>
                      <div class="uk-margin-small-top">
                        <span id="copy-repo-status" class="uk-text-meta"></span>
                      </div>
                    </details>
                </div>
            </div>
        </div>
    </div>
</div>

<script>
  (function () {
    const input = document.getElementById("repo-url");
    const button = document.getElementById("copy-repo-url");
    const status = document.getElementById("copy-repo-status");
    const dragButton = document.querySelector(".js-drag-download");
    const manualDownloadLink = document.getElementById("manual-download-link");

    if (!input || !button || !status) {
      return;
    }

    const setStatus = (message) => {
      status.textContent = message;
    };

    input.addEventListener("focus", () => {
      input.select();
    });

    if (dragButton && manualDownloadLink) {
      const downloadUrl = dragButton.getAttribute("data-download-url");
      const downloadName = dragButton.getAttribute("data-download-name") || "blenderdmx.zip";
      manualDownloadLink.href = downloadUrl || "#";
      manualDownloadLink.download = downloadName;
      dragButton.setAttribute("title", "Drag into Blender");
      dragButton.setAttribute("aria-label", "Drag and Drop into Blender");
    }

    button.addEventListener("click", async () => {
      try {
        await navigator.clipboard.writeText(input.value);
        setStatus("Copied.");
        return;
      } catch (error) {
        input.focus();
        input.select();
        const copied = document.execCommand("copy");
        setStatus(copied ? "Copied." : "Copy failed. Select the URL and copy it manually.");
      }
    });

    document.querySelectorAll(".js-drag-download").forEach((element) => {
      element.addEventListener("click", (event) => {
        event.preventDefault();
      });
      element.addEventListener("dragstart", (event) => {
        const downloadUrl = element.getAttribute("data-download-url");
        const downloadName = element.getAttribute("data-download-name") || "blenderdmx.zip";

        if (!downloadUrl || !event.dataTransfer) {
          return;
        }

        event.dataTransfer.effectAllowed = "copy";
        event.dataTransfer.setData("text/plain", downloadUrl);
        event.dataTransfer.setData("text/uri-list", downloadUrl);
        event.dataTransfer.setData("DownloadURL", `application/zip:${downloadName}:${downloadUrl}`);
      });
    });
  })();
</script>
