---
name: ninaspro-course-creator
description: "Use this skill when the user wants to create, redesign, structure, or adapt a complete course for Niñas Pro from a topic, syllabus, PDF, slide deck, class material, or course program. The skill creates a requirements summary, a main plan, and after explicit approval, a complete Markdown-only course package for girls and young women in Chile, typically ages 13–19."
---

# Niñas Pro Course Creator

## Purpose

This skill creates complete course packages for Niñas Pro. It can create a course from scratch or critically redesign a course from source material such as PDFs, slides, class notes, or a course program.

The skill instructions are written in English. All course outputs for learners and mentors must be written in Spanish.

## Core audience

Design by default for Niñas Pro: girls and young women in Chile, usually between 13 and 19 years old, in extracurricular learning contexts. Use clear, rigorous, warm, respectful, non-infantilizing Spanish. Refer to the teaching role as `mentora` unless the user requests another term.

## Non-negotiables

- Always conduct a requirements interview before creating any course files.
- Always create `course-requirements.md` and `main-plan.md` first.
- Always wait for explicit user approval before generating class materials.
- Never assume missing critical information — always ask.
- Do not generate initial or final evaluations; create only `assessment-inputs.md` for a separate evaluation skill.
- Generate Markdown outputs for all text files. Generate actual `.pptx` visual slides using the local `slide-generator` skill (see `.agents/skills/skill-slide-generator/SKILL.md`) — never just a Markdown brief. Read the slide-generator SKILL.md before coding the slides, use `buildClassSkeleton` as the starting point, and resolve every warning from `validateSlideSequence` before considering the class done.
- **Apply `references/tone-and-narrative-guide.md` to every class.** Empowering tone is non-negotiable: bridge slides connecting each class to the previous and next, poetic tagline on the cover, at least one human analogy per class, poetic subtitles, warm closing on objectives, real Chilean names in examples, code comments with personality. Validate against the reference example `Clase-09-Funciones.pptx` (project root) before declaring a class done.
- Deliver the final course as a compressed `.zip` folder.
- Use reliable sources only. Do not invent sources.
- Use APA 7 for all references.
- Include gender perspective transversally in all materials.
- Include one real, verifiable STEAM woman per class, selected for relevance to class content — not just by name recognition.
- Every class must include: slides (visual + script), Kahoot, exercises with rubric, glossary, STEAM woman, preparation checklist, and quality check.
- Keep narrative continuity between classes.

## Pedagogical frameworks (internal design tools)

Apply these three frameworks in every class. They are design tools — never explain them to students.

### 5E Model (primary class structure)
Every class follows: **Engage → Explore → Explain → Elaborate → Evaluate**.
- Never open with a cold lecture. Always open with an Engage hook.
- Explore before Explain: students attempt something before being given the answer.
- Elaborate = exercises applying content to new contexts (not repeating the example).
- Evaluate = Kahoot + Exercise 10 (written reflection, always present, non-negotiable).
Consult `references/pedagogical-frameworks-guide.md` for the full 5E mapping.

### Bloom's Revised Taxonomy (objective and exercise design)
- Learning objectives must use observable action verbs (implementar, identificar, diseñar — never "entender" or "conocer").
- Exercise levels map to Bloom's: calentamiento (Remembering/Understanding), práctica central (Applying/Analyzing), desafío (Evaluating), reflexión (Evaluating metacognitive).
- Kahoot difficulty maps to Bloom's: básico (Understanding), intermedio (Applying/Analyzing), avanzado (Evaluating).
Consult `references/pedagogical-frameworks-guide.md` for Bloom's level tables.

### UDL — Universal Design for Learning (accessibility)
Apply through specific design decisions, not generic statements:
- Dual instructions (oral + written) for every activity.
- Tarjeta de referencia (printed or displayed reference card) for complex or new syntax/notation. Specify which card per class.
- Three exercise levels so all students can participate regardless of pace.
- Manual tracing before coding in programming courses (UDL adaptation + pedagogical standard).
- Exercise 10 (written reflection) as an alternative expression path.
Consult `references/pedagogical-frameworks-guide.md` for the full UDL checklist.

## Technology is course-specific

Never assume a platform. The technology stack is captured in the interview and documented in `course-requirements.md`. Exercises and platform references must match what was agreed. Consult `references/technology-guide.md` for platform-specific guidance when the course uses a particular tool.

## Required workflow

### Step 1 — Requirements interview
Consult `references/interview-guide.md` for the full question list and source material handling.

### Step 2 — Create `course-requirements.md`
Consult `references/course-requirements-guide.md`.

### Step 3 — Create `main-plan.md`
Consult `references/main-plan-guide.md`.

### Step 4 — Ask for explicit approval
Do not create class folders until the user explicitly approves both planning documents.

### Step 5 — Generate full course package
After approval, generate all files class by class, in order. For each file type, consult its dedicated reference:

| File | Reference |
|------|-----------|
| `00-class-overview.md` | `references/course-output-guide.md` |
| `01-slides.md` (script + brief) | `references/slides-guide.md` |
| `01-slides.pptx` (visual artifact) | `references/slides-guide.md` + `.agents/skills/skill-slide-generator/SKILL.md` |
| `02-kahoot.md` | `references/kahoot-guide.md` |
| `03-exercises.md` | `references/exercises-guide.md` |
| `04-glossary.md` | `references/glossary-guide.md` |
| `05-steam-woman.md` | `references/steam-woman-guide.md` |
| `06-preparation-checklist.md` | `references/course-output-guide.md` |
| `07-quality-check.md` | `references/quality-guide.md` |
| `08-apuntes.md` | `references/apuntes-guide.md` |
| `facilitation-guide.md` | `references/facilitation-guide.md` |
| `assessment-inputs.md` | `references/assessment-inputs-guide.md` |
| `visual-identity-guide.md` | `references/visual-identity-guide.md` |
| `references.md` | `references/references-guide.md` |
| `full-glossary.md` | `references/glossary-guide.md` |

For pedagogical framework application in any file: `references/pedagogical-frameworks-guide.md`.
For tone, narrative continuity between classes, analogies, and warm language: `references/tone-and-narrative-guide.md`.
For student-facing reading material and worked examples: `references/apuntes-guide.md`.
For time distribution: `references/time-distribution-guide.md`.
For technology-specific exercise design: `references/technology-guide.md`.
For STEAM woman selection: `references/steam-woman-guide.md` + `references/steam-women-registry.md`.

## Final course folder structure

```text
course-name/
├── README.md
├── course-requirements.md
├── main-plan.md
├── facilitation-guide.md
├── full-glossary.md
├── references.md
├── assessment-inputs.md
├── visual-identity-guide.md
├── class-01/
│   ├── 00-class-overview.md
│   ├── 01-slides.md          ← script + visual creation brief
│   ├── 01-slides.pptx        ← visual artifact (generado con slide-generator)
│   ├── 02-kahoot.md
│   ├── 03-exercises.md
│   ├── 04-glossary.md
│   ├── 05-steam-woman.md
│   ├── 06-preparation-checklist.md
│   ├── 07-quality-check.md
│   └── 08-apuntes.md
└── class-n/
    └── ...
```

Special sessions (Bienvenida, Ceremonia de cierre) are included in `facilitation-guide.md` and `README.md` — they do not have their own class folders.
