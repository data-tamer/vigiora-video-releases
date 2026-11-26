# Vigiora Video releases

Downloads for Vigiora Video, a video editor for short-form marketing content.
Each release on this page carries the macOS installer and its SHA-256 checksum.

## Install on macOS

1. Open the latest release and download `Vigiora-Video-<version>-macos-arm64.dmg`.
2. Open the DMG and drag **Vigiora Video** to Applications, then launch it. The
   app is signed and notarised, so it opens without a right-click.

Requires macOS 14 or later on Apple Silicon. ffmpeg is bundled; nothing else
to install.

To check a download: `shasum -a 256 -c Vigiora-Video-<version>-macos-arm64.dmg.sha256`
in the folder that holds both files.

## Other platforms

There is no Intel macOS, Linux or Windows package yet.

## Packs

The app downloads content packs (sounds, footage, templates, effects) from
the index at https://github.com/data-tamer/videox-packs. Anyone can add a
pack there by pull request.

## Everything the app does is an API

Every action in the window is also an HTTP action on `127.0.0.1:7788`, and
`videoo-mcp` exposes the same actions as MCP tools, so a script or an agent
can drive the editor. The app carries its own recipe books: call
`list_skills` and `get_skill` over the API.
