---
id: recruiter
name: Recruiter
folders:
  - roles/
  - pipeline/
  - templates/
  - sensitive/candidates/
  - sensitive/feedback/
files: []
sensitive_hints:
  - Candidate names
  - Contact info
  - Interview feedback
  - Scorecards
  - Compensation discussions
  - Internal hiring decisions
---

# Use case: Recruiter

---

## Sensitive content hints (add to default)

- Candidate names, contact info, interview feedback, scorecards, compensation discussions, internal hiring decisions. Strongly recommend **private**. Keep in `sensitive/` (e.g. `sensitive/candidates/`, `sensitive/feedback/`). Committed docs: role descriptions, process templates, anonymized pipeline stats only.

---

## Additional structure (layer on top of default folders)

**Folders (in addition to default):**

- `roles/` — job descriptions, requirements, open/closed roles; one doc per role or pipeline stage
- `pipeline/` — pipeline stages, process, or local summary (no candidate names); detailed pipeline in `sensitive/pipeline/` if needed
- `templates/` — interview guides, scorecard templates, outreach templates (no candidate data)
- `sensitive/candidates/` — candidate info, contact, notes
- `sensitive/feedback/` — interview feedback, scorecards, hiring committee notes; never committed

*(Default `inbox/`, `archive/`, `sensitive/` already exist.)*

---

## Inbox processing default

1. List inbox; classify each item.
2. **Route:** Job description / role update → `roles/`. Candidate-related notes, feedback, or scorecards → `sensitive/candidates/` or `sensitive/feedback/` (do not commit). Interview guides or templates → `templates/`. Pipeline summary (anonymized counts/stages only) → `pipeline/`.
3. Committed files: role specs, process docs, templates. No candidate names, feedback, or compensation.
4. Move originals to `archive/` (date-prefixed) or `sensitive/`. Report what was processed.
5. Update ProjectIndex.md.

---

## README additions (folder table rows)

| `roles/` | Job descriptions, requirements, open/closed roles |
| `pipeline/` | Pipeline stages, process summary (anonymized) |
| `templates/` | Interview guides, scorecards, outreach templates |
| `sensitive/candidates/` | Candidate info, notes; gitignored |
| `sensitive/feedback/` | Interview feedback, scorecards; gitignored |

**Workflow:** Drop job posts and notes in inbox; AI routes to roles, process, or sensitive (candidates/feedback). Keep all candidate and feedback data in sensitive/ only.

---

## AGENTS.md additions (append after base sections)

### Project structure (recruiting)

- Roles, pipeline (anonymized), templates. All candidate data and interview feedback in `sensitive/candidates/` and `sensitive/feedback/`; never committed.
- Committed content: role descriptions, process docs, templates. No candidate PII or identifiable feedback.

### Working with this repo

- New role: add to roles/ from job description; add interview guides and outreach templates to templates/; keep all candidate-specific content in sensitive/.
- Before committing: confirm no candidate names, contact info, feedback, or compensation.
