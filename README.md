# Ember

A warm, low-glare Obsidian theme — charred near-black in dark mode, warm
parchment in light mode, with an ember-orange accent. Palette inspired by
[gethaunts.app](https://gethaunts.app).

## Fonts

| Role | Font |
|------|------|
| Body / UI | Hanken Grotesk |
| Headings | Bricolage Grotesque |
| Code | JetBrains Mono |

Loaded from Google Fonts via `@import` (needs internet on first load, then
cached). Falls back to system fonts offline. To use locally-installed fonts
instead, remove the `@import` line at the top of `theme.css`.

## Palette

| Token | Dark | Light |
|-------|------|-------|
| Background | `#0e0c0b` | `#fbf4ea` |
| Surface | `#161109` | `#fffaf2` |
| Text | `#f4ece2` | `#211913` |
| Muted | `#9c9085` | `#6b5d50` |
| Ember (core) | `#e8732c` | `#e8732c` |
| Accent / links | `#ffc26a` | `#b8410f` |
| Selection | ember @ 22% | ember @ 18% |

### Heading ramp
`h1`→`h6` step through a warm ember ramp (glow → amber → ember → deep ember →
muted → dim). `h1` also gets an ember underline. Edit the `--ember-h1`…
`--ember-h6` variables in the `.theme-dark` / `.theme-light` blocks to retune.

## Features

- Full dark + light variants
- Ember-highlighted **selected/active rows** in every sidebar (files, search,
  outline, bookmarks)
- Tables with a visible grid, shaded header, zebra rows, and horizontal scroll
  for wide tables
- Pill-style tags and inline code; ember-edged blockquotes
- Themed chrome: titlebar, tabs, scrollbar, active editor line
- **Custom task statuses** (Things-style) — colour-coded checkboxes for 25
  markers, in reading view and live preview

## Task statuses

Use `- [X]` where `X` is one of the markers below. Styling is keyed off
Obsidian's `data-task` attribute and works in both reading view and live
preview. Colours come from the `--task-*` variables (tweak per scheme near the
top of `theme.css`).

| Basic | | Extras | | Extras | |
|---|---|---|---|---|---|
| `/` incomplete | ◐ amber | `?` question | teal | `f` fire | red |
| `x` done | ember + strike | `!` important | red | `k` key | amber |
| `-` canceled | strike, dim | `*` star | amber | `w` win | green |
| `>` forwarded | → teal | `"` quote | muted | `u` up | ↑ green |
| `<` scheduling | ← teal | `l` location | teal | `d` down | ↓ red |
| | | `b` bookmark | teal | `D` draft PR | muted |
| | | `i` information | teal | `P` open PR | green |
| | | `S` savings | $ green | `M` merged PR | purple |
| | | `I` idea | amber | | |
| | | `p` pros | + green | `c` cons | − red |

> Glyphs are drawn as an SVG `mask` over the checkbox's `background-color`
> (pseudo-elements don't render on checkbox inputs in every Obsidian build, but
> masks always do). Markers without a clean monochrome glyph (bookmark, key,
> fire, PR states, etc.) use their letter, colour-coded. To change a glyph, edit
> the `<text>…</text>` content in that marker's rule in the *Task statuses*
> section of `theme.css`.

## Install / enable

The theme lives at `.obsidian/themes/Ember/`. Enable it via
**Settings → Appearance → Themes → Manage → Ember**, or set
`"cssTheme": "Ember"` in `.obsidian/appearance.json`.

For best results set **Settings → Appearance → fonts** to *Default* so the
theme's fonts win, and the **Accent color** to `#e8732c` (or `#ffc26a`).

## Customising

All colours are CSS variables defined in the `.theme-dark` and `.theme-light`
blocks near the top of `theme.css` (prefixed `--ember-*`). Change them there and
reload (Appearance → CSS / restart) to retheme without touching the rules below.

## Credits

- Palette inspiration: [Haunts](https://gethaunts.app)
- Fonts: Bricolage Grotesque, Hanken Grotesk, JetBrains Mono (all OFL)
