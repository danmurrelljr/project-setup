# Use case: Job Interviewing

**id:** `job-interviewing`

Organizing and preparing for job interviews: resume versions, cover letters, and interview prep materials by year and role.

---

## Sensitive content hints (add to default)

- Resume and cover letter content, company and role names, interview feedback, compensation discussions, performance notes, job IDs and URLs. Strongly recommend **private**; treat as employment/personal data.

---

## Additional structure (layer on top of default folders)

**Year-based organization:**

- `{YYYY}/` — e.g. `2025/`, `2026/` (historical vs current materials)
- `{YYYY}/resume/` — resume markdown; source of truth is `resume.md`; PDF generated on demand via AI or tool
- `{YYYY}/cover-letters/` — one file per role/company (e.g. `company-name.md`); keep `_template.md` for new letters
- `{YYYY}/{company}-{role-slug}-{job-id}/` — one folder per active interview (kebab-case)
- `{YYYY}/archive/` — move interview folders here when process ends (rejected, withdrawn, or completed) so only in-progress prep stays at top level

**Interview folder naming:** `{company}-{role-name-slug}-{job-id}/` (e.g. `apple-software-engineering-manager-200622462/`).

---

## Standard interview prep folder (when creating a new one)

**Required files:**

1. `job-details.md` — job description, requirements, responsibilities, qualifications, job ID, company, location, URL
2. `README.md` — role overview, key focus areas, preparation strategy, quick start
3. `AGENT_NOTES.md` — context for AI: role summary, key requirements, preparation focus
4. `preparation-notes.md` — checklist, research tasks, examples to prepare, questions to ask, interview-day checklist

**Optional (role-specific):** practice problems (`leetcode-practice.md`, `practice-solutions.py`), reference docs (`big-o-reference.md`), code practice folder.

---

## README additions (folder table rows)

| `{YYYY}/` | Materials for that year (resume, cover letters, interview prep) |
| `{YYYY}/resume/` | Resume markdown; PDF on demand |
| `{YYYY}/cover-letters/` | One file per role/company; use `_template.md` for new |
| `{YYYY}/{company}-{role}-{job-id}/` | One folder per active interview; standard files inside |
| `{YYYY}/archive/` | Completed/rejected/withdrawn interview folders |

**Workflow bullets:** New cover letter: copy `_template.md` to e.g. `company-name.md`. New interview: create folder with standard files; when done, move folder to `{YYYY}/archive/`.

---

## AGENTS.md additions (append after base sections)

### Repository structure (job interviewing)

- **Years:** `{YYYY}/` for historical and current materials.
- **Resume/cover letters:** Current year in `{YYYY}/resume/resume.md` and `{YYYY}/cover-letters/*.md`. New cover letter: copy `_template.md`, fill front matter and body. No export scripts in repo; generate PDF when needed via AI or markdown-to-PDF tool.
- **Interview folders:** One per active process in `{YYYY}/`, named `{company}-{role-slug}-{job-id}/`. When a process ends, move that folder into `{YYYY}/archive/`.

### Creating a new interview prep folder

1. Extract job details from posting (description, requirements, job ID, company, location).
2. Create the four standard files: `job-details.md`, `README.md`, `AGENT_NOTES.md`, `preparation-notes.md`.
3. Add role-specific materials (practice problems, code, references) as needed.
4. Update root docs if needed.

### Working with this repo

- **Interview prep:** Read the role’s `AGENT_NOTES.md`, then `job-details.md` and `preparation-notes.md`; use `README.md` for strategy.
- **Naming:** Kebab-case for folders and markdown files; code files follow language conventions.

### File naming

- Folders: `company-role-name-job-id/`
- Markdown: lowercase with hyphens (e.g. `job-details.md`, `preparation-notes.md`)
