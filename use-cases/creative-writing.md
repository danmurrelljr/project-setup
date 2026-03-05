# Use case: Creative Writing (Fiction / KDP)

**id:** `creative-writing`

Collect, organize, and develop story ideas into finished works for self-publishing (e.g. Amazon KDP). Inbox receives fragments and assets; AI helps move them into structured folders, expand seeds into drafts, and keep voice and catalog consistent.

---

## Sensitive content hints (add to default)

- Optional: if the user writes memoir or identifiable real people, suggest keeping early drafts or private notes in `sensitive/`. Otherwise default privacy is sufficient.

---

## Additional structure (layer on top of default folders)

**Folders (in addition to default):**

- `Ideas/` — story seeds, raw concepts, brainstorming. Use a consistent template for new ideas (e.g. `Ideas/_template.md`).
- `Drafts/` — active story development; iterative drafts by project or title.
- `Research/` — world-building, character profiles, reference notes. **Includes** `Writing_Voice.md`: generated and maintained by the agent from the user's writing; the agent creates it if missing, and regularly reviews and refines it based on drafts and new material.
- `Assets/` — media: cover art, character illustrations, promotional materials.
- `Published/` — finalized works ready for distribution. Include `Published/README.md` as the catalog index (title, platform, link, date).

*(Default `inbox/`, `archive/`, `sensitive/` already exist.)*

---

## Inbox processing default

1. List inbox; for each file, read and classify.
2. **Route:**
   - Story fragments / concepts / seeds → move to `Ideas/` using the idea template (title, premise, genre, notes). Create from template if one exists.
   - Research / voice notes / world-building → merge or add to `Research/` (character/world docs). If the user describes their voice or style, use it to create or update `Writing_Voice.md`.
   - Media (images, art, promo) → move to `Assets/` (optionally in subfolders by project).
   - Unclassified or mixed → summarize and place in `Ideas/` or `Research/` as best fit; move original to `archive/` with date prefix.
3. Move processed originals to `archive/` (date-prefixed). Report what was processed and suggest follow-ups (e.g. "Three new seeds in Ideas/—consider expanding one into a draft").
4. After processing, update ProjectIndex.md.

---

## README additions (folder table rows)

| `Ideas/` | Story seeds, concepts, brainstorming; use template for new entries |
| `Drafts/` | Active story development and iterative drafts |
| `Research/` | World-building, character profiles, references; Writing_Voice.md (agent-generated and refined from user's writing) |
| `Assets/` | Cover art, illustrations, promotional materials |
| `Published/` | Finalized works; Published/README.md is the catalog index |

**Workflow:** Drop fragments and assets in inbox; ask AI to organize into Ideas/ (with template), Research/, or Assets/. Develop seeds into drafts in Drafts/. The AI generates and refines Research/Writing_Voice.md from your writing; it reviews that file before generating new creative content and updates it as your style evolves. Keep Published/README.md updated as works are completed.

**Vision (optional boilerplate):** This project collects scattered ideas and iteratively develops them into complete stories for self-publishing on platforms like Amazon KDP.

---

## AGENTS.md additions (append after base sections)

### Writing voice

- **Create if missing:** Generate `Research/Writing_Voice.md` from the user's existing drafts, fragments, or a short sample they provide. Capture tone, style traits, and any explicit preferences (e.g. direct but reflective, conversational, curiosity-driven).
- **Review before generating:** Before generating any creative content, the agent must read `Research/Writing_Voice.md` and match the documented voice.
- **Refine regularly:** Periodically re-read the user's drafts and published work; update Writing_Voice.md with new observations (sentence rhythm, vocabulary, dialogue style, etc.) so the voice doc stays aligned with their actual writing.

### Project structure (creative writing)

- `Ideas/`: Story seeds and concepts; use `Ideas/_template.md` (or equivalent) when adding from inbox.
- `Drafts/`: Active development; one folder or file per story as the user prefers.
- `Research/`: World-building, characters, references; contains Writing_Voice.md (agent-generated and refined from user's writing).
- `Assets/`: Cover art, illustrations, promo.
- `Published/`: Final works; `Published/README.md` is the catalog index (title, platform, link, date).

### Agent workflow

1. **Organize:** Move fragments from inbox to Ideas/ using the template; route research and assets to Research/ and Assets/.
2. **Develop:** Collaborate on expanding seeds from Ideas/ into drafts in Drafts/.
3. **Verify:** Check new writing against Research/Writing_Voice.md before treating as final; update Writing_Voice.md when the user's writing reveals new style traits.
4. **Catalog:** When a work is published, add it to `Published/README.md` and move final files into Published/.

### Creating the idea template

If the user does not have one, suggest `Ideas/_template.md` with fields such as: Title, Premise, Genre, Characters (brief), Notes, Date added. New inbox items that are story seeds get turned into idea files from this template.
