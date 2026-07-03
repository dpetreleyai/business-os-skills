# Business-OS Skills Registry

Curated agent skills for [Business-OS](https://github.com/dpetreleyai/business-os)
workspaces. Operators' installs check this repo (at most daily) and get a
session-start notification when something new lands — they review and install
via `/skill-library`, no release-note chasing.

## Structure

- `registry.json` — the index clients read: name, version, description,
  category, file list per skill.
- `skills/<name>/SKILL.md` (+ any extra files listed in `files`).

## Publishing a skill

1. Add `skills/<name>/SKILL.md` — frontmatter `name` + `description`
   (description doubles as the review blurb operators see; write it for a
   business owner, not a developer).
2. Add the entry to `registry.json`; bump `version` on every content change
   (string compare — any change triggers the update notification).
3. Commit to `main`. Clients pick it up on their next daily check.

## Rules for skills in this registry

- Plain-language, owner-facing; assume the Business-OS folder structure
  (departments, `drafts/output/reference`, sibling vault, naming conventions).
- No credential handling, no network calls to non-registry hosts, no
  destructive file operations — the library skill flags violators instead of
  installing them.
- Save outputs where the structure says they belong; wire new artifacts into
  `CONTEXT.md`/vault so the guardian doesn't flag them as drift.
