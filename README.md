# Sipa Fusion Cascade Calculator V3.2 (English Edition)

## Overview

This is the English-language edition of the Sipa Fusion Cascade Calculator V3.2. It preserves the calculation and planning logic of the supplied Chinese V3.2 package while translating the user interface, generated plan text, offline message, and installation-related metadata into English.

The tool provides four modes:

1. **By Application Scenario** — presets for a single ultra-wide screen, L-shaped two-wall setup, U-shaped three-wall setup, four walls, four walls plus floor, six surfaces, and custom projection surfaces.
2. **By Channel Count** — estimate blending-unit count and cascade topology for 1–32 output channels.
3. **Plan from Wall Dimensions** — compare landscape and portrait projector orientations for 1–6 equal-sized walls, using wall dimensions, overlap percentage, target coverage, and optional throw ratio.
4. **Media Resolution** — estimate a logical media canvas from wall count, projector count per wall, per-channel resolution, orientation, and overlap percentage.

## Calculation assumptions and limits

- Each projector is counted as one blending output channel.
- One or two output channels are estimated as one blending unit. Above two channels, the calculator groups channels in pairs and assigns any remaining channel to the final unit (for example, 3 = 2+1, 5 = 2+2+1, and 6 = 2+2+2).
- The calculator does not select or certify a specific blending-processor model.
- Wall-dimension planning assumes equal-sized walls with the same projector count per wall. If dimensions differ, calculate each wall separately.
- Estimated throw distance is image width multiplied by the entered throw ratio. It is not a final mounting dimension.
- Media-canvas results are logical estimates. They are not a guarantee of media-server input timing, encoded video dimensions, output timing, corner compensation, or frame-accurate synchronization.
- The 1080p and 4K media settings are candidate starting points for testing, not universal certification standards. Validate each device model, firmware, resolution, and USB/internal-storage playback path separately.
- Results are for preliminary engineering planning only, not installation drawings or a guarantee of performance.

## Files in this package

- `index.html` — calculator interface and calculation logic
- `manifest.json` — Progressive Web App metadata
- `sw.js` — offline caching service worker
- `offline.html` — offline fallback page
- `header-logo.png` — Sipa header logo
- `icon-192.png` — app icon
- `icon-512.png` — large app icon

## Publish on GitHub Pages

Recommended repository name: `sipa-fusion-calc-en`.

1. Sign in to GitHub as `wj710528-hub`.
2. Create a **new public repository** named exactly `sipa-fusion-calc-en`. Do not overwrite the Chinese `sipa-fusion-calc` repository.
3. Unzip this package on your computer.
4. Open the new repository and choose **Add file → Upload files**.
5. Upload the *contents* of the unzipped package to the repository root. `index.html`, `manifest.json`, `sw.js`, `offline.html`, the three PNG files, and `README.md` should be at the top level, not nested inside another folder.
6. Commit the upload to the `main` branch.
7. Open **Settings → Pages**.
8. Under **Build and deployment**, choose **Deploy from a branch**; select branch `main` and folder `/(root)`, then save.
9. Wait for the Pages deployment to finish. The expected URL is `https://wj710528-hub.github.io/sipa-fusion-calc-en/`.
10. Open that URL on a computer and a phone. Test all four modes, both per-channel resolutions, copy/download actions, and the QR code before distributing it.

## Add to a phone home screen

### iPhone / iPad
1. Open the published URL in Safari.
2. Tap **Share**.
3. Select **Add to Home Screen**.
4. Confirm the name and tap **Add**.

### Android
1. Open the published URL in Chrome.
2. Tap the three-dot menu.
3. Select **Install app** or **Add to Home screen** (wording depends on the device/browser).
4. Confirm installation.

Open the page online successfully at least once before testing offline use. Offline operation depends on browser cache and service-worker support.

## Updating the English edition

1. Make a backup of the currently published files.
2. Update the relevant files in the repository.
3. **Increment `CACHE_NAME` in `sw.js`** for each published update (for example, from `sipa-fusion-en-v1-cache` to `sipa-fusion-en-v2-cache`) so browsers can refresh cached files.
4. Commit the changes and wait for GitHub Pages to deploy.
5. Test in a private/incognito browser window and on at least one phone. If a phone still shows an old version, close the installed app and reopen it online; if necessary, remove the old home-screen shortcut and add it again.

## Release note

This edition is a translation of the supplied Chinese V3.2 package. The Sipa logo and app icons are retained. The English QR posters in the companion materials point to the expected URL above; they will work only after the repository has been created and GitHub Pages has successfully published that exact URL.
