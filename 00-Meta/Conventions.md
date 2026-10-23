---
title: Vault Conventions
type: meta
created: 2026-08-03
tags:
  - meta/conventions
---
# Vault Conventions

How this vault is organised, so future-you doesn't have to guess. This is the note to
update when you change how you work.

## Folders

| Folder | Holds |
|---|---|
| `00-Meta/` | [[Syllabus]], [[Roadmap]], [[Glossary]], this note |
| `01-Fundamentals/` | Modules 0–1 — setup, exposure, focus, the camera as a machine |
| `02-Light/` | Module 2 concepts |
| `03-Composition/` | Module 3 concepts |
| `04-Post-Processing/` | Module 4 concepts |
| `05-Video/` | Module 5 — shooting and editing video |
| `06-Genres/` | Module 6 — one note per genre |
| `06-Practice/` | Output, not theory: `Shoot-Logs/`, `Critiques/`, `Daily/` |
| `07-Critique/` | Module 7 — seeing, critique, a body of work; capstone planning |
| `07-References/` | Photographers, books, courses, links |
| `99-Templates/` | Note templates (Templates plugin points here) |
| `attachments/` | Small reference JPEGs/PNGs only — see the size rule below |

Numeric prefixes exist to force the file explorer into learning order. Folders don't
affect linking — Obsidian resolves `[[Aperture]]` by name from anywhere, so move notes
freely.

Templates are notes too, so Obsidian indexes them: their `type` and `status` fields
would turn up in searches and in any Bases view. Keep them out with Settings → Files
and links → Excluded files → `99-Templates/`.

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
type: concept          # concept | assignment | shoot-log | critique | daily | genre | index | meta | reference
module: 1
tags:
  - fundamentals/exposure
created: 2026-08-03
---
```

There are no `status` or `confidence` fields on concept, genre or assignment notes. The
vault doesn't track progress; you do. Meta and reference notes keep a document `status`
of `draft` or `active`. To search by property, use square brackets: `[module:2]`,
`[type:genre]`.

## What a study note contains

Every concept in the [[Syllabus]] has a full note, built on [[Concept-Note]]:

1. **In one line** — a summary at the top
2. **What it is**, **How it works** (the mechanism), **How to use it**
3. **On your kit** — the L10, iPhone, Pocket 3 and Action 5 Pro, from [[My-Kit]]
4. **Common mistakes** and **Try it** (a short exercise, tied to an assignment)
5. **Check yourself** — questions whose answers fold open when you click them
6. **Related** — links, ending with the module's index note

Genre notes cover the seven points listed in [[Genre-Index]] instead.

**No blank line between the closing `---` and the `# Heading`.** The H1 starts on the
very next line. Applies to every note and every template in `99-Templates/`.

## Tags

Hierarchical, lowercase, singular:

`fundamentals/exposure` · `light/natural` · `light/flash` · `composition/colour` ·
`post/colour` · `video/editing` · `video/sound` · `genre/street` · `seeing/critique` ·
`practice/shoot-log` · `practice/critique` · `meta/syllabus` · `gear/kit`

Tag by *topic*. Use folders for lifecycle stage, links for relationships, and tags for
cross-cutting themes. Don't tag a note with its bare folder name (`light` on a note in
`02-Light/`), because that says nothing the folder doesn't. A hierarchical tag like
`light/flash` is fine: the second level adds the topic.

## Linking

- Link generously, but only to notes that exist. An unresolved `[[link]]` shows dimmed
  in the editor. It means a note is missing: write it, or remove the link. (Unlinked
  mentions are something else: plain-text uses of a note's name.)
- Concept notes link **sideways** to related concepts and **up** to their module's
  index note.
- Shoot logs link to the concepts they tested. That backlink is how you later find
  "every frame where I was working on depth of field".

## Wikilinks vs Markdown links — a deliberate split

GitHub does **not** render `[[wikilinks]]`; Obsidian prefers them.

- **Inside the vault** → wikilinks. Obsidian is where you actually work, and links are
  rewritten on rename (`alwaysUpdateLinks` is on, for both link styles).
- **In [`README.md`](../README.md)** → standard Markdown links, because that file's
  audience is GitHub.

If you ever want the whole vault browsable on GitHub, you'd need two settings:
`useMarkdownLinks: true` *and* "New link format" set to "Relative path to file"
(`newLinkFormat: relative`). The current `shortest` format writes bare filenames, which
break across folders on GitHub. Existing wikilinks aren't converted retroactively, so
decide once.

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
