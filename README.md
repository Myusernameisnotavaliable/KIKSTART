# KIKSTART

KIKSTART is a browser-based football game project under active development.

- **Play the current hosted build:** https://kikstart.pages.dev/
- **Project status:** actively being developed; features and behaviour may change.

## Features

The project includes football matches, squad and player progression, local save data, and an online friend-match mode. Online play uses PeerJS and browser WebRTC networking. These features are still being developed and should not be assumed to be production-ready.

## Source layout

The website is served as static files. The root `index.html` loader fetches and joins the numbered `site-v40.5-part-01.txt` through `site-v40.5-part-15.txt` files in order. Keep the loader and all referenced parts together in the same folder when running the project.

Older standalone HTML files and older source parts are retained as historical builds. They are not necessarily the current website source.

## Run locally

The loader uses `fetch()` to load the source parts, so serve the folder over HTTP rather than opening `index.html` directly as a `file://` URL.

With Python 3 installed, run this from the repository folder:

```bash
python3 -m http.server 8000 --bind 127.0.0.1
```

Then open <http://127.0.0.1:8000/> in a browser. Stop the local server with `Ctrl+C` in the Terminal window where it is running.

The project currently has no package-manager build step. Some browser libraries are loaded from external CDNs, so an internet connection is needed for all features to load.

## Saves

Game progress is stored locally in the browser used to play. Browser storage is separate between browsers and profiles. Clearing the site's browser data can remove local progress, so back up important saves before clearing browser data.

## Development notes

- Make changes on a development branch and review the diff before merging.
- Preserve the static-hosting layout unless a change explicitly requires otherwise.
- Test gameplay and online features in real browser sessions; source inspection alone is not proof that a feature works.
- Do not commit API keys, passwords, access tokens, private keys, or account-specific service credentials. See [SECURITY.md](SECURITY.md).

## Licence

No licence is currently included in this repository. Do not assume that the code, artwork, audio, or other included assets are available for reuse or redistribution. A licence will be added only after the project owner has confirmed the rights and chosen the intended terms.
