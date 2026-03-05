# Use case: Product Designer / User Research

**id:** `product-designer-research`

Research studies, findings, personas, and design artifacts. Inbox receives session notes, screenshots, and feedback; agent organizes and keeps participant data out of committed files.

---

## Sensitive content hints (add to default)

- Participant names, contact info, identifiable quotes, raw session recordings or transcripts. Keep in `sensitive/` (e.g. `sensitive/participants/`, `sensitive/sessions/`). Committed docs use anonymized quotes and aggregate findings only.

---

## Additional structure (layer on top of default folders)

**Folders (in addition to default):**

- `research/` — study plans, scripts, findings; one doc or subfolder per study or round
- `personas/` — persona docs (anonymized); no PII in committed versions
- `prototypes/` or `designs/` — links or exports of prototypes, key screens, design system snippets
- `usability-notes/` or `findings/` — synthesized insights, design implications (no participant IDs)
- `sensitive/participants/` or `sensitive/sessions/` — (optional) raw consent, contact info, unredacted transcripts; never committed

*(Default `inbox/`, `archive/`, `sensitive/` already exist.)*

---

## Inbox processing default

1. List inbox; classify each item.
2. **Route:** Session notes / raw feedback → anonymize and merge into `research/` or `usability-notes/`; store originals with PII in `sensitive/` if needed. Persona input → `personas/` (anonymized). Screenshots / design artifacts → `prototypes/` or `designs/`. Study plan or script → `research/`.
3. When adding to committed docs: strip participant identifiers; use "Participant A," "user reported…," or aggregate themes.
4. Move originals to `archive/` (date-prefixed) or `sensitive/`. Report what was processed.
5. Update ProjectIndex.md.

---

## README additions (folder table rows)

| `research/` | Study plans, scripts, findings (anonymized) |
| `personas/` | Persona docs (no PII) |
| `prototypes/` or `designs/` | Prototypes, key screens, design system |
| `usability-notes/` or `findings/` | Synthesized insights, design implications |
| `sensitive/participants/` or `sensitive/sessions/` | (If used) Raw participant data; gitignored |

**Workflow:** Drop session notes and artifacts in inbox; AI anonymizes and routes to research, personas, or findings. Keep raw participant data in sensitive/ only.

---

## AGENTS.md additions (append after base sections)

### Project structure (design / research)

- Research, personas, prototypes/designs, usability-notes. Participant PII only in `sensitive/` subfolders.
- In committed files: anonymized quotes ("Participant A"), aggregate themes, no names or contact info.

### Working with this repo

- New study: add plan and script in research/; store consent/contact/session raw data in sensitive/.
- Before committing: confirm no participant identifiers or unredacted transcripts.
