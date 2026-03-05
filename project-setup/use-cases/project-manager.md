---
id: project-manager
name: Project Manager
folders:
  - projects/
  - status/
  - risks/
  - deliverables/
  - stakeholders/
files: []
sensitive_hints:
  - Internal cost data
  - Vendor terms
  - Identifiable performance or escalation details
---

# Use case: Project Manager

---

## Sensitive content hints (add to default)

- Internal cost data, vendor terms, identifiable performance or escalation details. Keep in `sensitive/` if needed. Recommend private repo for internal projects.

---

## Additional structure (layer on top of default folders)

**Folders (in addition to default):**

- `projects/` — one subfolder or doc per project/initiative; scope, timeline, key dates
- `status/` — status reports, weekly or milestone summaries; or a single `status.md` with rolling updates
- `risks/` — risk register, blockers, mitigation notes; one doc or dated entries
- `deliverables/` — deliverables checklist, acceptance criteria, handoff notes
- `stakeholders/` — project stakeholders, RACI or contact summary (work-safe)

*(Default `inbox/`, `archive/`, `sensitive/` already exist.)*

---

## Inbox processing default

1. List inbox; classify each item.
2. **Route:** Status update / progress → `status/` or relevant project in `projects/`. Risk or blocker → `risks/`. Deliverable or handoff → `deliverables/`. Stakeholder or dependency note → `stakeholders/` or project doc. Timeline or milestone change → `projects/` (relevant initiative).
3. Move originals to `archive/` (date-prefixed). Report what was processed and any new risks or blockers.
4. Update ProjectIndex.md.

---

## README additions (folder table rows)

| `projects/` | Per-project scope, timeline, key dates |
| `status/` | Status reports, milestone summaries |
| `risks/` | Risk register, blockers, mitigation |
| `deliverables/` | Deliverables checklist, handoff notes |
| `stakeholders/` | Project stakeholders, RACI (work-safe) |

**Workflow:** Drop updates and blockers in inbox; AI routes to status, risks, deliverables, or project docs. Keep status and risk register current; commit after milestones or on request.

---

## AGENTS.md additions (append after base sections)

### Project structure (project management)

- `projects/`: One doc or subfolder per initiative; scope, timeline, key dates.
- `status/`: Rolling status reports or milestone summaries.
- `risks/`: Risk register; add blockers and mitigation; keep dated.
- `deliverables/`: Checklist, acceptance criteria, handoff notes.
- `stakeholders/`: Stakeholder summary (work-safe); sensitive detail in sensitive/ if needed.

### Working with this repo

- Default timeline: log under current date unless specified.
- When adding risks or blockers, note owner and next step.
- Before committing: no internal cost or vendor terms unless in sensitive/.
