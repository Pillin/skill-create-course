# Glossary Guide

## Purpose

There are two glossary files: `04-glossary.md` (per class) and `full-glossary.md` (root level, consolidated). Both serve different audiences. The class glossary is for students during the class. The full glossary is for mentors as a reference across the entire course.

---

## `04-glossary.md` — per class

### Minimum count
- **Minimum 8–10 terms per class.**

### Term selection
- Select only terms that were actually taught in that class.
- Do not include terms from previous or future classes unless they are directly reused.
- Prioritize terms that students commonly confuse or misuse.

### Per-term structure

```
## [Term] (or `[term]` for code tokens)
- **Nivel:** Básico / Intermedio / Avanzado
- **Definición simple:** 1–2 sentences. No jargon. Accessible to a 13-year-old.
- **Ejemplo:** A concrete, minimal example. Code block if applicable.
- **Analogía:** Optional but recommended. A comparison to something familiar.
- **Errores comunes:** 1–2 most common misuses or confusions.
```

All fields required except Analogía (include it whenever it genuinely helps — omit it if it would be forced).

---

## `full-glossary.md` — consolidated root file

### Format
- Alphabetical order.
- Each term entry: term in `##` heading, followed by a one-paragraph definition in plain prose.
- Each entry includes a **class reference tag** in parentheses: `(C01)`, `(C05)`, etc. For terms introduced in multiple classes, list all: `(C03, C04)`.
- No tables. No per-field structure. Just readable prose per term.

### Content
- All terms from all class glossaries, deduplicated.
- When the same term appears in multiple classes with slightly different definitions, write a single unified definition that covers all uses.
- Abbreviations and code tokens are written in backticks.

### Example entry
```
## Acumulador (C05)
Variable que empieza en un valor neutro (0 para suma, 1 para producto) y acumula resultados en cada iteración de un bucle. Por ejemplo: `int suma = 0; for(...) suma += i;`
```

---

## Generation order

Generate `04-glossary.md` files during class generation. Generate `full-glossary.md` last, after all class glossaries exist, by consolidating them.
