# Apuntes Guide

## Purpose

`08-apuntes.md` is the **complete written material** for each class. It is the document a student can read to learn the full topic on her own — before, during, or after the live session — without needing a mentor present.

The apuntes are not a summary or a cheat-sheet. They are the full theory of the class: every concept explained from scratch, with context, reasoning, analogies, and enough worked examples that a student who reads them carefully can understand and apply the content. Think of them as a textbook chapter for that specific class.

A student who missed class, or who wants to review, or who prefers reading over listening should be able to understand and use the content of this class by reading `08-apuntes.md` alone.

---

## Audience

Write directly to the student. Use "tú" throughout. Warm, clear, rigorous — not infantilizing. Same tone as the rest of the course materials (see `references/tone-and-narrative-guide.md`).

---

## Minimum structure

Every `08-apuntes.md` must include all seven sections below, in order. There are no optional sections.

---

### 1. Introducción — ¿De qué trata esta clase?

- 2–3 sentences connecting this class to the previous one and to the course arc.
- A single motivating question or real-world scenario that makes the topic feel necessary — why does this exist, and why does it matter to someone who codes?
- A brief roadmap: what will the student know by the end of reading this.

**Example opening pattern:**
> En la clase anterior aprendiste X. Hoy vas a descubrir Y — la herramienta que te permite hacer Z sin repetir código. Imagina que tienes que [concrete real-world scenario]. Al terminar de leer esta clase, vas a poder [concrete skill].

---

### 2. Conceptos clave — explicación completa

For **each major concept** taught in this class, write a full explanation — not a definition with a bullet list, but a real explanation that builds understanding from the ground up.

```markdown
## [Concept name]

[Full explanation of what this concept is and why it exists.
Start from what the student already knows, then build up to the new concept.
Be complete: if there is a prior concept required to understand this one, briefly re-explain it.
Minimum 2–3 paragraphs for each concept.]

**¿Por qué existe esto?**
[The motivation: what problem does this concept solve? What was hard or impossible without it?]

**Analogía:**
[A comparison to something familiar from daily life. Required. Must be specific, not generic.]

**Ejemplo trabajado — paso a paso:**
[A complete, worked example with step-by-step reasoning. Show every step. Explain why each step is necessary.
For code: annotated code block with a comment on each non-trivial line. Then trace the code manually with a concrete input and show the output.]

**Variantes y casos especiales:**
[Common variations of the concept, edge cases, or things that work differently than expected.
At least 2 variations or special cases per concept.]

**En resumen:**
[One sentence — what would you tell a friend about this concept?]
```

- Minimum 3 concepts per class, maximum 6.
- Each concept must have a full explanation, a motivation, an analogía, a worked example, and variants/edge cases. No exceptions.
- The analogía must connect to the student's everyday life, not a computer science scenario.
- For programming courses: every code block must be manually traced before inclusion. Verify the output matches what you claim. Never include unverified code.
- The explanation must be self-contained: do not say "as we saw in class" or "as the slides show." The apuntes are readable independently.

---

### 3. Errores frecuentes

A detailed walkthrough of 4–6 common mistakes, with explanation, example, and correction. Do not just list them — explain why each mistake happens and how to recognize it.

```markdown
## Error frecuente [N] — [Short name]

**¿Qué pasa?**
[Describe the mistake. What does the student do or write?]

**¿Por qué ocurre?**
[The cognitive or logical reason behind this mistake.]

**Ejemplo del error:**
[Show the mistake in context — code block, pseudocode, or written example.]

**Cómo corregirlo:**
[Full correction with explanation. Not just "use X instead" — explain why X works.]
```

---

### 4. Tarjeta de referencia rápida

A compact, scannable reference the student can keep visible while working. This is the UDL reference card for this class.

Format depends on course type:

- **Programming courses:** syntax reference with minimal examples.
- **Non-programming courses:** key terms, formulas, or steps in a scannable format.

```markdown
| Concepto / Sintaxis | Ejemplo mínimo | Para qué sirve |
|---------------------|----------------|----------------|
| ...                 | ...            | ...            |
```

Keep this section short and dense — it is a reference, not an explanation. All explanations go in section 2.

---

### 5. Ejemplos adicionales trabajados

Minimum **5 additional worked examples**, each in a different context from the ones in section 2. Every example must:

- Apply the concepts of this class in a realistic situation.
- Include the full solution with step-by-step reasoning — not just the answer.
- Be labeled with a difficulty level: Básico, Intermedio, or Avanzado.
- The set of 5 examples must cover all three difficulty levels.

```markdown
### Ejemplo [N] — [Short title] (Básico / Intermedio / Avanzado)

**Situación:**
[A realistic scenario that motivates this example. Use real Chilean names and contexts.]

**¿Qué necesitamos resolver?**
[State the problem clearly before solving it.]

**Solución, paso a paso:**
[Full walkthrough. For code: annotated code block, then a manual trace with a concrete input showing the output.]

**¿Qué aprendemos de este ejemplo?**
[One sentence: what is the takeaway or new insight this example adds?]
```

---

### 6. Preguntas de comprensión

5–7 questions a student can use to check her own understanding after reading. These are not exercises (those are in `03-exercises.md`) — they are comprehension prompts.

- Mix of factual questions ("¿Qué hace X?") and reasoning questions ("¿Por qué usarías X en lugar de Y?").
- Include answers at the end of the section so the student can self-check.
- Questions should cover all major concepts of the class.

```markdown
1. [Question]
2. [Question]
...

---
**Respuestas:**
1. [Answer]
2. [Answer]
...
```

---

### 7. Para explorar más

4–6 optional resources for students who want to go deeper. Must be:

- Real, verifiable, and accessible (no paywalls, no invented URLs).
- In Spanish when possible; if in English, mark it as `[En inglés]`.
- Described in 1–2 sentences so the student knows what to expect.
- Organized from easiest to most advanced.

```markdown
- [Resource name](URL) — [What the student will find there and why it is useful at this stage of the course.]
```

If a URL cannot be verified as real and working, do not include it. Leave the resource slot with:
`_[Recurso pendiente de verificación]_`

---

## What apuntes are NOT

- Not a transcript of the slides — the apuntes explain fully, in prose, what the slides only show visually.
- Not a list of exercise answers — solutions go in `03-exercises.md`.
- Not a glossary — terms go in `04-glossary.md`. Reference the glossary for definitions but do not duplicate it.
- Not a class summary — the full theory goes here, not a recap of what happened.

---

## Tone and narrative continuity

- Use real Chilean names in all examples (see `references/tone-and-narrative-guide.md`).
- The opening paragraph of each `08-apuntes.md` must reference the previous class explicitly.
- The closing line of each `08-apuntes.md` must hint at what comes next in the course.
- Write in active voice: "Python ejecuta…", "La función devuelve…", not "es ejecutado…" or "se devuelve…".
- Vary sentence length. Long explanatory sentences are fine, but break them with shorter ones so the reading pace stays engaging.

---

## Length

There is no upper word limit. The apuntes should be as long as the material requires. A class with 4 major concepts will have longer apuntes than a class with 2. Do not compress or omit content to keep the document short — completeness is the goal.

Minimum expected length: 1500–2500 words per class, not counting code blocks.

---

## Generation order

Generate `08-apuntes.md` after `01-slides.md` and before `02-kahoot.md`. The slides brief contains the concept list and worked examples — use them as the source of truth for what was actually taught. Do not invent concepts that are not in the slides. The apuntes expand and explain those concepts in full prose; they do not add new topics.
