# Pedagogical Frameworks Guide

## Purpose

Defines how the three core pedagogical frameworks — 5E, Bloom's Revised Taxonomy, and UDL — are applied in every Niñas Pro course. These are internal design tools, not content to teach to students. Every class file must reflect these frameworks, even if they are never mentioned by name in the materials.

---

## 1. The 5E Model (primary structure)

The 5E model (Engage → Explore → Explain → Elaborate → Evaluate) defines the sequence of every class. Each phase has a clear purpose and maps to specific blocks in the session.

| Phase | Purpose | Maps to |
|-------|---------|---------|
| **Engage** | Activate prior knowledge. Create a need or question. Make students curious. | Apertura (10 min) |
| **Explore** | Students investigate before being told the answer. Guided discovery, not passive reception. | Práctica guiada inicial / demo interactiva |
| **Explain** | Formalize and name what was discovered. Introduce vocabulary and structure. | Cátedra / slides (50 min or compressed) |
| **Elaborate** | Apply to new, more complex, or unfamiliar contexts. Transfer. | Ejercicios en plataforma o papel (práctica autónoma) |
| **Evaluate** | Check understanding. Identify gaps. Self-assessment and peer feedback. | Kahoot + ejercicio de reflexión (Exercise 10) |

### 5E in practice

- **Engage before Explain.** Do not open the lecture block immediately. Always open with a question, problem, or activation that creates a need for the content. Example: "¿Cuánto tiempo tomaría escribir los números del 1 al 100 a mano?" before introducing loops.
- **Explore is not always a full activity.** In a 50-minute lecture it might be 5–8 minutes of students attempting something before being shown the answer. The key is that students construct meaning before receiving it.
- **Elaborate ≠ more examples.** Elaborate means applying to a new context, not repeating the same type of problem. Exercise levels 3–7 (práctica central) are Elaborate. Exercises 8–9 (desafío) are deep Elaborate.
- **Evaluate is not only Kahoot.** The formative rubric, peer review exercises, and Exercise 10 (written reflection) are all Evaluate phases.

### 5E and classes with inspirational talks

For classes where 60 minutes are given to a guest:
- Engage and Explore are compressed or embedded in the first 30-minute lecture.
- The inspirational talk functions as an extended Elaborate/Engage hybrid: it shows the content in a real professional context.
- Evaluate (Kahoot + reflection on the talk) follows the talk.

---

## 2. Bloom's Revised Taxonomy (objective design)

Bloom's revised taxonomy defines the cognitive level of every learning objective, exercise, and Kahoot question.

| Level | Action verbs | Use in this skill |
|-------|-------------|-------------------|
| **Remembering** | Identify, name, list, recall | Warm-up exercises, basic Kahoot questions |
| **Understanding** | Explain, describe, paraphrase, classify | Intermediate Kahoot, glossary definitions |
| **Applying** | Use, implement, execute, solve | Práctica central exercises (3–7) |
| **Analyzing** | Compare, differentiate, trace, debug | Challenge exercises (8–9), peer review |
| **Evaluating** | Justify, critique, assess, decide | Code review, design decisions, reflection |
| **Creating** | Design, construct, produce, develop | Integrating exercises, final Demo Day project |

### Bloom's in practice

- **Learning objectives must use Bloom's action verbs.** Never write "understand" or "know" — these are not observable. Write "implementar", "identificar", "diseñar", "comparar".
- **Kahoot difficulty levels map to Bloom's:**
  - Básico → Remembering / Understanding
  - Intermedio → Applying / Analyzing
  - Avanzado → Evaluating / Creating
- **Exercise level progression maps to Bloom's:**
  - Calentamiento → Remembering / Understanding
  - Práctica central → Applying
  - Desafío → Analyzing / Evaluating
  - Reflexión → Evaluating (metacognitive)
- **The course arc follows Bloom's.** Early classes (C01–C03) live in Remembering/Understanding/Applying. Mid-course (C04–C07) adds Analyzing. Late course (C08–C10) reaches Evaluating and early Creating.

---

## 3. Universal Design for Learning (UDL) — practical application

UDL ensures every student can access and engage with the course regardless of learning differences. Apply it through specific design decisions, not generic statements.

### Three UDL principles and how they appear in this skill

**Multiple means of representation** (how information is presented):
- Every instruction is given both verbally and in writing.
- Code examples are shown on screen AND traced on the whiteboard.
- Key reference material is available as a **tarjeta de referencia** (printed or displayed card): syntax tables, diagram symbol guides, operator tables. Specify which card is needed per class in `06-preparation-checklist.md`.
- Abstract concepts are illustrated with analogies in the glossary and slides.

**Multiple means of action and expression** (how students engage and respond):
- Exercises have three difficulty levels: all students participate, none are blocked.
- Platform-based practice (auto-judge platforms like Dodona, or any online tool) allows self-paced retry — never remove this advantage.
- Written reflection (Exercise 10) gives students who struggle with coding a way to demonstrate understanding.
- Pair and individual exercise modes are both available.

**Multiple means of engagement** (how students are motivated):
- Every class connects content to a real STEAM woman whose work uses that content professionally.
- Every class opens with a question that connects to students' own experience.
- Inspirational talk classes (if any) provide a live professional model.
- The error is normalized: "En programación, todos los programas fallan antes de funcionar."

### UDL adaptations to specify per class

In `00-class-overview.md` and `06-preparation-checklist.md`, name the concrete adaptation for that class — not just "apply UDL." Examples:
- "Se entrega tarjeta de referencia con los símbolos del diagrama de flujo."
- "Los ejercicios de código incluyen el paso de trazado manual antes de codificar."
- "El tiempo del Kahoot se ajusta para dar margen a lectoras más lentas."
- "Las instrucciones del ejercicio están disponibles en pantalla durante toda la práctica."

---

## Frameworks combined: a class-level checklist

Before finalizing any class file, verify:

- [ ] **5E — Engage:** The class opens with a question or problem that creates a need for the content. No cold lecture start.
- [ ] **5E — Explore:** Students attempt something before being shown the full answer.
- [ ] **5E — Explain:** Concepts are formalized with vocabulary after exploration.
- [ ] **5E — Elaborate:** Exercises apply content to new contexts (not just repeat the example).
- [ ] **5E — Evaluate:** Kahoot + reflection cover what students learned and where gaps remain.
- [ ] **Bloom's:** Objectives use observable action verbs at the right cognitive level.
- [ ] **Bloom's:** Exercise levels progress from Remembering to Evaluating.
- [ ] **Bloom's:** Kahoot difficulty distribution matches the Bloom's levels.
- [ ] **UDL — Representation:** Dual instructions (oral + written), reference card specified if needed.
- [ ] **UDL — Action/Expression:** Three exercise levels present, self-paced practice available.
- [ ] **UDL — Engagement:** STEAM woman integrated, real-life connection in the opening.
