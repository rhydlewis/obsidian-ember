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

- [x] Revise task-status marker glyphs — replaced text-in-mask glyphs with
      Lucide vector masks (src/_tasks.scss, generated from lucide-static); crisp
      and consistent. Lightened global icon stroke for a refined feel.
- [x] Callouts — ember-tinted, per-type (src/_callouts.scss)
- [x] Code-block syntax highlighting (src/_code.scss)
- [x] UI chrome — modals, command palette, menus, settings, status bar (src/_chrome.scss)

## Upcoming (planned Phase 3 styling — directed one at a time)

- [ ] Embeds
- [ ] List relationship lines
- [ ] Mobile
- [ ] Plugins (Dataview, Kanban, Tasks, Calendar)
- [ ] Wire remaining element toggles (tables, tags, code blocks, embeds)
      to their styling

## Phase 4

- [ ] Accessibility/contrast pass (both schemes), PDF export, selector dedupe,
      screenshot (512×288), README/CHANGELOG, GitHub release + directory submission
