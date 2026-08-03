---
title: Vault Conventions
type: meta
created: 2026-08-03
tags:
  - meta
---

# Vault Conventions

How this vault is organised, so future-you doesn't have to guess. This is the note to
update when you change how you work.

## Folders

| Folder | Holds |
|---|---|
| `00-Meta/` | [[Syllabus]], [[Roadmap]], [[Progress-Tracker]], [[Glossary]], this note |
| `01-Fundamentals/` | Module 1 concepts — exposure, focus, the camera as a machine |
| `02-Light/` | Module 2 concepts |
| `03-Composition/` | Module 3 concepts |
| `04-Post-Processing/` | Module 4 concepts |
| `05-Genres/` | Module 5 — one note per genre |
| `06-Practice/` | Output, not theory: `Shoot-Logs/`, `Critiques/`, `Daily/` |
| `07-References/` | Photographers, books, courses, links |
| `99-Templates/` | Note templates (Templates plugin points here) |
| `attachments/` | Small reference JPEGs/PNGs only — see the size rule below |

Numeric prefixes exist to force the file explorer into learning order. Folders don't
affect linking — Obsidian resolves `[[Aperture]]` by name from anywhere, so move notes
freely.

## Naming

- Notes: `Title-Case-With-Hyphens.md` — hyphens rather than spaces keep GitHub URLs
  clean and avoid `%20` in links.
- Shoot logs: `YYYY-MM-DD-short-slug.md` (e.g. `2026-08-08-aperture-ladder.md`).
- Critiques: `Critique-Photographer-Subject.md`.

## Frontmatter properties

Every note gets frontmatter. The Properties plugin renders it as fields, and it's what
makes the vault searchable later.

```yaml
---
title: Aperture
type: concept          # concept | assignment | shoot-log | critique | genre | meta | reference
module: 1
status: seed           # seed | drafted | understood
tags:
  - fundamentals/exposure
confidence: 2          # 1-5, honest; drives what to revisit
---
```

`status` and `confidence` are the useful ones. Search `status: seed` to find your
backlog; search `confidence: 1` before a gate.

## Tags

Hierarchical, lowercase, singular:

`fundamentals/exposure` · `light/natural` · `light/flash` · `composition/colour` ·
`post/colour` · `genre/street` · `practice/shoot-log` · `practice/critique` ·
`meta/syllabus` · `gear/lens`

Tag by *topic*. Use folders for lifecycle stage, links for relationships, and tags for
cross-cutting themes. Don't duplicate the folder name as a tag.

## Linking

- Link generously. An unresolved `[[link]]` is a to-do, not an error — it shows up
  greyed out and in the Unlinked Mentions pane.
- Concept notes should link **up** to their module in [[Syllabus]] and **sideways** to
  related concepts.
- Shoot logs link to the concepts they tested. That backlink is how you later find
  "every frame where I was working on depth of field".

## Wikilinks vs Markdown links — a deliberate split

GitHub does **not** render `[[wikilinks]]`; Obsidian prefers them.

- **Inside the vault** → wikilinks. Obsidian is where you actually work, and wikilinks
  survive renames (`alwaysUpdateLinks` is on).
- **In [`README.md`](../README.md)** → standard Markdown links, because that file's
  audience is GitHub.

If you ever want the whole vault browsable on GitHub, flip
`useMarkdownLinks: true` in `.obsidian/app.json` — but existing wikilinks aren't
converted retroactively, so decide once.

## Images and repo size

`attachments/` is for **small web-sized reference images** — long edge ≤ 2000 px,
ideally under 500 KB. RAW files, PSDs and TIFFs are gitignored on purpose.

Git stores every version of a binary forever. A few hundred reference JPEGs is fine; a
folder of 40 MB RAWs will make the repo unclonable within a month. Your negatives
belong in your photo library with a 3-2-1 backup — see [[Archive-Strategy]] — not here.
This vault is the *notebook*.

## Git habits

- Commit at the end of each study session; the message is the week and the topic, e.g.
  `Week 2: shutter speed + ISO ladder notes`.
- `.obsidian/workspace.json` is ignored, so opening the vault on a second device won't
  produce a conflict.
- If you use Obsidian Sync *and* git, let Sync handle live sync and git handle history.
  Running both as sync mechanisms causes conflicts.
