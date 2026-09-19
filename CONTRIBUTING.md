# Contributing

This project is a prompt artifact, not a codebase. The whole project is one
`SKILL.md` plus example output, so contributions are mostly about wording and
rendering quality.

## What is most useful

- **Renders from other models.** Run the skill on a model that isn't in the README
  table and open an issue with what came out — especially if it came out badly.
- **Wording that improves the first shot.** The skill went through ~30 rounds of
  tuning. If you change a line, say which model you tested on and what changed in
  the render.
- **Edge cases in real syllabi.** Recurring rules, TBD dates, split schedule/grading
  documents, non-Monday week starts, quarter systems, labs and discussion sections.

## Ground rules for editing `skills/semester-matrix/SKILL.md`

- Keep it model-agnostic — no tool-specific or vendor-specific instructions.
- Keep the two-layer structure (semester view first, weekly view on click).
- Keep the inspection loop and the pass threshold.
- Keep cells text-free; marks only.
- Prefer removing a line over adding one. Length is not the goal; a clean first
  render is.

## Sharing a render

Please strip anything you don't want public before attaching a screenshot or an
HTML file — course codes, instructor names, and section numbers all travel with it.
