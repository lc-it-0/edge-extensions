# edge-extensions

Automated CRX hosting for Microsoft Edge MDM deployment via `ExtensionInstallForcelist`.

## Extensions

| Extension | Version | Update Manifest |
|---|---|---|
| uBlock Origin (MV2) | see `docs/ublock-origin/version.txt` | `https://lc-it-0.github.io/edge-extensions/ublock-origin/update-manifest.xml` |

## How it works

1. GitHub Actions checks daily for new uBlock Origin releases
2. Downloads the official Chromium build from GitHub
3. Signs it with a private key (stored as Actions Secret)
4. Publishes `.crx` + `update-manifest.xml` to GitHub Pages
5. Edge polls the update manifest automatically on all managed Macs
