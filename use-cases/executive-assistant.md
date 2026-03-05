---
id: executive-assistant
name: Executive Assistant
folders:
  - meetings/
  - travel/
  - tasks/
  - contacts/
  - templates/
  - sensitive/calendar/
  - sensitive/contacts/
  - sensitive/travel/
  - sensitive/meetings/
files: []
sensitive_hints:
  - Executive calendar
  - Travel details
  - Contact lists
  - Confidential meeting notes
  - Compensation or HR-related items
---

# Use case: Executive Assistant

---

## Sensitive content hints (add to default)

- Executive calendar, travel details, contact lists, confidential meeting notes, compensation or HR-related items. Strongly recommend **private**. Keep in `sensitive/` (e.g. `sensitive/calendar/`, `sensitive/contacts/`). Committed docs: work-safe summaries, templates, and process notes only.

---

## Additional structure (layer on top of default folders)

**Folders (in addition to default):**

- `meetings/` — meeting prep, agendas, follow-ups (work-safe summaries); sensitive details in `sensitive/meetings/` if needed
- `travel/` — itineraries, confirmations (work-safe summaries); full details in `sensitive/travel/`
- `tasks/` or `action-items/` — running task list, deadlines, status (sanitized for commit or local-only)
- `contacts/` — work-safe contact index (role, org); full contact PII in `sensitive/contacts/`
- `templates/` — recurring meeting templates, travel checklists, document templates
- `sensitive/` subfolders as needed: calendar, contacts, travel, meetings for confidential detail

*(Default `inbox/`, `archive/`, `sensitive/` already exist.)*

---

## Inbox processing default

1. List inbox; classify each item.
2. **Route:** Meeting notes / action items → `meetings/` (summary) or `tasks/`; full confidential notes → `sensitive/meetings/`. Travel confirmations → `travel/` (summary) or `sensitive/travel/`. Contact info → `sensitive/contacts/`; work-safe role/org only in `contacts/`. General tasks → `tasks/`.
3. Sanitize: committed files get summaries and no PII (no full itineraries, personal numbers, exec calendar).
4. Move originals to `archive/` (date-prefixed) or `sensitive/`. Report what was processed.
5. Update ProjectIndex.md.

---

## README additions (folder table rows)

| `meetings/` | Meeting prep, agendas, follow-ups (work-safe) |
| `travel/` | Travel summaries; full itineraries in sensitive/travel/ |
| `tasks/` or `action-items/` | Task list, deadlines |
| `contacts/` | Work-safe contact index; PII in sensitive/contacts/ |
| `templates/` | Meeting, travel, document templates |
| `sensitive/` subfolders | Calendar, contacts, travel, meetings (confidential); gitignored |

**Workflow:** Drop action items and confirmations in inbox; AI routes to meetings, travel, tasks, or contacts. Keep confidential detail in sensitive/ only.

---

## AGENTS.md additions (append after base sections)

### Project structure (executive support)

- Meetings, travel, tasks, contacts, templates. All confidential detail (calendar, full itineraries, contact PII, sensitive meeting notes) in `sensitive/` subfolders only.
- Committed content: work-safe summaries, templates, process notes. No exec calendar, full travel details, or contact PII.

### Working with this repo

- Default timeline: log under current date unless specified.
- Before committing: confirm no calendar, travel PII, or contact details in committed files.
- **Commit Format:** Always use the format `{project-name}: {message}`.
