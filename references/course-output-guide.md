# Course Output Guide

## Purpose

Defines the generation sequence, the `00-class-overview.md` standard, the `README.md` standard, and the `06-preparation-checklist.md` standard.

---

## Generation sequence

1. **Root files:** `README.md`, `course-requirements.md`, `main-plan.md`, `facilitation-guide.md`, `visual-identity-guide.md`, `references.md`, `assessment-inputs.md`.
2. **Classes in order** (class-01 through class-n). Per class:
   a. `00-class-overview.md`
   b. `01-slides.md` (content script)
   c. `01-slides.pptx` (read `/mnt/skills/public/pptx/SKILL.md` first; apply Niñas Pro brandbook)
   d. `02-kahoot.md`
   e. `03-exercises.md`
   f. `04-glossary.md`
   g. `05-steam-woman.md`
   h. `06-preparation-checklist.md`
   i. `07-quality-check.md`
3. **`full-glossary.md`** — after all class glossaries exist.
4. **Compress** everything to `.zip` and present.

---

## `00-class-overview.md` standard

The map of the class. Mentors read this first. Required sections:

- **Propósito de la clase** — why this class exists in the course arc (one paragraph).
- **Conexión con la clase anterior** — explicit bridge from the previous session.
- **Conexión con la clase siguiente** — explicit bridge to the next session.
- **Objetivos de aprendizaje** — 3–5 objectives using Bloom's observable-action verbs. State the Bloom's level in parentheses after each: "Implementar ciclos `for` con variable de control (Apply — Bloom 3)."
- **Fases 5E de esta clase** — brief mapping of which class blocks correspond to which 5E phase.
- **Contenidos clave** — bulleted list of what is taught.
- **Actividad o producto principal** — the core exercise or project.
- **Tecnología y materiales** — what is needed.
- **Adaptaciones DUA** — specific UDL adaptations for this class (reference card topic, tracing exercise, etc.). Must be specific, not generic.
- **Enfoque de género transversal** — how gender perspective appears in this specific class.
- **Archivos de esta clase** — list of all 9 outputs (8 Markdown + 1 .pptx).

---

## `06-preparation-checklist.md` standard

Completed the day before the class. Required categories:

- **Materiales** — slides `.pptx` tested on projector, Kahoot loaded and PIN tested, exercises available on platform, reference cards printed or on screen.
- **Tecnología** — projector + laptop connection tested, platform access verified (not just assumed), `.pptx` speaker notes view tested.
- **Contenido** — mentor has read the full slides script, practiced the live demo, prepared extra examples for fast-moving groups.
- **Logística** — group size known, room setup, any special guest coordination.
- **Nota pedagógica** — one paragraph: what makes this class pedagogically challenging, what the mentor should watch for, tone notes.

For classes with inspirational talks: add a dedicated section confirming guest logistics and Plan B activity.

---

## `README.md` standard

Entry point for any mentor picking up the course. Required sections:

- **Descripción del paquete** — what this is and who it is for.
- **Estructura del paquete** — full folder tree with one-line descriptions. Include both `01-slides.md` and `01-slides.pptx` in each class listing.
- **Cómo usar este paquete** — steps: before the course, before each class, during, after.
- **Sesiones especiales** — notes on inspirational talk classes, ceremonies.
- **Tecnología requerida** — table: tool, use, access URL.
- **Notas importantes** — no evaluations, references file, glossary, language of materials.

---

## Naming conventions

- Folders: `class-01`, `class-02`, ..., `class-n` (zero-padded).
- Markdown files: `00-class-overview.md` through `07-quality-check.md` (zero-padded).
- PPTX file: `01-slides.pptx` (same number as the Markdown script).
- Root files: lowercase with hyphens, no spaces.
- ZIP name: `course-slug-ninaspro.zip`.

---

## Special sessions

Bienvenida (opening) and Ceremonia de cierre (closing) do not have class folders. Their facilitation content goes in `facilitation-guide.md` under clearly labeled sections. They appear in `README.md` as a note only.
