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

Every class must include:
- **An Engage slide (Slide 01 or 02):** a hook question or problem connected to students' experience.
- **A live demo or exploration slide:** students see or attempt something before the full explanation.
- **A STEAM woman slide:** introduces the featured woman. Placed in the second half of the lecture (after Explain, before Elaborate). Includes: name, dates, area, country/context, and the explicit connection to today's content.
- **A closing slide:** names what was learned, and bridges explicitly to the next class.

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
