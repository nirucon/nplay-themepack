# NPLAY Theme Pack

Ten classic editor and terminal colour schemes for NPLAY.

**Status: beta** · Part of the [NIRUX](https://github.com/nirucon/nirux) suite · [MIT License](LICENSE)

## About

A small collection of external themes for
[NPLAY](https://github.com/nirucon/nplay), my terminal music player. It holds
only declarative `.toml` theme files and a standard-library Python installer.
It never modifies NPLAY itself, its playback, settings, Spotify credentials
or music database.

The palettes are unofficial adaptations inspired by well-known editor and
terminal colour schemes. The pack is not affiliated with or endorsed by the
original theme maintainers; only colour values are used, no logos, artwork or
code. For themes in the NIRUX style, see
[nplay-themepackniru](https://github.com/nirucon/nplay-themepackniru).

## Features

| Theme | ID | Character | Accent |
|---|---|---|---|
| Catppuccin Mocha | `catppuccin-mocha` | Soft charcoal, cream and lavender | `#CBA6F7` |
| Dracula | `dracula` | Dark plum with violet | `#BD93F9` |
| Everforest Dark | `everforest-dark` | Forest green and warm beige | `#A7C080` |
| Gruvbox Dark | `gruvbox-dark` | Warm vintage brown | `#FABD2F` |
| Kanagawa Wave | `kanagawa-wave` | Ink blue and soft periwinkle | `#7E9CD8` |
| Nord | `nord` | Arctic slate and frost | `#88C0D0` |
| One Dark | `one-dark` | Neutral editor charcoal | `#61AFEF` |
| Rosé Pine | `rose-pine` | Muted plum and rose | `#C4A7E7` |
| Solarized Dark | `solarized-dark` | Deep teal and muted gold | `#B58900` |
| Tokyo Night | `tokyo-night` | Deep navy and electric blue | `#7AA2F7` |

## Requirements

- NPLAY 1.4.1 or later (external TOML theme support).
- Python 3.11+ for the installer (`tomllib`).
- A terminal with at least 256 colours is recommended.

## Installation

The pack is not installed by NIRUX; install it by hand. From a clone or an
extracted release:

```sh
bash install.sh
```

The installer validates all ten files, then copies them to
`${XDG_CONFIG_HOME:-$HOME/.config}/nplay/themes/`. Existing files are
**never overwritten**, and a symlinked theme directory is refused. No root
privileges are needed. You can also copy single files from `themes/` into
that directory yourself.

## Usage

In NPLAY open **Browse → Settings → Appearance → Theme**, choose
**RELOAD CUSTOM THEMES**, then pick a theme (or press `t`). NPLAY saves the
choice.

To check the files:

```sh
python3 manage.py check
nplay --list-themes
nplay --check-theme ~/.config/nplay/themes/dracula.toml
```

## Uninstall

```sh
bash uninstall.sh
```

This removes the pack's files **only when they still match the distributed
originals**; anything you customized is kept. NPLAY's configuration and other
custom themes are untouched.

## Status, disclaimer and how it's made

**Status: beta.** The ten themes are complete and validated by the installer; they track NPLAY's theme format, which has been stable since 1.4.1.

NIRUX and every niru* project are made by me, Nicklas Rudolfsson
([@nirucon](https://github.com/nirucon)), for me. They are tailored to my own
needs, preferences and workflows, on my own machines. If they fit yours too,
that's a nice bonus.

- **Free and open source.** Anyone is free to use, study, change and share
  it under the [MIT License](LICENSE).
- **No guarantees.** There is no warranty of any kind. Use it at your own
  risk, read what you install and keep backups of anything that matters.
- **How it's made.** Some of these projects I built from scratch by hand. In
  more recent releases I have used Claude, Anthropic's AI, to do much of the
  heavy lifting under my direction: I decide what to build and how it should
  behave, and I test it on my own machines. It saves me a lot of time, and
  the result is quite OK.
- **Alpha, beta, dev, and maybe forever.** Most things here are alpha, beta
  or dev, and may stay that way. Maybe one day there will be a real stable
  release, but given how fast development moves, and how I am as a person,
  maybe never :)

| Label | Meaning |
|---|---|
| dev | Under active construction; may not build, install or work yet. |
| alpha | Works on my machines, but incomplete or rough; expect breaking changes. |
| beta | In daily use on my machines and mostly complete; rough edges remain. |

## License

MIT License, see [LICENSE](LICENSE). Copyright (c) 2026 Ing Leif Nicklas Rudolfsson.
