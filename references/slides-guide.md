# Slides Guide

## Purpose

`01-slides.md` defines the content, structure, and script of each class's visual presentation. It is both a **content specification** and a **visual creation brief**.

The slides file has two uses:
1. **As a script:** the mentor reads it to deliver the class.
2. **As a brief:** a visual designer or tool (e.g., Canva, PowerPoint) uses it to create the actual presentation file.

When possible, slides should be **created as actual visual artifacts** (e.g., via Canva), not just as Markdown scripts. See the "Slide creation" section below.

---

## 5E structure of a class's slides

Slides follow the 5E model. Each phase maps to specific slides:

| 5E Phase | Slide role | Typical position |
|----------|-----------|-----------------|
| **Engage** | Opening hook — a question, problem, or surprising fact | Slides 01–02 |
| **Explore** | Students attempt or observe something before the explanation | Slide 03 (or embedded in Engage) |
| **Explain** | Core content: concepts, definitions, examples, live demos | Slides 04–N-3 |
| **Elaborate** | Transition to exercises — instructions, context, connections | Slide N-2 |
| **Evaluate** | STEAM woman + closing + bridge to next class | Slides N-1, N |

**Rule:** Never open with a cold lecture slide. The first content slide must be an Engage hook — a question, analogy, or problem that creates a need for what is about to be taught.

---

## File header

Start every `01-slides.md` with a time distribution summary:

```
**Duración total:** 180 min
**Bloque de cátedra (Explain):** 50 min (slides 01–NN)
**Kahoot:** 15 min
**Pausa:** 10 min
**Práctica guiada (Elaborate):** 30 min
**Práctica autónoma:** 45 min
**Cierre (Evaluate):** 20 min
```

Adjust for classes with inspirational talks (see inspirational talk section below).

---

## Per-slide specification

Every slide must include these labeled fields:

```markdown
## Slide NN — [Short title]

- **5E Phase:** Engage / Explore / Explain / Elaborate / Evaluate
- **Bloom's level:** Remembering / Understanding / Applying / Analyzing / Evaluating / Creating
- **Visible content:** [What appears on screen — maximum 5 lines. Concise.]
- **Suggested layout:** [Optional: title+image, two columns, code block, etc.]
- **Speaker script:** [What the mentor says — complete sentences, natural tone.]
- **Board/demo instructions:** [Whiteboard diagrams or live platform demo, when applicable.]
- **Interaction:** [Question or micro-activity for students, when applicable.]
- **Estimated time:** N min
```

**Always required:** `Visible content`, `Speaker script`, `Estimated time`.
**Include when applicable:** `Board/demo instructions`, `Interaction`.
**Optional but recommended:** `Suggested layout`, `Bloom's level`, `5E Phase`.

---

## Mandatory slides in every class

Every class must include the following slides (matching the `slide-generator` type names):

