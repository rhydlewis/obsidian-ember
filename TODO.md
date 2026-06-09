# Ember — TODO / backlog

Working backlog for the theme. Not shipped (releases attach only `theme.css` +
`manifest.json`).

## Open

- [ ] **Revise task-status marker glyphs.** The custom task markers (`◐ ✕ → ←
  ★ ? !` … and lettered ones like `b k w`) are drawn as `<text>` inside an SVG
  `mask` over the checkbox background. They look odd — inconsistent
  alignment/weight/size across markers, and the text-in-mask approach is
  fragile. Revise: tune mask sizing/baseline per glyph, or move to proper
  vector icon paths for a cleaner, consistent set. Check against the Tasks
  section of `Style Showcase.md` in both schemes.

- [ ] **Decide: should the Style Showcase table render real markers?** The
  "Marker" column currently shows ``/``, ``x``, ``>`` … as plain inline code.
  Question: render the actual styled/coloured marker glyph in that column for a
  live reference, or keep it as code? (Demo-note content question, not a theme
  bug — but ties into the glyph revision above.)

## Upcoming (planned Phase 3 styling — directed one at a time)

- [ ] Callouts (next)
- [ ] Code-block syntax highlighting
- [ ] UI chrome (modals, command palette, settings, status bar, search, popovers)
- [ ] Embeds
- [ ] List relationship lines
- [ ] Mobile
- [ ] Plugins (Dataview, Kanban, Tasks, Calendar)
- [ ] Wire remaining element toggles (tables, tags, tasks, code blocks, embeds)
      to their styling

## Phase 4

- [ ] Accessibility/contrast pass (both schemes), PDF export, selector dedupe,
      screenshot (512×288), README/CHANGELOG, GitHub release + directory submission
