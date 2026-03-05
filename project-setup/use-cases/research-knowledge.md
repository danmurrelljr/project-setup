---
id: research-knowledge
name: Research / Knowledge
folders:
  - sources/
  - notes/
  - drafts/
  - citations/
  - sensitive/data/
  - sensitive/participants/
files: []
sensitive_hints:
  - Unpublished data
  - Human-subject information
  - Identifiable participant details
  - Confidential sources
---

# Use case: Research / Knowledge

---

## Sensitive content hints (add to default)

- Unpublished data, human-subject information, identifiable participant details, confidential sources. Keep in `sensitive/` (e.g. `sensitive/data/`, `sensitive/participants/`). Committed docs: anonymized or public-facing only.

---

## Additional structure (layer on top of default folders)

**Folders (in addition to default):**

- `sources/` — references, PDFs (or links), source metadata; one note or file per source or topic
- `notes/` or `literature/` — literature notes, reading notes, synthesized ideas; optionally by topic or author
- `drafts/` — paper, thesis, or article drafts; one folder or file per piece
- `citations/` or `references/` — bibliography, citation list, or export for Zotero/other (optional)
- `sensitive/data/` or `sensitive/participants/` — (optional) raw data, human-subject info; never committed

*(Default `inbox/`, `archive/`, `sensitive/` already exist.)*

---

## Inbox processing default

1. List inbox; classify each item.
2. **Route:** Source or reference → `sources/` (with minimal metadata: author, year, title, link or path). Quote or reading note → `notes/` or `literature/` (tag or link to source). Draft fragment or idea → `drafts/` (relevant piece). Raw data or participant info → `sensitive/data/` or `sensitive/participants/` (do not commit). Citation → `citations/` or into source note.
3. When adding to committed docs: no identifiable participant data; anonymize or aggregate.
4. Move originals to `archive/` (date-prefixed) or `sensitive/`. Report what was processed.
5. Update ProjectIndex.md.

---

## README additions (folder table rows)

| `sources/` | References, source metadata, links |
| `notes/` or `literature/` | Literature notes, reading notes, synthesized ideas |
| `drafts/` | Paper, thesis, or article drafts |
| `citations/` or `references/` | Bibliography, citation list (optional) |
| `sensitive/data/` or `sensitive/participants/` | (If used) Raw data, human-subject info; gitignored |

**Workflow:** Drop quotes and references in inbox; AI routes to sources, notes, or drafts. Keep raw data and participant info in sensitive/ only.

---

## AGENTS.md additions (append after base sections)

### Project structure (research / knowledge)

- Sources, notes (or literature), drafts, optional citations. Raw data and human-subject information only in `sensitive/` subfolders; never in committed files.
- In committed docs: anonymized findings, public sources, no identifiable participants.

### Working with this repo

- New source: add to sources/ with enough metadata to cite; link from notes when relevant.
- Before committing: confirm no unpublished data or participant identifiers.
