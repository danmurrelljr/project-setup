# Use case: Product Manager

**id:** `product-manager`

Roadmap, requirements, backlog, and stakeholder alignment for a product or product area. Inbox captures feedback, ideas, and meeting notes; agent routes them and keeps docs current.

---

## Sensitive content hints (add to default)

- Unreleased strategy, pricing, confidential stakeholder feedback, identifiable customer PII. Keep in `sensitive/` or redact in committed docs. Recommend private repo.

---

## Additional structure (layer on top of default folders)

**Folders (in addition to default):**

- `roadmap/` — initiatives, themes, timeline (e.g. by quarter or release)
- `requirements/` or `prds/` — product requirements, PRDs, user stories; one doc or subfolder per initiative/feature
- `backlog/` — prioritized backlog, discovery items, or link to external tool (with local summary if needed)
- `stakeholders/` — alignment notes, key partners, eng/design contacts (work-safe summaries)
- `metrics/` or `reports/` — success metrics, adoption, outcomes (anonymized or aggregate)

*(Default `inbox/`, `archive/`, `sensitive/` already exist.)*

---

## Inbox processing default

1. List inbox; classify each item.
2. **Route:** Feature request / idea → `backlog/` or relevant PRD in `requirements/`; meeting notes / alignment → `stakeholders/` or `roadmap/`; feedback or metric → `metrics/` or appropriate requirements doc; strategy or confidential → `sensitive/` or redact before committing.
3. Move originals to `archive/` (date-prefixed). Report and suggest follow-ups (e.g. "Three items added to backlog—consider prioritization").
4. Update ProjectIndex.md.

---

## README additions (folder table rows)

| `roadmap/` | Initiatives, themes, timeline |
| `requirements/` or `prds/` | PRDs, user stories, requirements |
| `backlog/` | Prioritized backlog, discovery items |
| `stakeholders/` | Alignment notes, key partners |
| `metrics/` or `reports/` | Success metrics, outcomes (anonymized) |

**Workflow:** Drop feedback and notes in inbox; AI routes to roadmap, requirements, backlog, or stakeholders. Keep confidential strategy in sensitive/.

---

## AGENTS.md additions (append after base sections)

### Project structure (product management)

- Roadmap, requirements (or PRDs), backlog, stakeholders, metrics. Sensitive or unreleased strategy in `sensitive/`.
- When referencing customers or internal feedback in committed docs, anonymize or aggregate.

### Working with this repo

- Keep roadmap and backlog in sync; when requirements change, note the delta and where it’s documented.
- Before committing: no pricing, unreleased strategy, or identifiable customer data.
