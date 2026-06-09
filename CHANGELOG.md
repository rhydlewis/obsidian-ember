# Changelog

All notable changes to Ember are documented here. Versions follow
[semantic versioning](https://semver.org).

## 1.0.1

Addresses Obsidian community-review feedback.

### Changed
- `authorUrl` now points to the author profile, not the theme repo.
- Properties: per-type colouring no longer uses `:has()` (keyed off the lucide
  icon class + `data-property-type` on the value element) — avoids the
  selector-invalidation performance warning.
- Task statuses: dropped `!important` from the glyph rules (the `body.ember-tasks`
  scope already wins on specificity), and removed `text-decoration-color`.
  `!important` count reduced from ~40 to 11 (remaining uses — reduce-motion,
  dyslexia font, font/active-row overrides — are necessary).

## 1.0.0

First public release.

### Added
- Warm dark + light schemes with an HSL-driven palette (`--base-h`,
  `--accent-h/s/l`).
- **Style Settings** integration: accent HSL picker, bundled **Catppuccin** and
  **Nord** palettes, true-black **OLED** mode, text/heading/mono font controls,
  code ligatures, old-style figures, dyslexia-friendly font, reading measure,
  comfortable/compact density, reduced motion, and per-element toggles.
- **Properties / frontmatter** card: per-type coloured icons, themed multi-select
  pills, tabular date/number values, optional banner (`--ember-banner-image`).
- **Callouts** tinted per type, sharing the task/property colour language.
- **Syntax highlighting** in ember tones for reading view (Prism) and live
  preview (CodeMirror).
- **Custom task statuses** — 25 Lucide-icon markers, colour-coded, in both views.
- **UI chrome**: command palette, modals, context menus, settings, status bar,
  hover popovers, tooltips; refined icon stroke.
- Styled **embeds**, opt-in list **relationship lines**, **mobile** chrome, and
  **Dataview** / **Kanban** plugin theming.
- Tables, pill tags, ember-edged blockquotes, themed titlebar/tabs/scrollbar,
  and ember-highlighted active rows across every sidebar.

### Notes
- No bundled or remotely-loaded fonts — defaults to the system stack; install
  the recommended fonts locally for the intended look (see the README).
- WCAG AA contrast checked across both schemes.
