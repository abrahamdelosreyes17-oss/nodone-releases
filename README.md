# NodOne Releases

This repository hosts the published Windows installers for **NodOne** —
a private workspace tool. NodOne's source code is not public; this repo
exists only to distribute installer binaries and metadata for the in-app
auto-updater.

## Latest release
See `releases.json` for the canonical version manifest.
See [GitHub Releases](https://github.com/abrahamdelosreyes17-oss/nodone-releases/releases) for the .exe artifacts.

## How updates work
The NodOne app fetches `releases.json` from this repo's `main` branch
(raw.githubusercontent.com). When a newer version appears, NodOne shows
an in-app prompt offering to install it.

## Publishing a release
See [RELEASE_PROCESS.md](./RELEASE_PROCESS.md).