| # | Type | Required content |
|---|------|------------------|
| 1 | `title` | Class number, title, **and poetic tagline** (see `tone-and-narrative-guide.md`). |
| 2 | `bridge` | "LO QUE YA SABES" (from previous class) + "LO QUE VIENE HOY" (today's content) in two columns. **Non-negotiable except for class 01.** This is the narrative connector between classes. |
| 3 | `engage` | A hook question or problem connected to students' experience. **Never a cold-lecture content slide.** |
| 4 | `objectives` | 3–5 learning objectives using Bloom's observable action verbs + **warm closing message** ("Si al final puedes hacer estas cuatro cosas, la clase fue exitosa"). |
| — | `analogy` | **At least one per class.** Concrete analogy from daily life (VIDA REAL ↔ TÉRMINO TÉCNICO) for the hardest concept. This is where the slide stops feeling like a textbook. |
| — | `manual-trace` (only for programming courses) | At least one variable-state tracing slide before the first `code` slide — UDL adaptation + pedagogical standard. |
| — | `steam` | The featured woman of the class. Second half of the lecture, before `closing`. Name, dates, area, context, explicit content connection. |
| — | `reflection` | Exercise 10 prompt (written reflection). **Non-negotiable.** Always present, always at the end of the Evaluate phase. |
| N-1 | `bridge` (forward) | "Lo que viene…" preview of next class. Closes the narrative loop. |
| last | `closing` | Three sections: `Hoy aprendimos` / `Próxima clase` / `Tarea`. |

For classes with inspirational talks (Clases 3, 5, 9 in standard Niñas Pro programs), also include a `plan-b` slide (hidden from regular flow, projected only if the guest cancels).

**Recommended additional types** (use when the content calls for them):
- `pull-quote` — a single poetic phrase on a colored background. Use to set up a concept or to break visual rhythm.
- `comparison` — "sin X / con X" or "antes / después" side by side. Useful for showing why the new technique matters.
- `anatomy` — break a structure into 4 labeled parts (e.g. parts of a function: TIPO RETORNO / NOMBRE / PARÁMETROS / RETORNO).
- `try-it` — "Inténtalo tú" invitation before the practice block. Warm transition, not a cold exercise list.

See `tone-and-narrative-guide.md` for the full rules on bridges, taglines, analogies, subtitles, and Chilean naming conventions. See `.agents/skills/skill-slide-generator/SKILL.md` for the parameter shape of each type.

---

## Visual design standards

- **High contrast.** Dark text on light background, or light text on dark background.
- **Low text density.** Maximum 5 lines of visible content per slide. Explanations belong in the speaker script, not on screen.
- **Inclusive imagery.** Represent diversity of gender, ethnicity, and body type. Use the image prompt guidelines in `references/visual-identity-guide.md`.
- **Code blocks.** Monospace font, dark background (`#1e1e1e`), light text (`#d4d4d4`). Minimum 18pt for projector use.
- **Diagrams.** Functional, not decorative. Each diagram must be explainable in one sentence.
- **Non-infantilizing aesthetic.** No cartoon characters, no pastel overload, no rounded fonts that signal "this is for children."

---

## Slide creation (beyond the Markdown script)

The `01-slides.md` file defines the content. For courses where a visual presentation is also needed:

- **Use Canva** when the Canva MCP connector is available. Generate a presentation using `generate-design` (design type: `presentation`) based on the content defined in `01-slides.md`. The outline review flow (`request-outline-review` → `generate-design-structured`) is the correct path for creating structured presentations.
- **Use PowerPoint or Google Slides** when Canva is not available. The `01-slides.md` file provides everything needed: visible content, layout suggestions, and image prompts.
- **Visual identity:** apply the colors, fonts, and logo defined in `visual-identity-guide.md`. If the Niñas Pro brand kit is available in Canva, use it.

When slides are created as visual artifacts, note the file path or Canva design URL in the class's `06-preparation-checklist.md`.

---

## Speaker script tone

- Direct, rigorous, and warm. Never condescending.
- Use "vamos a" not "van a aprender a" — signals joint work.
- When content is hard, name it: "Este concepto es exigente. Vamos paso a paso."
- Use specific acknowledgment, not empty praise: "Identificaste exactamente el error que tenías que encontrar."
- Use feminine forms as default: "la programadora", "las alumnas", "ella".
- Error normalization: "En este campo, todos los programas fallan antes de funcionar."

---

## Classes with inspirational talks

For classes where 60 minutes are given to an external guest:
- Compressed lecture: 30 minutes instead of 50.
- Include a clearly labeled section:
  ```
  ## [BLOQUE: CHARLA INSPIRACIONAL — 60 min]
  ```
  With facilitation notes: how to introduce the guest, Q&A management, closing.
- **Always include a Plan B:** what to do if the guest cannot attend (written at the end of the block, visible to the mentor).
- The STEAM woman slide serves as the warm-up for the talk.

---

## 5E phase → slide-generator types

When generating the actual `.pptx`, map each 5E phase to one of the available slide types from `.agents/skills/skill-slide-generator/SKILL.md`:

| 5E Phase | Slide types from the generator |
|----------|-------------------------------|
| **Engage** | `engage` (hook question — slide 02, immediately after `title`). |
| **Explore** | `activity`, `error-code`, `manual-trace` (students attempt or trace before being told). |
| **Explain** | `content`, `definition`, `pillars`, `code`, `flowchart`, `reference` (formal concept after exploration). |
| **Elaborate** | `activity`, `steps`, `code` applied to a new context (not repeating the demo). |
| **Evaluate** | `kahoot`, `steam`, `reflection`, `rubric`, `closing`. |

Structural slides (no 5E phase): `title`, `section` (chapter divider), `objectives`, `plan-b`.

The generator runs `validateSlideSequence` automatically and emits warnings if the sequence violates these rules (no Engage immediately after Title, no Objectives, no STEAM, no Reflection, STEAM after Closing, more than 5 visible lines on a content slide).

## Bloom's mapping guidance for slides

| Slide type | Bloom's level |
|------------|---------------|
| Hook question (Engage) | Remembering / Understanding |
| Concept definition | Understanding |
| Worked example | Applying |
| Error analysis / "What's wrong here?" | Analyzing |
| Design decision / "Which would you choose?" | Evaluating |
| Student creates their own example | Creating |

Include at least one slide at the Analyzing or higher level in every class.

---

## Valores de marca confirmados (del brandbook 2022)

No es necesario consultar el brandbook para slides. Usar estos valores directamente:

```
Fondo de slides título:      #6B32ED (púrpura)
Fondo slides contenido:      #FFFFFF (blanco) o #171929 (navy)
Fondo slides código:         #171929 (navy)
Texto principal:             #FFFFFF sobre colores oscuros
Texto sobre blanco:          #171929 (navy)
Acento 1:                    #FDCA36 (amarillo)
Acento 2:                    #2B88F7 (azul)
Acento 3:                    #05A175 (verde)

Fuente títulos:              Space Grotesk Bold (Google Fonts)
Fuente cuerpo:               Space Grotesk Regular (Google Fonts)
Fuente código:               Space Mono (Google Fonts)

Logo: siempre en esquina superior derecha, versión blanca sobre fondos oscuros
```

Ver `references/visual-identity-guide.md` para todos los valores, reglas de combinación y guías por tipo de slide.
