# NPLAY Theme Pack

**10 classic color schemes for NPLAY 1.4.1+** · A separate, unofficial community-style theme collection.

NPLAY is a personal Linux terminal audio player. This theme pack is independently installable: **it does not modify the NPLAY application, playback, settings, Spotify credentials, or music database.** It contains only declarative `.toml` files, plus a small standard-library Python installer.

## Themes

| Theme | Character | Accent |
|---|---|---|
| Catppuccin Mocha | Soft charcoal, cream and lavender | `#CBA6F7` |
| Dracula | Dark plum with violet | `#BD93F9` |
| Gruvbox Dark | Warm vintage brown | `#FABD2F` |
| Nord | Arctic slate and frost | `#88C0D0` |
| Tokyo Night | Deep navy and electric blue | `#7AA2F7` |
| Rosé Pine | Muted plum and rose | `#C4A7E7` |
| Solarized Dark | Deep teal and muted gold | `#B58900` |
| One Dark | Neutral editor charcoal | `#61AFEF` |
| Everforest Dark | Forest green and warm beige | `#A7C080` |
| Kanagawa Wave | Ink blue and soft periwinkle | `#7E9CD8` |

The palette values are unofficial adaptations inspired by recognizable editor/terminal color schemes. The pack is not affiliated with or endorsed by the original theme maintainers. Colors are used as palette data; no original logos, artwork, or software code are included.

## Requirements

- NPLAY **1.4.1 or later**, with external TOML theme support
- Python 3.11+ for the pack's installer
- A terminal with at least 256 colors recommended

## Installation

From the extracted pack directory:

```sh
bash install.sh
```

The installer checks all ten TOML files before copying them into `${XDG_CONFIG_HOME:-$HOME/.config}/nplay/themes/`. Existing files are **never overwritten**. No root privileges are needed.

Then open NPLAY:

1. Go to **Settings → Appearance → Theme**.
2. Select **RELOAD CUSTOM THEMES**.
3. Choose a theme. The selection is saved by NPLAY.

You can also copy individual `.toml` files from `themes/` into the same directory without using the installer.

## Validation

```sh
python3 manage.py check
nplay --list-themes
nplay --check-theme ~/.config/nplay/themes/dracula.toml
```

If you use a custom `XDG_CONFIG_HOME`, adjust the final path accordingly.

## Uninstall

```sh
bash uninstall.sh
```

The uninstaller removes only the pack's ten files **when their contents still match the distributed originals**. Any file you've customized is retained. Your NPLAY configuration and all unrelated custom themes are untouched.

## Development and compatibility

Each theme defines the six semantic roles supported by NPLAY 1.4.1: `fg`, `muted`, `accent`, `bg`, `select_fg`, `select_bg`. Theme IDs match filenames. These are deliberately simple themes: no executables, dependencies, shell expressions, or NPLAY source patches.

NPLAY currently maps RGB colors to its terminal palette. Exact colors can vary slightly depending on terminal support. These themes were validated against NPLAY's actual 1.4.1 theme loader; terminal screenshots are not supplied as they would depend on the user's terminal configuration.

## License and attribution

This repository's original scripts and documentation are released under the MIT License. The color palettes are unofficial adaptations of widely recognized themes and remain subject to any applicable upstream rights. The theme names identify the design inspirations, not endorsements.

This is a personal, best-effort project with no guaranteed support.

## Author

Ing Leif Nicklas Rudolfsson
