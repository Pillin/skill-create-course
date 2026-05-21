# Tone and Narrative Guide

## Purpose

Defines the **empowering, warm, narratively-connected tone** that every Niñas Pro course must use. This is the difference between slides that are technically correct but feel cold, and slides that feel like a mentora who actually loves what she teaches.

When this guide is ignored, learners get bullet lists, dry definitions, and disconnected classes. When it's followed, they get a course that flows like a story and treats them as the smart young women they are.

**Reference benchmark:** the file `Clase-09-Funciones.pptx` at the project root is the visual-and-pedagogical north for what good looks like. Open it before generating any class.

---

## The five non-negotiables of empowering tone

### 1. Bridge between classes (always)
Every class (except class 01) opens with an **explicit two-column slide**: "LO QUE YA SABES" (from the previous class) on the left, "LO QUE VIENE HOY" on the right. This is the `bridge` slide type in the slide-generator. Never start a class with just the title — the bridge must be slide 02.

> Wrong: Title → Engage with no prior reference
> Right: Title → Bridge ("De clases anteriores: variables, if, ciclos…") → Engage

### 2. Poetic tagline on the cover
The `title` slide carries a tagline besides the class name. Not just "Funciones y modularidad" but "Funciones y modularidad — dividir para conquistar. Bloques de código con nombre propio."

The tagline must:
- Compress the central insight of the class into one memorable phrase.
- Use everyday language, no jargon.
- Feel like a chapter title in a novel, not a syllabus entry.

### 3. At least one analogy per hard concept
Every class introduces at least one new technical concept through a **human analogy**. Use the `analogy` slide type: a table with two columns — VIDA REAL on the left, TÉRMINO TÉCNICO on the right.

Examples that work:
- "Una función es como tu amiga Camila la barista. Tiene nombre, sabe hacer algo, le pides con info, te devuelve algo."
- "Un arreglo es como una fila de casilleros en el colegio. Cada uno tiene un número y guarda una cosa."
- "Un ciclo `while` es como esperar la micro: sigues mirando hasta que pasa."

This is where the slide stops feeling like a textbook and starts feeling like a person teaching.

### 4. Poetic subtitle on every slide
Every content slide has a title AND a one-line subtitle below it that connects emotionally or sets up the slide. Examples from the benchmark:
- Title: "Anatomía de una función" → Subtitle: "Cuatro partes. Cada una con su rol."
- Title: "Cómo llamar una función" → Subtitle: "Le pasas argumentos. Te devuelve un valor."
- Title: "Scope: dónde existe cada variable" → Subtitle: "Las variables de una función solo viven adentro."

The subtitle is never optional. If you can't write one, the slide isn't clear enough yet.

### 5. Warm closing on objectives
The `objectives` slide ends with a warm message of trust, not just a list of Bloom verbs. Example: "Si al final puedes hacer estas cuatro cosas, la clase fue exitosa."

This signals that success is defined and reachable — the student isn't being tested against a hidden bar.

---

## Concrete language patterns

### Names in examples
Use real Chilean names: **Camila, Valentina, Constanza, Antonia, Florencia, Catalina, Isidora, Javiera, Sofía, Emilia**. Never `nombre1`, `usuario`, `foo`, `bar`, `x`, `var1` for human-meaningful slots.

Code variables that represent humans get real names:
```cpp
string nombre = "Valentina";          // ✓
string saluda = "Camila la barista";  // ✓
string n1 = "x";                      // ✗
```

### Code comments with personality
Comments in code blocks should sound like a mentora explaining live, not a textbook. Examples from the benchmark:
- `// ← ¡repetido!`
- `// ❌ ERROR: no existe en main, solo en doblar`
- `// La función vive una sola vez`
- `// Con return i; ya no necesitamos break. ¡Más limpio!`

Never generic comments like `// hacer algo`, `// proceso`, `// inicializa variable`.

### Verbs and phrasing
| Avoid (cold) | Use (warm) |
|--------------|-----------|
| "Vamos a aprender X" | "Hoy vamos a descubrir cómo…" |
| "Definición de Y" | "¿Qué es Y? (con tus palabras)" |
| "Ejercicios" | "Inténtalo tú" |
| "Resuelve" | "Pruébalo / Diseña / Inventa" |
| "Esto es importante" | "Esto es el truco" |
| "Pregunta correcta/incorrecta" | "Acertaste / Casi, vamos de nuevo" |
| "¡Muy bien!" (vacío) | "Encontraste exactamente el error que tenías que encontrar" |
| "Los estudiantes" | "Las alumnas" / "ustedes" |

### Difficulty acknowledgment
When something is hard, name it directly. Don't pretend it's easy.
- "Este concepto es exigente. Vamos paso a paso."
- "Si esto no cuadra todavía, es normal. Lo retomamos."
- "Es la parte más difícil de la clase. Respira."

The opposite — "esto es muy fácil" — is condescending and corrosive.

---

## Closing bridge to next class (slide N-1 or N)

Every class closes with a `bridge` slide that previews the next class. Use the same `bridge` type but with `direction: "forward"`. Format: "Próxima clase: [tagline]. Trae lo de hoy bien fijado: [why today connects to tomorrow]."

Example: "Próxima clase: integración, todo junto. La clase 10 combina condicionales, ciclos, arreglos, vectores, búsqueda y FUNCIONES. Trae lo de hoy bien fijado — las funciones son la herramienta central de la próxima."

This closes the narrative loop and gives the student a thread to follow home.

---

## Validation checklist (run before declaring a class done)

- [ ] **Bridge backward present** (slide 02, except class 01).
- [ ] **Bridge forward present** (penultimate slide).
- [ ] **Title has poetic tagline** (not just class name).
- [ ] **At least one `analogy` slide** with VIDA REAL ↔ TÉRMINO TÉCNICO.
- [ ] **Every content slide has a subtitle** below the title.
- [ ] **Objectives slide ends with warm message** ("Si al final puedes…").
- [ ] **Code examples use Chilean names** (Camila/Valentina/etc.), not `foo`/`var1`.
- [ ] **Code comments have personality** (not generic "// inicializar").
- [ ] **No "¡Muy bien!" empty praise** — specific acknowledgment only.
- [ ] **Difficulty named directly** when applicable.
- [ ] **Opens with Engage** (not cold lecture) — handled by slide-generator validator.

If any item fails, the slide-generator's `.pptx` is technically valid but pedagogically incomplete.

---

## Reference example to model against

`Clase-09-Funciones.pptx` (project root) — 21 slides built by hand by the Niñas Pro team. Demonstrates every pattern above:
- Bridge backward (slide 03: "LO QUE YA SABES / LO QUE VIENE HOY")
- Pull-quote (slide 04: "Una función hace UNA cosa, y la hace bien")
- Analogy (slide 07: "Una función es como tu amiga. Camila la barista")
- Comparison (slides 08-09: "sin-funciones.cpp" vs "con-funcion.cpp")
- Anatomy (slide 10: 4 quadrants of a function)
- Try-it (slide 15: "INTÉNTALO TÚ. Antes de seguir, prueba tú.")
- Bridge forward (slide 20: "Próxima clase: integración, todo junto")
- Warm closing (slide 21: "¡Gracias! Nos vemos en Dodona.")

Open this file before any generation work. It is the standard.
