# Use case: Personal Finance

**id:** `personal-finance`

Secure, local-first tracking of personal finances with an AI assistant: add data to inbox, AI organizes it, builds reports, and runs analyses. Designed for Cursor, Claude Code, Windsurf, or similar.

---

## Sensitive content hints (add to default)

- Account numbers, balances, SSN, financial institution names, raw statements, invoices with PII, tax documents, identity documents. Strongly recommend **private**. In any committed markdown, **redact**: use masked identifiers (e.g. `Chase-****1234`, `Bank-****5678`), never full account numbers.

---

## Additional structure (layer on top of default folders)

**Inside `sensitive/`** (default folder; add subfolders):

- `sensitive/statements/` — raw statements by institution
- `sensitive/invoices/` — invoices with PII by category
- `sensitive/tax_docs/` — by tax year
- `sensitive/identity/` — passports, IDs, critical identity docs

**Top-level (in addition to default):**

- `invoices/` — processed or non-sensitive invoices, organized by year/month
- `statements/` — summaries or redacted statement copies only (no PII)
- `budget/` — monthly and annual budget tracking
- `transactions/` — transaction CSVs by account, combined monthly ledgers
- `reports/` — generated net worth, cash flow, spending analysis
- `recurring/` — subscriptions, utilities, fixed bills
- `projects/` — one folder per initiative (big purchase, audit, life event); each has `Status.md` and supporting docs
- `cleanup/` — audit logs, reconciliation checklists
- `notes/` — daily logs, financial goals, stream-of-consciousness
- `templates/` — markdown templates for entries and reports

*(Default `inbox/` and `archive/` already exist.)*

---

## Inbox processing default

Route by content type: statements → `statements/` (redacted) or `sensitive/statements/` (raw); transactions/CSVs → `transactions/`; invoices → `invoices/` or `sensitive/invoices/`; tax docs → `sensitive/tax_docs/`. Process and move; redact any committed summary (masked account IDs only). Update ProjectIndex.md (and reports if needed) after processing.

---

## README additions (folder table rows)

| `sensitive/statements/` | Raw statements by institution (gitignored) |
| `sensitive/invoices/` | Invoices with PII (gitignored) |
| `sensitive/tax_docs/` | Tax docs by year (gitignored) |
| `sensitive/identity/` | Identity documents (gitignored) |
| `invoices/` | Processed invoices by year/month |
| `statements/` | Redacted statement summaries only |
| `budget/` | Monthly and annual budget |
| `transactions/` | Transaction CSVs, monthly ledgers |
| `reports/` | Net worth, cash flow, spending analysis |
| `recurring/` | Subscriptions, utilities, fixed bills |
| `projects/` | One folder per initiative; each has Status.md |
| `cleanup/` | Audit logs, reconciliation checklists |
| `notes/` | Logs, goals, notes |
| `templates/` | Markdown templates |

**Workflow:** Add data to inbox (or directly to folders); ask AI to process inbox into the right place. Log activity in notes. Commit only redacted markdown and non-sensitive assets. Prefer local-only or self-hosted Git (e.g. Forgejo) for backup without cloud.

---

## AGENTS.md additions (append after base sections)

### Project structure (personal finance)

- **Sensitive:** Raw statements, invoices with PII, tax docs, identity docs live in `sensitive/` subfolders (statements/, invoices/, tax_docs/, identity/). Never commit; never use full account numbers in committed files.
- **Redaction:** In any markdown that is committed, use masked account IDs only (e.g. `Chase-****1234`). No full account numbers, SSN, or institution names in committed content.
- **ProjectIndex.md** is the central hub for navigation and “current focus” tasks; update it when processing inbox or after significant changes.
- **Projects:** One folder per initiative in `projects/` (e.g. subscription audit, debt payoff, tax-prep, big purchase). Each has `Status.md` and supporting docs.

### Inbox processing (finance)

Process and move into the right folder (transactions/, reports/, recurring/, statements/, invoices/, or sensitive/ subfolder for raw PII). Redact before committing any new markdown. Update ProjectIndex.md and reports as needed.

### Working with this repo

- Prefer local-only or self-hosted Git (e.g. Forgejo on NAS) for history and backup without putting financial data on GitHub/GitLab.
- When adding data: drop in inbox and ask AI to process, or place in the appropriate folder. Keep raw/PII in sensitive/ only.
