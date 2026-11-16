# KIKSTART download and release process

This file documents the intended public distribution setup. The game source repository remains private.

## Current state

- Source repository: `Myusernameisnotavaliable/KIKSTART` (private).
- Website: `https://kikstart.pages.dev/` (Cloudflare Pages).
- Download page: `/download.html`.
- Mac application archive: not yet supplied/published.
- Native macOS auto-updater: not yet implemented.

## Publishing the Mac app

1. Build and test the actual `KIKSTART.app` bundle. An HTML file is not a Mac app installer.
2. On a Mac, sign the app with an appropriate Developer ID certificate and notarize it for distribution where possible.
3. Zip the finished app bundle without changing its internal structure.
4. Publish the ZIP as an asset attached to a GitHub Release in a separate public downloads repository.
5. Replace the "COMING SOON" status on `download.html` with a link to the actual release asset.
6. Test the download link in a signed-out/private browser session and test installation on a second Mac.

## Website updates vs installed app updates

Updating the Pages site's `index.html` updates the browser game. It does not modify the copy of `Resources/index.html` inside an already-installed app.

For the installed Mac app to receive gameplay updates without replacing the app bundle, its web-view wrapper must deliberately load the hosted game URL, or use a separate signed update mechanism. Before changing the app to load the hosted site, verify save-data migration and test the online 1v1 flow on two devices.

## Release checklist

- [ ] Confirm the tested game version and preserve the existing release.
- [ ] Confirm player saves are backed up and remain compatible.
- [ ] Build and test the real Mac application bundle.
- [ ] Sign and notarize the app for distribution.
- [ ] Upload the ZIP to a public GitHub Release.
- [ ] Replace the placeholder status on `download.html` with the release link.
- [ ] Test the download, extraction, installation and launch on another Mac.
- [ ] Test that website updates do not erase saved progress.
