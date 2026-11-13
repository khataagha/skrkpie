# SGRGPY

`SGRGPY` is a macOS desktop GUI wrapper for `scrcpy`, designed around the scrcpy CLI but tailored for a fast, polished experience on macOS 12.x.

It is intentionally shaped around the workflow you described:
- neutral, minimal interface inspired by modern design systems such as Tabler
- standard macOS window chrome with traffic lights
- device mirror vs. extended display mode
- slider controls + keyboard-enterable numeric fields
- bottom Android navigation bar (Recent / Home / Back)
- preferences window via Command+, and profile presets
- ready-to-run packaging script for a macOS `.app` bundle

## Requirements

- macOS 12 or newer
- `scrcpy` installed and available on `PATH`
- Xcode command-line tools (`xcode-select --install`)

## Install `scrcpy`

If you do not already have it:

```bash
brew install --cask android-platform-tools
brew install scrcpy
```

If `scrcpy` is not in your PATH, you can either:
- export `SCRCPY_BIN=/path/to/scrcpy`
- or place the binary in `/opt/homebrew/bin/scrcpy` or `/usr/local/bin/scrcpy`

## Build the app bundle

From the repository root:

```bash
cd sgrgpy
./build_app.sh
```

This creates:

```text
dist/SGRGPY.app
```

You can then run it by double-clicking the app bundle in Finder.

## App behavior

- `Resolution`: slider and numerical input
- `Bitrate`: slider and numeric field
- `FPS`: slider and numeric field
- `Mirror` or `Extended display`
- `Audio`, `Show touches`, `Stay awake`, `Fullscreen`
- `Record to file`
- `Preferences...` via Command+, with appearance and preset management

## App name and tagline

- Name: `SGRGPY`
- Tagline: `gui the f in scrcpy`

## Notes

The app is built as a thin wrapper around the official scrcpy binary, so it remains compatible with current scrcpy releases while providing a native desktop interface.
