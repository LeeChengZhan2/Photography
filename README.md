# 📷 Photography

A personal learning vault — a structured, self-taught photography curriculum kept as
plain Markdown, edited in [Obsidian](https://obsidian.md) and version-controlled here.

Not a portfolio. This is the notebook: the theory in my own words, the assignments, the
shoot logs, and the record of what I got wrong.

---

## Start here

| | |
|---|---|
| 📚 [**Syllabus**](00-Meta/Syllabus.md) | Seven modules — objectives, concepts, assignments, exit tests |
| 🗓️ [**Roadmap**](00-Meta/Roadmap.md) | 28-week schedule with dates and gates |
| ✅ [**Progress Tracker**](00-Meta/Progress-Tracker.md) | Current position |
| 📖 [**Glossary**](00-Meta/Glossary.md) | Terms, one line each |
| 🧭 [**Conventions**](00-Meta/Conventions.md) | Folders, naming, tags, linking rules |
| 🏠 [**Home**](Home.md) | The Obsidian entry hub |

## The curriculum in one screen

| # | Module | Weeks | Question it answers |
|---|---|---|---|
| 0 | Orientation & Setup | ½ | What does my kit do, and where do the files go? |
| 1 | Exposure & the Camera | 4 | Can I choose settings from intent, in seconds? |
| 2 | Light | 4 | Can I read light before I raise the camera? |
| 3 | Composition & Visual Language | 4 | Is every element in the frame on purpose? |
| 4 | Post-Processing & Colour | 4 | Can I finish a coherent set, repeatably? |
| 5 | Genre Deep-Dive (pick two) | 4 | What does depth in one genre demand? |
| 6 | Seeing, Critique & Body of Work | 4 | Can I say what my work is about? |
| — | **Capstone** | 4 | A 12–20 image series, sequenced, printed, stated. |

Five gates punctuate the sequence. The order matters more than the dates — later
modules assume the earlier ones.

## Structure

```
├── Home.md                 Obsidian entry hub
├── CLAUDE.md               guidance for Claude Code in this vault
├── 00-Meta/                syllabus, roadmap, tracker, glossary, conventions
├── 01-Fundamentals/        exposure, focus, the camera as a machine
├── 02-Light/               quality, direction, colour, flash
├── 03-Composition/         visual language
├── 04-Post-Processing/     RAW workflow, colour, output
├── 05-Genres/              one note per genre
├── 06-Practice/            Shoot-Logs/ · Critiques/ · Daily/
├── 07-References/          photographers, books, tools
├── 99-Templates/           note templates
└── attachments/            small reference images only
```

Each module folder carries a `*-Index.md` map-of-content note listing its concepts and
assignments.

## How this vault works with each tool

**Obsidian** is the primary interface. Notes are linked with `[[wikilinks]]`, tagged
hierarchically (`fundamentals/exposure`), and carry YAML frontmatter that the
Properties view renders as fields. The Templates plugin points at `99-Templates/`, and
daily notes land in `06-Practice/Daily/`. Shared config
(`app.json`, `core-plugins.json`, `appearance.json`, `graph.json`) is committed;
per-machine UI state (`workspace.json`) is not, so the vault opens cleanly on a second
device without merge conflicts.

**GitHub** is history and backup, not a reading interface. Two consequences:

- GitHub doesn't render `[[wikilinks]]`, so cross-links look like plain text here.
  That's a deliberate trade — see
  [Conventions](00-Meta/Conventions.md#wikilinks-vs-markdown-links--a-deliberate-split).
  This README uses standard Markdown links so it reads correctly on GitHub.
- **RAW files, PSDs and TIFFs are gitignored.** Negatives live in a photo library with
  its own 3-2-1 backup. Only small web-sized reference JPEGs belong in `attachments/`,
  because git keeps every version of a binary forever.

## Conventions, briefly

- Notes: `Title-Case-With-Hyphens.md` · shoot logs: `YYYY-MM-DD-slug.md`
- Frontmatter carries `type`, `module`, `status` (`seed` → `drafted` → `understood`)
  and an honest `confidence: 1–5`. Search `confidence: 1` before a gate.
- Commit at the end of each study session: `Week 2: shutter speed + ISO ladder notes`

Full detail in [Conventions](00-Meta/Conventions.md).

## Status

Draft `v0.1` — syllabus and roadmap scaffolded 2026-08-03. Concept notes are written as
the modules are worked through; [Aperture](01-Fundamentals/Aperture.md) is a worked
example of the intended standard.
