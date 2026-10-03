# Hackerboy — an Omarchy theme

[Omarchy](https://omarchy.org/)'s stock **Hackerman** theme — near-black
navy background, neon-green accent — with a **full-colour terminal
palette**, so `eza`/`ls`, `git`, syntax highlighting and TUIs read in
real colour instead of green-on-green.

![Hackerboy — btop and LazyVim on the theme's Milky Way wallpaper](screenshot.webp)

## Why

Hackerman looks great as a desktop: dark navy, neon-green borders, a
green bar. In the terminal the same idea works against it. Every ANSI
slot is a shade of green or pale blue-green — "red" is `#50f872`,
"yellow" is `#50f7d4` — so anything that uses colour to carry meaning
loses it:

- `eza`/`ls` listings: directories, executables, symlinks, permissions
  and dates all come out the same green.
- `git diff`: added and removed lines are both green.
- Errors and warnings don't stand out from normal output.
- Syntax highlighting and TUIs like btop collapse to one hue.

Hackerboy keeps everything that makes Hackerman look the way it does —
background, foreground, the green accent, green and cyan — and replaces
only the slots that were green stand-ins with the hues their names
promise. Red is red, yellow is yellow, blue is blue. They're bright,
slightly neon tones chosen to sit on the near-black navy without
clashing with the green.

- `background = #0B0C16`, `foreground = #ddf7ff`, `accent = #82FB9C`
  (all unchanged from Hackerman, as are green and cyan)
- New hues: `red #ff5f7a`, `yellow #f7d450`, `orange #ffa057`,
  `blue #5c9dff`, `magenta #c77dff`, `brown #b08d57` (plus brights)
- Folder icons: same as Hackerman
- 4 bundled backgrounds in `backgrounds/`

Window borders and the bar stay Hackerman green. Anything Omarchy
generates from the palette — btop, Neovim, VS Code, error colours —
picks up the new hues.

## Install

```bash
omarchy theme install https://github.com/ggregoro/hackerboy
omarchy theme set Hackerboy
```

Or clone it manually:

```bash
git clone https://github.com/ggregoro/hackerboy \
  ~/.config/omarchy/themes/hackerboy
omarchy theme set hackerboy
```

Cycle backgrounds with `Super+Ctrl+Space` or `omarchy theme bg next`.

## Tweaking

Edit `colors.toml`, then re-run `omarchy theme set hackerboy`.
Everything else — terminal colours, Hyprland borders, the bar, btop,
Neovim — regenerates from it.

## Revert

`omarchy theme set hackerman` returns to Omarchy's stock theme.

## Credits & licensing

The base palette (background, foreground, accent, green, cyan) comes
from the Hackerman theme that ships with Omarchy. The bundled wallpapers
are a personal selection, including a Milky Way photo by Jeremy Thomas
on Unsplash. Swap `backgrounds/` for your own if you prefer. Theme files
(`colors.toml`, `icons.theme`, this README) are MIT-licensed — see
`LICENSE`.
