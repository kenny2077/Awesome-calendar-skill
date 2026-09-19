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

## Commit messages

This repo follows [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/).
The subject line is `<type>(<scope>): <summary>`, in the imperative, lowercase, with no
trailing period and no more than 72 characters.

```text
feat(site): lead the landing page with the live calendar

The demo now opens the page with no copy above it, so the first thing a
visitor does is hover a cell.
```

### Types

| Type | Use it for |
| --- | --- |
| `feat` | A new capability a user can see |
| `fix` | A defect corrected |
| `refactor` | Restructuring with no change in behaviour |
| `style` | Visual or formatting work with no change in behaviour |
| `docs` | README, CONTRIBUTING, comments |
| `chore` | Tooling, config, housekeeping |
| `build` | Assets and artifacts that ship with the repo |
| `revert` | Undoing an earlier commit |

### Scopes

| Scope | Covers |
| --- | --- |
| `skill` | `skills/semester-matrix/SKILL.md` |
| `site` | `index.html`, the GitHub Pages demo |
| `demo` | `examples/` |
| `assets` | `docs/assets/` |
| `docs` | `README.md`, `CONTRIBUTING.md` |
| `repo` | Licence, ignore files, repository configuration |

Omit the scope when a change genuinely spans the repo. Add `!` after the type or scope
for a breaking change — for this project that means the skill no longer produces the
same two-layer output from the same inputs.

### Body

Say what changed and why, not how. Wrap at 80 characters. Reference issues with
`Refs #12` or `Closes #12` on their own line at the end.
