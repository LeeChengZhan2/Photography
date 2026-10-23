# CLAUDE.md

Guidance for Claude Code working in this repository.

## What this is

A **personal photography learning vault** — not a software project. Plain Markdown,
edited in Obsidian, version-controlled with git (remote: `LeeChengZhan2/Photography`).
There is no build, no test suite, no dependencies. The artefact is understanding.

Curriculum: [Syllabus](00-Meta/Syllabus.md) (8 modules + capstone) ·
[Roadmap](00-Meta/Roadmap.md) (32 weeks, starting 2026-10-26, with time per module) ·
[Conventions](00-Meta/Conventions.md)

## The one rule that matters

**Every title opens a complete note.** The user learns by reading these notes, shooting
the assignments, and answering each note's "Check yourself" questions. They asked for the
notes to hold the knowledge itself, so a concept that is only a title, or an empty stub,
is a gap to fix — not a to-do for them. (On 2026-10-22 this replaced the vault's
original rule that the user writes every note in their own words.)

Concept notes follow [Concept-Note](99-Templates/Concept-Note.md): a one-line summary,
what it is, how it works, how to use it, the user's kit, common mistakes, a short
exercise, and 3–5 folded question callouts with answers. Genre notes cover the seven
points in [Genre-Index](06-Genres/Genre-Index.md).
[Exposure-Triangle](01-Fundamentals/Exposure-Triangle.md) is the reference for tone and
depth.

When writing or changing a note:

- **Plain, simple English.** Short sentences, everyday words, every term explained the
  first time. British spelling.
- **Mechanism first.** Explain *why* something behaves as it does, not only the rule.
- **Kit facts come from [My-Kit](01-Fundamentals/My-Kit.md) only.** Its specs were
  checked against the makers' pages; don't invent menu paths, buttons or specs.
- **No stubs, no blanks to fill in.** Don't link a note that doesn't exist: write it,
  or leave the link out.

When the user asks about a concept, it still helps to ask what they think first and
then correct them — but the full answer belongs in the note.

**There is no progress tracker, by the user's choice.** They track their own progress.
Don't add checklists, `status`/`confidence` fields, or ticking to any note.

## Layout

```
CLAUDE.md · README.md (GitHub landing) · Home.md (Obsidian hub)
00-Meta/            syllabus, roadmap, glossary, conventions
01-Fundamentals/    Modules 0–1 — setup, exposure, focus, the camera
02-Light/           Module 2
03-Composition/     Module 3
04-Post-Processing/ Module 4
05-Video/           Module 5 — shooting and editing video
06-Genres/          Module 6 — one note per genre
06-Practice/        Shoot-Logs/ · Critiques/ · Daily/   ← output, not theory
07-Critique/        Module 7 — seeing, critique, a body of work; capstone planning
07-References/      photographers, books, tools
99-Templates/       note templates (Templates plugin points here)
attachments/        small reference images only
```

Each module folder has a `*-Index.md` map-of-content note. Numeric prefixes force the
file explorer into learning order; they carry no other meaning.

## Conventions to follow when editing

- **Filenames:** `Title-Case-With-Hyphens.md`. Shoot logs `YYYY-MM-DD-slug.md`.
  Hyphens not spaces, so GitHub URLs stay clean.
- **Frontmatter on every note:**
  ```yaml
  title: Shutter Speed
  type: concept | assignment | shoot-log | critique | daily | genre | index | meta | reference
  module: 0-7
  tags: [fundamentals/exposure]
  created: 2026-10-22
  ```
  No blank line between the closing `---` and the `# Title`.
- **Tags** are hierarchical, lowercase, singular: `fundamentals/exposure`,
  `light/flash`, `composition/colour`, `genre/street`, `practice/shoot-log`. Tag by
  topic. Never tag a note with its bare folder name (`light` on a note in `02-Light/`).
- **Links:** `[[Wikilinks]]` inside the vault; **standard Markdown links in
  `README.md` only**, because GitHub can't render wikilinks. Don't "fix" wikilinks in
  vault notes into Markdown links — that split is deliberate and documented in
  [Conventions](00-Meta/Conventions.md).
- Obsidian resolves `[[Note]]` by name from any folder, so a link never needs a path.
- Every `[[link]]` must open a note with real content. An unresolved link is a gap:
  write the note, or remove the link. Never create an empty stub.
- Prose wraps at ~88 columns. Use Obsidian callouts (`> [!note]`, `> [!tip]`) rather
  than raw HTML.

## Things not to do

- **Don't commit binaries.** RAW (`.CR3`, `.NEF`, `.ARW`, …), PSD, TIFF and video are
  gitignored deliberately — git keeps every version of a binary forever and would make
  the repo unclonable. Only web-sized JPEG/PNG references (long edge ≤ 2000 px, under
  ~500 KB) belong in `attachments/`. If a rule needs relaxing, edit `.gitignore` and say
  why; never use `git add -f`.
- **Don't commit `.obsidian/workspace.json`.** It's per-machine UI state and the main
  cause of multi-device merge conflicts. Shared config (`app.json`,
  `core-plugins.json`, `community-plugins.json`, `appearance.json`, `graph.json`,
  `templates.json`, `daily-notes.json`) *is* tracked.
- **Never commit credentials.** `.obsidian/plugins/` is gitignored, and
  `.obsidian/plugins/*/data.json` independently as a second line of defence — plugins
  store access tokens there. Don't relax either rule, and never `git add -f` inside
  `.obsidian/plugins/`. Same for `.env`, `*.pat` and `.git-credentials`.
- **Don't add `.gitkeep` placeholders.** If a folder needs to exist in a clone, give it
  a real index note that earns its place.
- **Don't add progress tracking** — no tracker note, checkbox lists of done work, or
  `status`/`confidence` fields. The user keeps track themselves.
- **Don't reorder the syllabus modules.** Exposure → light → composition → post is
  load-bearing; each module's assignments assume the previous module's control. Dates
  can slip freely, sequence can't.
- **Don't recommend gear purchases** unless asked. Modules 0–5 need nothing new.

## Editing while Obsidian is open

Obsidian usually has this vault open and will rewrite `.obsidian/*.json` from its
in-memory state. After changing config there, verify the write survived rather than
assuming it did — and prefer telling the user to change settings in the UI for anything
they can reach through Settings.

## Git

- Not on a branch workflow; work goes straight to `main`.
- Commit at the end of a study session. Message format is the week and topic:
  `Week 2: shutter speed + ISO ladder notes`
- **Only commit or push when asked.** Prefer leaving changes staged and reporting them.
- If Obsidian Sync is ever enabled, let Sync handle live sync and git handle history —
  running both as sync mechanisms causes conflicts.

## Useful tasks to offer

- Updating the "This week" block in [Home.md](Home.md) from the
  [Roadmap](00-Meta/Roadmap.md)
- Building an Obsidian **Bases** view over shoot logs or assignments (the Bases core
  plugin is enabled)
- Adding a glossary entry for a term the user hit
- Auditing for unresolved links, orphaned notes, or topics the syllabus doesn't cover
- Updating notes when the kit changes (start from [My-Kit](01-Fundamentals/My-Kit.md))
- Rescheduling the roadmap dates after a slip, keeping the gate order intact
