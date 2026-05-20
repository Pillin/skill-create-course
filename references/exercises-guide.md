# Exercises Guide

## Purpose

`03-exercises.md` is the Elaborate + Evaluate core of each class. It is where students apply, analyze, and evaluate — the three upper levels of Bloom's taxonomy that cannot happen during lecture.

---

## Minimum count

- **Minimum 10 exercises per class.**

---

## Four-level structure (Bloom's + 5E)

| Level | Exercises | Bloom's | 5E | Purpose |
|-------|-----------|---------|-----|---------|
| **Calentamiento** | 1–2 | Remembering / Understanding | Explore | Activate and check prior knowledge. Low stakes. ~5–10 min each. |
| **Práctica central** | 3–7 | Applying / Analyzing | Elaborate | Core skill practice. Progressive complexity. ~10–15 min each. |
| **Desafío** | 8–9 | Analyzing / Evaluating | Elaborate+ | For students who advance quickly. May require combining concepts. ~15 min each. |
| **Reflexión** | 10 | Evaluating (metacognitive) | Evaluate | Written individual reflection. Always last. Always present. ~8 min. **Non-negotiable.** |

**Exercise 10 is always a written reflection.** Never a coding exercise. Never optional. It is the Evaluate phase of the 5E model — it gives students (and mentors) a signal of where understanding is and where gaps remain.

---

## Per-exercise structure

```markdown
### Ejercicio NN — [Title] ([level])
- **Nivel:** Básico / Intermedio / Avanzado / Reflexivo
- **Bloom's:** Remembering / Understanding / Applying / Analyzing / Evaluating / Creating
- **Modalidad:** Individual / Pareja / Trío / Grupal
- **Tiempo sugerido:** NN min
- **Materiales:** [Only if non-digital]
- **Objetivo:** [Single pedagogical objective, one sentence]

#### Enunciado
[Exercise text. Clear and complete. Include input/output example if applicable.]

#### Entregable esperado
[What a correct or strong submission looks like]

#### Pistas opcionales
[1–3 hints the mentor can offer without giving away the solution]

#### Solución para la mentora
[Complete solution with comments]

#### Errores frecuentes
[2–3 most common mistakes and how to address them]
```

Required: `Nivel`, `Modalidad`, `Tiempo sugerido`, `Objetivo`, `Enunciado`, `Entregable esperado`, `Solución para la mentora`, `Errores frecuentes`.
Optional: `Bloom's` label (include when it adds clarity), `Materiales`, `Pistas opcionales`.

---

## 5E in exercise design

- **Calentamiento (Explore):** The student should be able to attempt this without the mentor's help. It confirms they can access the content just taught.
- **Práctica central (Elaborate):** Each exercise applies the concept in a slightly different context than the example from the lecture. Not a copy of the demo.
- **Desafío (Elaborate+):** Combines multiple concepts, requires the student to make a design decision, or handles an edge case.
- **Reflexión (Evaluate):** Prompt: what was hard, what was surprising, what question remains unanswered.

---

## Technology-agnostic exercise design

**Do not assume Dodona or any specific platform.** Design exercises that work regardless of the technology stack. Then annotate per-exercise how they are submitted:

- **With auto-judge platform (Dodona, OmegaUp, etc.):** include input/output format. Output must be deterministic. Add note if exercise is not compatible with the judge.
- **Without auto-judge:** exercises are submitted as code files, paper, or discussed in class. Specify the submission method in the enunciado or a note.
- **For non-code exercises** (pseudocode, diagrams, written reflection): always note explicitly: "Este ejercicio no requiere envío a [platform]. Se entrega en [papel / archivo de texto / discusión grupal]."

The technology used in the course is defined in `course-requirements.md`. Match the exercise submission notes to whatever the course actually uses.

---

## Programming exercise standards

- **Trace every code solution manually** with a concrete input before including it. Verify the output is exactly what you claim.
- **Include at least one exercise per class that requires manual tracing before coding.** This is both a UDL adaptation (reduces cognitive overload) and a pedagogical standard (builds algorithmic thinking before syntax).
- **Edge cases.** The Desafío exercises must test at least one edge case (empty input, single element, maximum value, etc.).

---

## UDL in exercise design

- **Three levels ensure all students engage.** No student is blocked (calentamiento is accessible to all), no student is bored (desafío is challenging for the fastest).
- **Self-paced retry on platform.** If the course uses an auto-judge platform, students can retry at their own pace — this is a UDL advantage. Never design exercises that penalize retrying.
- **Pair/individual choice.** Mark core exercises as individual but allow pairs if the student needs support. Mark explicitly when peer collaboration is the pedagogical design (not just support).
- **Written reflection accessibility.** Exercise 10 (written reflection) ensures students who struggle with the coding portion still have a way to demonstrate understanding of the concept.

---

## Formative rubric

End every `03-exercises.md` with a `## Rúbrica formativa de la clase` table:

| Nivel | Descripción | Puntaje |
|-------|-------------|---------|
| 1–2 | [Cannot access the basic task — foundational gap] | 1–2 |
| 3–4 | [Partial completion — can do calentamiento, gaps in práctica central] | 3–4 |
| 5–6 | [Completes core exercises correctly — Bloom's Applying level reached] | 5–6 |
| 7–8 | [Completes most exercises including some desafío — Analyzing level] | 7–8 |
| 9–10 | [Completes all exercises, handles edge cases, explains decisions — Evaluating level] | 9–10 |

The rubric is formative. It tells the student where she is. It is not a final grade.

---

## Classes with inspirational talks

Exercise 10 for these classes is always: "¿Qué fue lo más impactante de la charla? ¿Qué pregunta le harías a la invitada si tuvieras más tiempo?" This is the Evaluate phase of the inspirational talk — it closes the loop on what was heard.

---

## Peer review exercise

At least one exercise per course should be a structured peer review: a student reads and comments on another student's solution. Include specific reviewer prompts:
- ¿Tiene funciones / bloques bien separados?
- ¿Los nombres de variables son claros?
- ¿Hay algún caso borde no considerado?
- ¿Qué cambiarías?
