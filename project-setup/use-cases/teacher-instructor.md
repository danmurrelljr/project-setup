---
id: teacher-instructor
name: Teacher / Instructor
folders:
  - curriculum/
  - lessons/
  - materials/
  - assessments/
  - sensitive/students/
  - sensitive/grades/
files:
  - notes.md
sensitive_hints:
  - Student names
  - Grades
  - Attendance
  - Accommodations
  - Disciplinary notes
  - Parent communications
---

# Use case: Teacher / Instructor

Organize curriculum, lesson plans, materials, and assessments by course or term. Capture ideas and feedback in inbox; route to the right place. Student-identifiable data stays out of committed files.

---

## Sensitive content hints (add to default)

- Student names, grades, attendance, accommodations, disciplinary notes, parent communications. Keep in `sensitive/` (e.g. `sensitive/students/`, `sensitive/grades/`). Committed docs use anonymized or aggregate language only.
- **FERPA (US):** In the United States, student education records are protected under FERPA. Storing student-identifiable data — even in a local, private repo — may have compliance implications; consult your institution's policy before keeping any student records in this project. When in doubt, keep nothing student-identifiable outside `sensitive/`, and consider whether even `sensitive/` is the right place for official records.

---

## Additional structure (layer on top of default folders)

**Folders (in addition to default):**

- `curriculum/` — scope and sequence, learning objectives, by unit or term
- `lessons/` — lesson plans; optionally by term or course (e.g. `lessons/2026-spring/`)
- `materials/` — handouts, slides, activities (non-sensitive)
- `assessments/` — rubrics, exam questions, assignment templates
- `sensitive/students/` or `sensitive/grades/` — (optional subfolders) any student-identifiable data; never committed

**Top-level files:**

- `notes.md` — general running log; dated entries for unclassified ideas, feedback, or observations that don't fit a specific folder

*(Default `inbox/`, `archive/`, `sensitive/` already exist.)*

---

## Inbox processing default

1. List inbox; classify each item.
2. **Route:** Lesson ideas / fragments → `lessons/` or `curriculum/`; handout or activity → `materials/`; assessment idea → `assessments/`; student-specific or grade data → `sensitive/` (do not commit). General notes → append to a running log or `notes.md` with date.
3. Move originals to `archive/` (date-prefixed). Report what was processed.
4. Update ProjectIndex.md.

---

## README additions (folder table rows)

| `curriculum/` | Scope, sequence, learning objectives |
| `lessons/` | Lesson plans by term or course |
| `materials/` | Handouts, slides, activities |
| `assessments/` | Rubrics, exam questions, templates |
| `sensitive/students/` or `sensitive/grades/` | (If used) Student-identifiable data; gitignored |
| `notes.md` | General running log; dated unclassified notes |

**Workflow:** Drop ideas and feedback in inbox; AI routes to curriculum, lessons, materials, or assessments. Keep student data in sensitive/ only; committed docs stay anonymized/aggregate.

---

## AGENTS.md additions (append after base sections)

### Project structure (teaching)

- `curriculum/`, `lessons/`, `materials/`, `assessments/`, `notes.md`. Student data only in `sensitive/` subfolders; never in committed files.
- When referencing students in committed docs, use anonymized descriptions or aggregates (e.g. "one student requested…", "midterm average…").

### Working with this repo

- New term: duplicate or adapt lesson templates; update curriculum for the new scope.
- Before committing: confirm no student names, IDs, or identifiable performance data.
