# Use case: Marketing

**id:** `marketing`

Campaigns, content calendar, assets, and performance. Inbox receives ideas, copy, and metrics; agent organizes and keeps unreleased or confidential strategy out of committed files.

---

## Sensitive content hints (add to default)

- Unreleased campaigns, pricing, confidential performance or strategy, identifiable customer data. Keep in `sensitive/` or redact in committed docs. Recommend private repo for internal marketing.

---

## Additional structure (layer on top of default folders)

**Folders (in addition to default):**

- `campaigns/` — one doc or subfolder per campaign; brief, channels, timeline, status
- `content/` — content calendar, copy drafts, headlines; by channel or date
- `assets/` — images, video references, brand assets (or links); optional subfolders by campaign or type
- `metrics/` or `performance/` — results, reach, conversion (anonymized or aggregate); one doc or dated reports

*(Default `inbox/`, `archive/`, `sensitive/` already exist.)*

---

## Inbox processing default

1. List inbox; classify each item.
2. **Route:** Campaign idea or brief → `campaigns/`. Copy or content idea → `content/`. Asset or creative reference → `assets/`. Performance data or metric → `metrics/` (anonymize if needed). Unreleased or confidential strategy → `sensitive/`.
3. Move originals to `archive/` (date-prefixed). Report what was processed.
4. Update ProjectIndex.md.

---

## README additions (folder table rows)

| `campaigns/` | Campaign briefs, channels, timeline, status |
| `content/` | Content calendar, copy drafts, headlines |
| `assets/` | Images, video refs, brand assets |
| `metrics/` or `performance/` | Results, reach, conversion (anonymized) |

**Workflow:** Drop ideas and copy in inbox; AI routes to campaigns, content, assets, or metrics. Keep unreleased strategy in sensitive/.

---

## AGENTS.md additions (append after base sections)

### Project structure (marketing)

- Campaigns, content, assets, metrics. Unreleased or confidential strategy in `sensitive/`.
- When referencing performance in committed docs, use anonymized or aggregate language.

### Working with this repo

- New campaign: add brief in campaigns/; link content and assets as they’re created.
- Before committing: no pricing, unreleased creative, or identifiable customer data.
