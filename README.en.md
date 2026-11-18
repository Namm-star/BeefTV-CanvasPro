# BeefTV CanvasPro

[中文](README.md)

Windows installers and model packs for a CanvasPro-modified build of [BeefTV](https://github.com/glanderness/BeefTV). This repository is independently maintained and is not an official upstream release.

[Download the installer and configuration](https://github.com/Namm-star/BeefTV-CanvasPro/releases/latest)

The build is based on BeefTV v2.2.5 and preserves CanvasPro model packs, protocol mappings, result-download proxy settings and ComfyUI fixes. Engine 3 adds asynchronous temporary reference-media uploads for the adapted Jimeng protocols. The bundled pack has 349 models: 28 text, 45 image and 276 video.

This release fixes completed asynchronous images being reported as model-service failures when artifact downloads fail. Recovery queries the original task using its frozen protocol and downloads its output without submitting generation again. Historical unrecoverable conclusions can be rechecked when the exact original task ID and query protocol remain available. Explicit generation failure ends recovery, and a mismatched returned task ID stops retrieval.

This hotfix waits until the entire reference-media batch is complete before validating its temporary HTTPS URLs and submitting generation. It fixes premature failures when individual items are ready but the batch has not published its URLs, while preserving the original reference order.

The current distribution removes upstream BeefTV login, balance, top-up, official-account connections and automatic account recovery. Legacy login and payment endpoints are unavailable. Upstream application auto-updates are disabled; download subsequent modified builds from this repository's releases.

The installer targets Windows x64 and is unsigned. It contains no user API keys, workspace databases or proxy settings. Model services require your own credentials and may charge for requests.

After upgrading, existing imported model packs remain active until replaced. Preview and apply the bundled update in model settings, or import the JSON attached to the release. Running tasks retain their original protocol snapshots.

Download `BeefTV-v2.2.5-windows-amd64-artifact-recovery-20261118-setup.exe`, save your canvas and exit BeefTV before installing the update. Build commit: `428fd98`. Model pack: `20261117-suanli-maintenance-add-10-rates-counts-v3-pack1`; users already on this pack do not need to import it again. Verify release assets with `SHA256SUMS.txt`. Existing CanvasPro and other user-key connections are retained. Nodes configured with the retired upstream account require a different model service.

For a retrieval failure, use Continue retrieval on the original task before considering regeneration. The recovery fix requires updating the application; importing the model pack alone does not update execution logic.

See [LICENSE](LICENSE), [NOTICE](NOTICE) and [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) for upstream attribution and the applicable scoped licenses.
