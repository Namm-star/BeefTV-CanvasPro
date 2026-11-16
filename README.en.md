# BeefTV CanvasPro

[中文](README.md)

Windows installers and model packs for a CanvasPro-modified build of [BeefTV](https://github.com/glanderness/BeefTV). This repository is independently maintained and is not an official upstream release.

[Download the installer and configuration](https://github.com/Namm-star/BeefTV-CanvasPro/releases/latest)

The build is based on BeefTV v2.2.5 and preserves CanvasPro model packs, protocol mappings, result-download proxy settings and ComfyUI fixes. Engine 3 adds asynchronous temporary reference-media uploads for the adapted Jimeng protocols. The bundled pack has 350 models: 28 text, 45 image and 277 video.

The installer targets Windows x64 and is unsigned. It contains no user API keys, workspace databases or proxy settings. Model services require your own credentials and may charge for requests.

After upgrading, existing imported model packs remain active until replaced. Preview and apply the bundled update in model settings, or import the JSON attached to the release. Running tasks retain their original protocol snapshots.

Build commit: `40084f92e911f781f99fdef85881156313c8769f`. Model pack: `20261116-temporary-reference-media-v1-pack1`. Verify release assets with `SHA256SUMS.txt`.

See [LICENSE](LICENSE), [NOTICE](NOTICE) and [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) for upstream attribution and the applicable scoped licenses.
