---
id: creative-writing
name: Creative Writing (Fiction / KDP)
folders:
  - ideas/
  - drafts/
  - research/
  - assets/
  - published/
files:
  - ideas/_template.md
  - research/writing-voice.md
  - published/README.md
sensitive_hints:
  - Memoir content
  - Identifiable real people
---

# Use case: Creative Writing (Fiction / KDP)

---

## Sensitive content hints (add to default)

- Optional: if the user writes memoir or identifiable real people, suggest keeping early drafts or private notes in `sensitive/`. Otherwise default privacy is sufficient.

---

## Additional structure (layer on top of default folders)

**Folders (in addition to default):**

- `ideas/` — story seeds, raw concepts, brainstorming. Use a consistent template for new ideas (e.g. `ideas/_template.md`).
- `drafts/` — active story development; iterative drafts by project or title.
- `research/` — world-building, character profiles, reference notes. **Includes** `writing-voice.md`: generated and maintained by the agent from the user's writing; the agent creates it if missing, and regularly reviews and refines it based on drafts and new material.
- `assets/` — media: cover art, character illustrations, promotional materials.
- `published/` — finalized works ready for distribution. Include `published/README.md` as the catalog index (title, platform, link, date).

*(Default `inbox/`, `archive/`, `sensitive/` already exist.)*

---

## Inbox processing default

1. List inbox; for each file, read and classify.
2. **Route:**
   - Story fragments / concepts / seeds → move to `ideas/` using the idea template (title, premise, genre, notes). Create from template if one exists.
   - Research / voice notes / world-building → merge or add to `research/` (character/world docs). If the user describes their voice or style, use it to create or update `writing-voice.md`.
   - Media (images, art, promo) → move to `assets/` (optionally in subfolders by project).
   - Unclassified or mixed → summarize and place in `ideas/` or `research/` as best fit; move original to `archive/` with date prefix.
3. Move processed originals to `archive/` (date-prefixed). Report what was processed and suggest follow-ups (e.g. "Three new seeds in ideas/—consider expanding one into a draft").
4. After processing, update ProjectIndex.md.

---

## README additions (folder table rows)

| `ideas/` | Story seeds, concepts, brainstorming; use template for new entries |
| `drafts/` | Active story development and iterative drafts |
| `research/` | World-building, character profiles, references; writing-voice.md (agent-generated and refined from user's writing) |
| `assets/` | Cover art, illustrations, promotional materials |
| `published/` | Finalized works; published/README.md is the catalog index |

**Workflow:** Drop fragments and assets in inbox; ask AI to organize into ideas/ (with template), research/, or assets/. Develop seeds into drafts in drafts/. The AI generates and refines research/writing-voice.md from your writing; it reviews that file before generating new creative content and updates it as your style evolves. Keep published/README.md updated as works are completed.

**Vision (optional boilerplate):** This project collects scattered ideas and iteratively develops them into complete stories for self-publishing on platforms like Amazon KDP.

---

## AGENTS.md additions (append after base sections)

### Writing voice

- **Create if missing:** Generate `research/writing-voice.md` from the user's existing drafts, fragments, or a short sample they provide. Capture tone, style traits, and any explicit preferences (e.g. direct but reflective, conversational, curiosity-driven).
- **Review before generating:** Before generating any creative content, the agent must read `research/writing-voice.md` and match the documented voice.
- **Stylistic Guardrails:** Maintain a "Negative Constraints" section in `writing-voice.md` (e.g., "Avoid passive voice in action," "Never use 'suddenly' to resolve tension").
- **Refine regularly:** Periodically re-read the user's drafts and processed work; update writing-voice.md with new observations (sentence rhythm, vocabulary, dialogue style, etc.) so the voice doc stays aligned with their actual writing.

### Project structure (creative writing)

- `ideas/`: Story seeds and concepts; use `ideas/_template.md` (or equivalent) when adding from inbox.
- `drafts/`: Active development; one folder or file per story as the user prefers.
- `research/`: World-building, characters, references; contains writing-voice.md (agent-generated and refined from user's writing).
- `assets/`: Cover art, illustrations, promo.
- `published/`: Final works; `published/README.md` is the catalog index (title, platform, link, date).

### Agent workflow

1. **Organize:** Move fragments from inbox to ideas/ using the template; route research and assets to research/ and assets/.
2. **Develop:** Collaborate on expanding seeds from ideas/ into drafts in drafts/.
3. **Verify:** Check new writing against research/writing-voice.md before treating as final; update writing-voice.md when the user's writing reveals new style traits.
4. **Catalog:** When a work is published, add it to `published/README.md` and move final files into published/.

### Creating the idea template

If the user does not have one, suggest `ideas/_template.md` with fields such as: Title, Premise, Genre, Characters (brief), Notes, Date added. New inbox items that are story seeds get turned into idea files from this template.
