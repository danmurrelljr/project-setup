# Use cases

Use case docs extend the base project-setup. Each file is a diff: only what to add or change for that use case.

| id | Description |
|----|-------------|
| job-interviewing | Job interview prep: resume/cover letters by year, interview folders per role, standard prep files |
| personal-finance | Personal finance tracking: statements, transactions, budget, reports; sensitive/ subfolders; redact account numbers in committed files |
| career-management | Career strategy hub: goals, leadership portfolio (STAR), political navigation, transition plan; inbox routes to core docs; keep separate from work repos |
| creative-writing | Fiction/KDP: Ideas, Drafts, Research (Writing_Voice.md agent-generated and refined from user's writing), Assets, Published catalog; inbox → template-based Ideas |
| team-management | Team planning & management: team/, platform/, strategy/, projects/, meetings/ (monthly check-ins + per-person histories); sanitize tone; sensitive/ for personnel-only notes |
| teacher-instructor | Curriculum, lessons, materials, assessments; student data in sensitive/ only; anonymized in committed docs |
| product-manager | Roadmap, requirements/PRDs, backlog, stakeholders, metrics; confidential strategy in sensitive/ |
| product-designer-research | Research, personas, prototypes, findings; participant PII in sensitive/; anonymized quotes in committed docs |
| executive-assistant | Meetings, travel, tasks, contacts, templates; exec calendar/PII in sensitive/; work-safe summaries only in repo |
| recruiter | Roles, pipeline, process/templates; candidates and interview feedback in sensitive/ only; no PII in committed docs |
| project-manager | Delivery: projects/, status/, risks/, deliverables/, stakeholders/; inbox → status and risk register |
| research-knowledge | Sources, literature notes, drafts, citations; raw data and human-subject info in sensitive/ only |
| marketing | Campaigns, content calendar, assets, metrics; unreleased strategy in sensitive/ |

**Usage:** When the user picks a use case during setup, read `use-cases/{id}.md` and merge its content with the base scaffold (additional folders/structure, README rows, AGENTS.md sections, sensitive-content hints).
