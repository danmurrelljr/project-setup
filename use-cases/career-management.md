# Use case: Career Management

**id:** `career-management`

Private hub for career strategy, leadership portfolio, and professional development. Kept separate from work repos for a "work-safe" boundary while maintaining a high-fidelity record of impact and long-term goals. AI acts as career strategist: challenge the user to refine outcomes, identify gaps, suggest high-leverage activities.

---

## Sensitive content hints (add to default)

- Compensation, confidential 1:1 notes, identifiable stakeholder details that could link back to a specific employer. Strongly recommend **private**. Never reference `sensitive/` contents in committed docs or assume they exist on other machines.

---

## Additional structure (layer on top of default folders)

**Core files (top-level):**

- `goals.md` — professional objectives and milestones (e.g. by year)
- `leadership-portfolio.md` — "brag sheet"; evidence base for promotions or job search. Use **STAR** (Situation, Task, Action, Result) and measurable outcomes, not just activities
- `political-navigation-guide.md` — stakeholder map, influence patterns, risk mitigation (the "room as it is")
- `transition-plan.md` — exit/pivot strategy; handoff, must-knows, landmines. Living document, milestone-driven
- `notes.md` — (optional) running log or "inbox digest" for general/unclassified career notes

**Folders (in addition to default):**

- `presentations/` — archival of personal intellectual property (e.g. talks, AI Office Hours)

*(Default `inbox/`, `archive/`, `sensitive/` already exist.)*

---

## Inbox processing default

1. List inbox; for each file, read and classify.
2. **Route:**
   - Accomplishments / metrics → merge into `leadership-portfolio.md` (STAR, measurable outcomes; convert activities into results)
   - Goals / milestones → add or align with `goals.md`
   - Stakeholder / political notes → merge into `political-navigation-guide.md` or `transition-plan.md` (relationships, tactics, risks)
   - Transition / handoff / operational → merge into `transition-plan.md`
   - Personal projects / side work → `leadership-portfolio.md` or `goals.md`; or `projects.md` if present
   - General / unclassified → append to `notes.md` (or a "Career notes" section) with date and summary
3. Move original to `archive/` (date-prefixed) or `sensitive/` if confidential. Report what was processed and any suggested follow-ups.
4. When merging, preserve existing structure; add a short note if content is ambiguous (e.g. "[Inbox YYYY-MM-DD: verify metric before resume use]").

---

## README additions (folder table rows)

| `goals.md` | Professional objectives and milestones |
| `leadership-portfolio.md` | Brag sheet; STAR-formatted outcomes |
| `political-navigation-guide.md` | Stakeholder map, influence, risks |
| `transition-plan.md` | Exit/pivot strategy, handoff, must-knows |
| `notes.md` | General career notes, inbox digest |
| `presentations/` | Archival of personal IP (talks, etc.) |

**Workflow:** Drop meeting takeaways and ideas in inbox; ask AI to process into the right doc. Keep portfolio and transition plan current. Prefer local-only or private remote; do not link this repo to work repos via paths or submodules.

---

## AGENTS.md additions (append after base sections)

### Core principles

1. **Impact tracking:** Capture measurable outcomes, not just activities. Convert "I built X" into "I achieved Y result (metric)."
2. **Political navigation:** Document the landscape as it is—stakeholders, influence, risks.
3. **Transition readiness:** Keep `transition-plan.md` as a living document, not reactive.
4. **AI as strategist:** Challenge the user to refine the brag sheet, close gaps in goals, and suggest high-leverage activities.

### Project structure (career management)

- Core docs: `goals.md`, `leadership-portfolio.md`, `political-navigation-guide.md`, `transition-plan.md`. Optional: `notes.md`, `projects.md`.
- `presentations/` for personal IP. Inbox/archive/sensitive per default.
- **Constraint:** Do not link this repo to work repos via hard paths or git submodules. Keep "work-safe" vs "personal career" separation.

### Working with this repo

- **New machine:** Clone; optionally `mkdir sensitive` for local-only materials. Inbox processing as usual.
- **Monthly:** Suggest a "Career check-in"—biggest win, political challenge navigated.
- **Relationships:** Treat as assets; track last contact with key stakeholders.
- **Narrative:** Help move from "Manager" to "Strategic Leader" in how outcomes are framed.

### Optional initialization prompts

When starting or auditing: (1) Review `leadership-portfolio.md`—are entries results or just activities? (2) Cross-reference with work goals if the user has a separate work repo (without hard-linking). (3) Update stakeholder map (Blockers, Champions, Neutral). (4) Capture career-relevant 1:1 wins here, not in the work repo.
