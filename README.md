# Ember

A warm, low-glare Obsidian theme — charred near-black in dark mode, warm
parchment in light mode, with an ember-orange accent. Palette inspired by
[gethaunts.app](https://gethaunts.app).

## Fonts

Ember ships with **no bundled or remotely-loaded fonts** — it defaults to your
system font stack, so it works fully offline with zero network calls. For the
intended look, install the three recommended fonts locally (all are free and
open-source) and point Obsidian at them.

| Role | Recommended font | Download |
|------|------------------|----------|
| Body / UI | Hanken Grotesk | [Google Fonts](https://fonts.google.com/specimen/Hanken+Grotesk) |
| Headings | Bricolage Grotesque | [Google Fonts](https://fonts.google.com/specimen/Bricolage+Grotesque) |
| Code | JetBrains Mono | [jetbrains.com/lp/mono](https://www.jetbrains.com/lp/mono/) · [GitHub releases](https://github.com/JetBrains/JetBrainsMono/releases) |

### 1. Download

From each link above, choose **Get font → Download all** (Google Fonts) or grab
the release `.zip` (JetBrains Mono). You'll get a folder of `.ttf` / `.otf`
files.

### 2. Install on your OS

- **macOS (Homebrew)** — the quickest route, no manual download needed:
  ```sh
  brew install --cask font-hanken-grotesk font-bricolage-grotesque font-jetbrains-mono
  ```
- **macOS (manual)** — unzip, select all the font files, double-click and choose
  **Install Font** (or drag them into the *Font Book* app).
- **Windows** — unzip, select all the font files, right-click → **Install for
  all users**.
- **Linux** — copy the font files into `~/.local/share/fonts/` (or
  `/usr/share/fonts/` for all users), then run `fc-cache -f`.

Restart Obsidian after installing so it picks up the newly-available fonts.

### 3. Tell Obsidian to use them

Install the **Style Settings** community plugin, then set the text, heading,
and monospace fonts under **Settings → Style Settings → Ember → Typography** —
type the exact font name (e.g. `Hanken Grotesk`, `Bricolage Grotesque`,
`JetBrains Mono`).

Alternatively set the base interface/text font under
**Settings → Appearance → Font**, and the code font under
**Settings → Appearance → Monospace font**.

> If a named font isn't installed, the theme falls back to the system stack
> automatically — nothing breaks, you just won't see that specific typeface.

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
- **Style Settings** support — accent (HSL) picker, bundled Catppuccin / Nord
  palettes, true-black OLED mode, font controls, reading measure, compact
  density, reduced-motion and dyslexia-friendly options, plus per-element
  toggles
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
- Task-status marker glyphs use [Lucide](https://lucide.dev) icons (ISC licence),
  the same icon set Obsidian ships
