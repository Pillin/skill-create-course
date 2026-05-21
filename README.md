# skill-create-course · Niñas Pro

Skill para crear **cursos completos** para Niñas Pro (programación e introducción a la tecnología para niñas y adolescentes 13–19 años en Chile). Diseña paquetes pedagógicos completos a partir de un tema, syllabus, PDF de programa o materiales de clase.

---

## Qué hace esta skill

Genera, a partir de una conversación de requisitos, **todos los archivos de un curso** listos para usar:

- Plan global del curso (`main-plan.md`)
- Requisitos y decisiones (`course-requirements.md`)
- Para cada clase: overview, slides script, Kahoot de 11 preguntas, 10 ejercicios con rúbrica, glosario, perfil de mujer STEAM, checklist de preparación, verificación de calidad
- Guía de facilitación completa para la mentora
- Glosario consolidado del curso
- Bibliografía en APA 7
- Insumos para evaluación
- Guía de identidad visual

Todo el material se genera en español, con marco pedagógico **5E + Bloom + DUA** y **perspectiva de género transversal**.

---

## Cuándo usar esta skill

Invoca esta skill cuando alguien diga:

- "Crear un curso de X para Niñas Pro"
- "Diseñar un programa de 10 clases sobre Y"
- "Rediseñar pedagógicamente este curso/syllabus/PDF"
- "Generar el material de una clase"
- "Adaptar este material para Niñas Pro"

**No la uses** para:
- Evaluaciones formales (diagnóstico, final) — eso es una skill separada.
- Material que no sea Niñas Pro (el tono y la identidad visual son específicos).

---

## Cómo empieza el flujo

1. **Entrevista de requisitos.** La skill te hará preguntas sobre audiencia, duración, plataforma, tecnología, mujeres STEAM ya usadas. No omitas este paso.
2. **Generación de planificación.** Se crean `course-requirements.md` y `main-plan.md`.
3. **Aprobación explícita.** No se generan materiales de clase hasta que el usuario apruebe ambos documentos.
4. **Generación clase por clase.** Cada clase produce 8 archivos `.md` + un `create-slides.js` + un `slides.pptx` generado con `skill-slide-generator`.
5. **Cierre del paquete.** Glosario consolidado, referencias, README, ZIP final.

---

## Estructura de archivos de un curso

```
nombre-del-curso/
├── README.md
├── course-requirements.md
├── main-plan.md
├── facilitation-guide.md
├── full-glossary.md
├── references.md
├── assessment-inputs.md
├── visual-identity-guide.md
├── welcome/                  ← Sesión de bienvenida (ceremonia)
│   ├── 00-overview.md
│   ├── create-slides.js
│   └── slides.pptx
├── class-01/ … class-10/     ← 10 clases formativas
│   ├── 00-class-overview.md
│   ├── 01-slides.md
│   ├── 02-kahoot.md
│   ├── 03-exercises.md
│   ├── 04-glossary.md
│   ├── 05-steam-woman.md
│   ├── 06-preparation-checklist.md
│   ├── 07-quality-check.md
│   ├── create-slides.js
│   └── slides.pptx
└── demo-day/                 ← Ceremonia de cierre (Demo Day)
    ├── 00-overview.md
    ├── create-slides.js
    └── slides.pptx
```

---

## Reglas no-negociables (tono y pedagogía)

La skill las hace cumplir. Si quieres editarlas, son explícitas en las referencias:

1. **Tono empoderador.** Nombres chilenos en ejemplos (Camila, Valentina, Sofía…), nunca `foo`/`var1`. Subtítulos poéticos en cada slide. Comentarios de código con personalidad (`// ← ¡repetido!`).
2. **Continuidad narrativa entre clases.** Slide `bridge` backward (slide 02) conectando con la clase anterior. Slide `bridge` forward antes del cierre apuntando a la próxima.
3. **STEAM al inicio.** La Mujer STEAM va después de los objetivos, antes de la cátedra — es el contexto, no el epílogo.
4. **Modelo 5E sin atajos.** Engage → Explore → Explain → Elaborate → Evaluate. Nunca abrir con cátedra fría.
5. **Bloom verbos observables.** "Implementar", "Identificar", "Diseñar" — nunca "entender" o "conocer".
6. **DUA por adaptación concreta.** Cada clase nombra qué adaptación aplica (tarjeta de referencia, trazado manual, tres niveles de ejercicios).
7. **Sin material visible de "Bloom N".** Esa metadata va a las speaker notes para la mentora, no a la slide proyectada.
8. **Mínimo una analogía cálida por clase** (tipo `analogy` con tabla VIDA REAL ↔ TÉRMINO TÉCNICO).
9. **Ejercicio 10 = reflexión escrita en cuaderno.** No es slide proyectada — va al cuaderno de la alumna.
10. **Cierre cálido.** Tipo `farewell` (no `pull-quote` simple ni `closing` con 3 columnas con "Tarea").
11. **APA 7 con fuentes verificables.** Especialmente para los perfiles de mujeres STEAM. Nunca inventar citas.
12. **Sin charla = sin slide de transición Kahoot.** El Kahoot y la práctica de Dodona se anuncian verbalmente — no llevan slide propia.

