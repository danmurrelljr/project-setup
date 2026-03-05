# Use case: Team Management

**id:** `team-management`

Workspace for a team's annual/master plan and ongoing management. For engineering managers (or similar) leading a remote or cross-functional team: strategy, roadmap, personnel context, meeting notes, and initiative deep-dives. The agent acts as "relentless organizer"—capturing unstructured notes and routing them into the right files with consistent structure and professional tone.

---

## Sensitive content hints (add to default)

- Personnel issues, performance concerns, political tactics, identifiable names in negative or confidential context. Strongly recommend **private**. Keep sensitive 1:1 content and manager-only notes in `sensitive/` so the repo can stay work-safe if ever shared with the team or leadership.

---

## Additional structure (layer on top of default folders)

**Folders (in addition to default):**

- `team/` — roster, member profiles, roles, stakeholders. Include `team/stakeholders.md` (or equivalent) for relationship maps and key collaborators.
- `platform/` — technical stack, infrastructure, environment maps (e.g. languages, services, staging/prod).
- `strategy/` — roadmap, retrospectives, and the annual master plan (e.g. `2026-master-plan.md` or `strategy/YYYY-master-plan.md`). Key objectives as checklist.
- `projects/` — deep-dive plans for high-priority initiatives (e.g. automation, release cadence, integrations); one doc or subfolder per initiative.
- `meetings/` — one-on-ones and team syncs. Two patterns:
  - **Monthly check-in:** `meetings/YYYY-MM-checkin.md` — snapshot of team progress, monthly themes, high-level goals; add "Team Progress" or "General Notes" as updates come in.
  - **Individual histories:** `meetings/[name].md` — long-term relationship and development tracking per team member; notes under monthly headers (e.g. `## 2026-01`).

*(Default `inbox/`, `archive/`, `sensitive/` already exist.)*

---

## Inbox processing default

1. List inbox; for each file, read and classify.
2. **Default timeline:** Unless a specific date is given, log under the **current date**.
3. **Tone & sanitization:** Rewrite profanity or insults into professional language; **preserve sentiment** (e.g. "creating unnecessary friction" not "being a jerk"; "pattern of critical errors" not harsh slang).
4. **Route:**
   - Team/personnel/stakeholder updates → `team/` or `team/stakeholders.md`; person-specific notes → append to `meetings/[name].md` under current month header.
   - Strategy/roadmap/objectives → `strategy/` or master plan file.
   - Initiative/project updates → `projects/` (relevant initiative doc).
   - Meeting takeaways / general progress → `meetings/YYYY-MM-checkin.md` (Team Progress or General Notes).
   - Sensitive personnel or political notes (manager-only) → `sensitive/`.
5. Move original to `archive/` (date-prefixed). Report what was processed.
6. Use clear H2/H3 headers (dates, topics, feedback) so future queries like "What did we discuss with X in November?" or "How has Y's feedback changed?" are answerable.

---

## README additions (folder table rows)

| `team/` | Roster, profiles, roles, stakeholders |
| `platform/` | Technical stack, infrastructure, environments |
| `strategy/` | Roadmap, retrospectives, annual master plan |
| `projects/` | Deep-dive plans for high-priority initiatives |
| `meetings/` | Monthly check-ins (YYYY-MM-checkin.md) and individual histories ([name].md) |

**Workflow:** Drop unstructured notes and updates in inbox; ask AI to organize into team/, strategy/, meetings/, or projects/. Monthly check-ins and per-person files stay current. Commit after milestones or on request; keep sensitive personnel content in sensitive/.

---

## AGENTS.md additions (append after base sections)

### Context (team management)

The user is a manager (e.g. engineering) for a team. This repo is the planning and execution workspace: annual objectives, technical context, personnel/relationship tracking, and meeting history. Keep sensitive personnel or political notes in sensitive/.

### Project structure (team management)

- `team/`: Roster, stakeholders, relationship maps.
- `platform/`: Tech stack, infrastructure, environment maps.
- `strategy/`: Roadmap, retrospectives, YYYY master plan with key objectives (checklist).
- `projects/`: Deep-dives for high-priority initiatives.
- `meetings/`: Monthly check-in files (`YYYY-MM-checkin.md`) and individual histories (`[name].md`) with chronological monthly headers.

### Information management

- **Unstructured input:** When the user provides notes, updates, or verbal comments, organize them immediately into the appropriate file. Default to **current date** unless specified.
- **Tone & sanitization:** Edit profanity or insults to professional language; preserve the underlying sentiment so context is not lost.
- **Retrieval:** Structure files with clear H2/H3 (Dates, Topics, Feedback) so the agent can answer "What did we discuss with [person] in [month]?" or "How has [person]'s feedback changed over time?"

### Commit protocol

Wait for significant milestones or explicit user request before pushing. Lets the user batch changes and review before sync.

### Agent hand-off

If the user works from multiple machines, a short "Agent hand-off" note (in README or AGENTS.md) can summarize: team name/context, key strategic pillars for the year, and where to find roster vs strategy vs meeting history. No need to name individuals in the repo; keep personnel nuance in meeting files or sensitive/.
