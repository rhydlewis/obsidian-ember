# Ember — TODO / backlog

Working backlog for the theme. Not shipped (releases attach only `theme.css` +
`manifest.json`).

## Open

- [ ] **Decide: should the Style Showcase table render real markers?** The
  "Marker" column currently shows ``/``, ``x``, ``>`` … as plain inline code.
  Question: render the actual styled/coloured marker glyph in that column for a
  live reference, or keep it as code? (Demo-note content question, not a theme
  bug — but ties into the glyph revision above.)

## Done

- [x] Mobile — navbar/toolbar/sidebar drawer polish (src/_mobile.scss)
- [x] Wire element toggles — tables + tags now gated (all element toggles live)
- [x] Embeds — ember-accented cards via native --embed-* vars (src/_embeds.scss)
- [x] List relationship lines — opt-in vertical guides (src/_lists.scss)
- [x] Plugins — Dataview inline fields + Kanban board/cards (src/_plugins.scss);
      Dataview tables inherit the base table styling
- [x] Revise task-status marker glyphs — replaced text-in-mask glyphs with
      Lucide vector masks (src/_tasks.scss, generated from lucide-static); crisp
      and consistent. Lightened global icon stroke for a refined feel.
- [x] Callouts — ember-tinted, per-type (src/_callouts.scss)
- [x] Code-block syntax highlighting (src/_code.scss)
- [x] UI chrome — modals, command palette, menus, settings, status bar (src/_chrome.scss)

## Upcoming

Phase 3 styling complete. Next is Phase 4 (below).

## Phase 4

- [ ] Accessibility/contrast pass (both schemes), PDF export, selector dedupe,
      screenshot (512×288), README/CHANGELOG, GitHub release + directory submission
