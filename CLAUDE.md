# CLAUDE.md

Guidance for Claude Code working in this repository.

## What this is

A **personal photography learning vault** — not a software project. Plain Markdown,
edited in Obsidian, version-controlled with git (remote: `LeeChengZhan2/Photography`).
There is no build, no test suite, no dependencies. The artefact is understanding.

Curriculum: [Syllabus](00-Meta/Syllabus.md) (7 modules + capstone) ·
[Roadmap](00-Meta/Roadmap.md) (28 weeks, started 2026-08-03) ·
[Progress-Tracker](00-Meta/Progress-Tracker.md) · [Conventions](00-Meta/Conventions.md)

## The one rule that matters

**Do not write the concept notes.** The vault's purpose is for the *user* to explain
photography in their own words — that act of explanation is the learning. A concept note
Claude wrote is worse than an empty one, because it looks finished and silently removes
the exercise.

So when asked about a concept, prefer to:

- **Quiz, don't tell.** Ask what they think happens and why, then correct.
- **Review their draft** — flag what's vague, wrong, or copied rather than understood.
- **Ask for the mechanism.** If a note only defines a term, ask *why* the physics
  behaves that way.
- **Point at the gap** — "your [[Aperture]] note has no frames linked; which shoot
  proves it?"

Claude *should* write freely: scaffolding, templates, indexes, tables of contents,
reference lists, glossary one-liners, tracker updates, git plumbing, and anything in
`00-Meta/`, `07-References/`, or `99-Templates/`.

If the user explicitly asks Claude to draft a concept note, do it — but mark it as a
draft to be rewritten, the way [Aperture](01-Fundamentals/Aperture.md) is marked. Never
silently set `status: understood` on the user's behalf.

## Layout

```
CLAUDE.md · README.md (GitHub landing) · Home.md (Obsidian hub)
00-Meta/            syllabus, roadmap, tracker, glossary, conventions
01-Fundamentals/    Module 1 — exposure, focus, the camera
02-Light/           Module 2
03-Composition/     Module 3
04-Post-Processing/ Module 4
05-Genres/          Module 5 — one note per genre
06-Practice/        Shoot-Logs/ · Critiques/ · Daily/   ← output, not theory
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
  type: concept | assignment | shoot-log | critique | genre | index | meta | reference
  module: 1-6
  status: seed | drafted | understood
  confidence: 1-5      # honest; drives what to revisit before a gate
  tags: [fundamentals/exposure]
  ```
- **Tags** are hierarchical, lowercase, singular: `fundamentals/exposure`,
  `light/flash`, `composition/colour`, `genre/street`, `practice/shoot-log`. Tag by
  topic. Never duplicate the folder name as a tag.
- **Links:** `[[Wikilinks]]` inside the vault; **standard Markdown links in
  `README.md` only**, because GitHub can't render wikilinks. Don't "fix" wikilinks in
  vault notes into Markdown links — that split is deliberate and documented in
  [Conventions](00-Meta/Conventions.md).
- Obsidian resolves `[[Note]]` by name from any folder, so a link never needs a path.
- An unresolved `[[link]]` is a **to-do, not a bug**. Do not create stub files just to
  satisfy one.
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
  `core-plugins.json`, `appearance.json`, `graph.json`, `templates.json`,
  `daily-notes.json`) *is* tracked.
- **Don't add `.gitkeep` placeholders.** If a folder needs to exist in a clone, give it
  a real index note that earns its place.
- **Don't tick boxes in [Progress-Tracker](00-Meta/Progress-Tracker.md)** unless the
  user says the work is done. It's their record.
- **Don't reorder the syllabus modules.** Exposure → light → composition → post is
  load-bearing; each module's assignments assume the previous module's control. Dates
  can slip freely, sequence can't.
- **Don't recommend gear purchases** unless asked. Modules 0–4 need nothing new.

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
- Auditing for orphaned notes, or concept notes with no linked shoot log
- Rescheduling the roadmap dates after a slip, keeping the gate order intact