Detalle completo en `references/tone-and-narrative-guide.md` y `references/pedagogical-frameworks-guide.md`.

---

## Cómo invocar la skill

Esta skill se carga automáticamente cuando hablas con Claude Code en un proyecto que la incluye en `.agents/skills/`. Para invocarla explícitamente:

```
"Usa skill-create-course para diseñar un curso de Python básico para Niñas Pro."
```

La skill leerá:
1. `SKILL.md` (instrucciones detalladas que Claude sigue)
2. Las referencias en `references/` según el archivo que esté generando

---

## Archivos de la skill

```
skill-create-course/
├── README.md                              ← este archivo
├── SKILL.md                               ← instrucciones para Claude
└── references/
    ├── tone-and-narrative-guide.md        ← TONO empoderador, conector entre clases, analogías
    ├── pedagogical-frameworks-guide.md    ← 5E + Bloom + DUA aplicados
    ├── interview-guide.md                 ← preguntas iniciales obligatorias
    ├── course-requirements-guide.md       ← formato course-requirements.md
    ├── main-plan-guide.md                 ← formato main-plan.md
    ├── course-output-guide.md             ← formato 00-class-overview, README, prep checklist
    ├── slides-guide.md                    ← formato 01-slides.md + mapeo 5E → tipos de slide
    ├── kahoot-guide.md                    ← formato 02-kahoot.md (11 preguntas, mix Bloom)
    ├── exercises-guide.md                 ← formato 03-exercises.md (10 ej, 4 niveles, rúbrica)
    ├── glossary-guide.md                  ← formato 04-glossary.md y full-glossary.md
    ├── steam-woman-guide.md               ← formato 05-steam-woman.md (selección + perfil)
    ├── steam-women-registry.md            ← registro de mujeres ya usadas en cursos previos
    ├── quality-guide.md                   ← formato 07-quality-check.md
    ├── facilitation-guide.md              ← formato facilitation-guide.md raíz
    ├── visual-identity-guide.md           ← Brandbook Niñas Pro 2022 aplicado
    ├── references-guide.md                ← formato references.md (APA 7)
    ├── assessment-inputs-guide.md         ← formato assessment-inputs.md (handoff a skill eval)
    ├── technology-guide.md                ← guía por plataforma (Dodona, Replit, OmegaUp)
    ├── time-distribution-guide.md         ← distribuciones estándar (clase, charla, ceremonias)
    └── lessons-learned.md                 ← decisiones, correcciones y aprendizajes acumulados
```

---

## Integración con otras skills

| Skill | Rol |
|-------|-----|
| `skill-slide-generator` | Genera el `.pptx` real desde `create-slides.js`. Esta skill lo invoca al final de cada clase. |
| *(skill de evaluación)* | Skill separada. Esta skill produce `assessment-inputs.md` como handoff. |

---

## Benchmark de calidad

El archivo `Clase-09-Funciones.pptx` (en la raíz del repo del curso) es el norte visual y pedagógico de cómo deben verse las slides. Antes de declarar un curso terminado, validar que las clases tengan calidad equivalente.

---

## Cuando algo cambia

Si el curso ya se generó y luego cambia algo (un tema, un Mujer STEAM, una tecnología), regenera solo los archivos afectados — no rehacer el paquete completo. La skill mantiene la continuidad narrativa siempre que respetes el `main-plan.md`.

---

## Fuente primaria

- **Brandbook Niñas Pro 2022** — `Brandbook Niñas Pro 2022.pdf` en la raíz del repo del curso.
- **Marcos pedagógicos** — BSCS 5E (Bybee 2006), Bloom revisado (Anderson & Krathwohl 2001), UDL 2.2 (CAST 2018).
