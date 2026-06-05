# Lessons Learned

## Purpose

Captures decisions, corrections, and insights from real course creation sessions. Updated after every completed course. Consult before starting a new course of the same type.

---

## Programación Competitiva Básico en C++ (2026)

### Time distribution
"1.5h cátedra y 1.5h ejercicios con 15 min de Kahoot" means the Kahoot is carved from the 3 hours, not added on top. The resulting distribution: 10 min apertura + 50 min cátedra + 15 min Kahoot + 10 min pausa + 30 min práctica guiada + 45 min Dodona + 20 min cierre = 180 min. Always confirm this explicitly.

### Manual tracing (trazado manual) as accessibility tool
For any programming course, manual tracing before coding is both a pedagogical tool and an accessibility adaptation. Name it explicitly in exercises and in the facilitation guide — do not leave it as an implicit good practice.

### Reference cards (tarjetas de referencia)
The most effective concrete UDL adaptation for early programming classes. Specify exactly what each card should contain:
- Class 01: flow diagram symbols.
- Class 02: base C++ program structure.
- Class 03: relational and logical operators table.
- Class 05: loop syntax comparison (for / while / do-while).
- Class 06: array access patterns.

### Exercise 10 is always a reflection
This was a non-negotiable maintained throughout the course. It creates metacognition and emotional closure. Never replace it with a coding exercise.

### Plan B for inspirational talk classes
Always include an explicit Plan B in the preparation checklist for if the external guest cannot attend. The Plan B for programming courses: a group code-tracing exercise using a problem relevant to the talk's theme.

### STEAM woman selection: content relevance beats fame
The most effective selections were those where the connection to the class content was specific:
- Karen Spärck Jones for linear search (her TF-IDF work is the large-scale version of the same problem).
- Gladys West for conditional logic (GPS uses exactly that reasoning).
- Radia Perlman for multiple-choice conditionals (her STP protocol chooses among multiple network paths).
Avoid selecting well-known names if a less-known woman has a more direct connection to the content.

### Dodona exercise verification
Every code exercise must be manually traced with a concrete input before including it. Two exercises had to be corrected during generation because the expected output was not what the code would actually produce.

### Class 05 slides stub
During generation, class-05/01-slides.md was created as a stub file because the file already existed. The full slides content is in 00-class-overview.md. Future generations: check for existing files before creating them; use str_replace or bash overwrite if the file needs to be replaced.

### Facilitation guide error messaging section
For programming courses, add a dedicated section in the facilitation guide: "Cómo acompañar errores comunes" with the most frequent compiler errors per class level and the protocol "leer el error con la alumna, no para ella."

### full-glossary.md format
Alphabetical order, each term with a (C0N) class tag, one-paragraph prose definition. No tables. No per-field structure. Generates last, after all class glossaries exist.

---

## IA Aplicada: Agentes (2025)

### Neurodivergent accessibility
Session raised: printed instruction cards for cognitive overload, alternative Kahoot formats, alternative cross-testing formats. Not fully resolved — pending for future iterations.

### Technical stack
OpenAI Python SDK with Groq provider via `base_url` override. Groq model: `llama-3.3-70b-versatile`. PatagonIA (Chile) not yet publicly available but recommended as course content.

### Latin American AI context
Incorporating PatagonIA (Chile), Sabiá (Brazil), and Amazônia IA into early classes adds relevant regional context. Add to Class 01 materials in future delivery.

---

## Robótica para Competencias ROV Aplicadas (2026)

### Si el programa fuente nombra una herramienta profesional pesada, NO asumir que es viable en aula
El programa nombraba el **UUV Simulator** (ROS + Gazebo). Es la referencia profesional, pero instalarlo en ~30 laptops de adolescentes es inviable. Solución: construir un **simulador de aula propio en Python puro** (`rovsim/`) que implementa la MISMA API conceptual (comandar empuje, leer sensores, cámara, waypoints, detección de color con OpenCV real) y corre en cualquier laptop con `pip install numpy opencv-python`. La herramienta profesional y el ROV físico quedan como el "mundo real" al que se apunta, con un puente explícito y honesto documentado en `technical-setup.md` (tabla `rovsim` ↔ ROS/Gazebo/ROV físico). **How to apply:** para cualquier curso técnico hands-on, decidir la plataforma EJECUTABLE antes de generar ejercicios; si la del programa es pesada, construir un wrapper/simulador liviano que implemente su API.

### La generación multiagente de primera pasada es pedagógicamente completa pero técnicamente NO ejecutable
Los subagentes produjeron clases con excelente estructura 5E/Bloom/DUA/tono, pero el código de los ejercicios usaba una **API inventada e inconsistente** (`rov.set_velocity` en una clase, `rov.set_thrust_z`/`set_yaw_rate` en otra) y fuentes de cámara incompatibles entre sí (un `rospy.Subscriber` a un topic de ROS en C6, `cv2.VideoCapture(0)` en C7, `cv2.imread("foo.jpg")` en otra). Nada de eso corría. **Lección:** cuando el curso es técnico, o se fija la API ANTES de generar, o se reconcilia después: (1) construir el simulador para que implemente la unión de los métodos que los agentes inventaron (con alias), y (2) barrer y reemplazar todas las fuentes de cámara por una sola (`rov.get_camera_frame()`). Verificar con un `selftest` ejecutable real.

### El usuario detectó "superficialidad" — la profundidad vive en los apuntes, no en las slides
Tras la primera pasada, la dueña del curso preguntó si no estaba "súper superficial". Tenía razón en parte: las slides son necesariamente delgadas. Solución: agregar `08-apuntes.md` por clase (1.500–2.600 palabras de teoría rigurosa pero accesible: control PID, hidrodinámica con Arquímedes, visión por computador, brecha sim→real, máquinas de estado) con ejemplos resueltos y referencias APA 7. **How to apply:** para cursos técnicos, ofrecer desde el inicio un material de lectura de fondo por clase además de las slides; el `01-slides.md` no carga la profundidad conceptual.

### Verificación honesta antes de declarar terminado
Cuando se generan ~100 archivos vía subagentes, leer los resúmenes NO basta: hay que abrir el contenido real (aquí, leer los ejercicios reveló la API ficticia) y, si hay código, EJECUTARLO. Construir un `selftest` (`python -m rovsim.selftest`) que corra los patrones reales del curso (PID, profundidad, giro, cámara+OpenCV) y exigir 4/4 antes de cerrar.

---

## Cross-course patterns

### The 10-class + 2-ceremony format
Both courses used: 10 content classes + 1 opening ceremony (Bienvenida, no class folder) + 1 closing ceremony (Demo Day, no class folder) = 12 sessions total, 88 files.

### Inspirational talk classes (3 per course)
Classes 3, 5, and 9 consistently work well for inspirational talks:
- Class 3: students have enough foundation to ask informed questions but are still in the "learning to code" phase — an inspiring talk sustains motivation.
- Class 5: mid-course, energy can drop — a talk recharges it.
- Class 9: near the end, a talk connecting to professional life helps bridge to what comes next.

### STEAM women repetition across courses
Fei-Fei Li, Grace Hopper, and Karen Spärck Jones have been used in both courses. Prioritize new names for future courses. See `references/steam-women-registry.md`.

### slide-generator brandbook + pedagogical refactor (2026-05-19)
Updated `.agents/skills/skill-slide-generator/generate.js` to align with Brandbook Niñas Pro 2022 and the pedagogical frameworks. Backwards-compatible: existing class-NN/create-slides.js calls keep working with the same field shapes.

Added pedagogical slide types: `objectives` (Bloom-verb learning objectives with pink numbered squares), `steps` (numbered procedure list, brandbook pattern), `manual-trace` (variable-state tracing for programming UDL), `reflection` (Exercise 10 / Evaluate phase, non-negotiable), `rubric` (formative 1–10), `plan-b` (Windows-95 modal for inspirational-talk fallback), `section` (chapter divider with retro frame).

Added brandbook visuals: pixel-art Windows-95 frame on `title` and `section`, yellow squiggle decoration, kawaii brand-icon SVGs (lightbulb-teal, calculator-red, flask-rose, globe-green, star-yellow, check, exclamation, quote, target, tools) replacing Font Awesome, optional B&W photo + overlay on `steam`.

Added validators: `validateSlideSequence(slides)` warns on cold-lecture openings, missing `objectives`/`steam`/`reflection`, and >5 visible lines. `checkLegibility` warns on non-brandbook-compliant color combinations. `buildClassSkeleton(opts)` returns a 5E-valid starter sequence — insert content slides between `objectives` and `kahoot`.

Code blocks now accept named tokens (`keyword`, `type`, `string`, `number`, `comment`, `error`) instead of hex literals; tokens map to brand colors. Existing hex literals still work.

Reason: prior generations were brand-paletted but missed the brandbook's signature retro/Windows-95 aesthetic, the kawaii illustration system, and several pedagogical slide types (objectives, reflection, manual-trace, rubric, plan-b). The validator catches the most common pedagogical mistakes (no engage after title, missing reflection) before the .pptx is finalized.

How to apply: in any new class, call `buildClassSkeleton(opts)` first, then splice in content slides between objectives and kahoot. Resolve all `[pedagogía]` and `[brandbook]` warnings before considering the .pptx done.

### slide-generator alignment with pedagogical references (2026-05-19, segunda pasada)
Después de releer todas las referencias de `skill-create-course` (no solo las cuatro principales), agregué tipos de slide que el generador necesitaba para reflejar lo que las guías piden:

- `glossary` — destaca 2-4 términos clave de la clase (refleja `glossary-guide.md`, que pide 8-10 términos por clase). El glosario completo sigue viviendo en `04-glossary.md`; el slide solo destaca los más críticos antes del cierre.
- `welcome` — sesión de bienvenida con agenda numerada (refleja `facilitation-guide.md` § Sesión de Bienvenida). Sesiones especiales están exentas del validador 5E.
- `closing-ceremony` — Demo Day con 3 hitos color-coded (refleja `time-distribution-guide.md` § Demo Day estructura).
- `block-transition` — transición entre bloques 5E con fase + duración + checklist (refleja `time-distribution-guide.md` § Distribución estándar de clase).

También expandí `steam` para incluir TODOS los campos que pide `steam-woman-guide.md`: `area`, `country`, `connectionToClass`, `quoteAttribution`, `reflectionQuestion`, `source`. El validador ahora emite warning si una slide `steam` no tiene `connectionToClass` (el guide es enfático: relevancia al contenido beats fama).

`error-code` ahora acepta un campo `protocol` que renderiza un callout amarillo "Mentora: …" reflejando el protocolo de `facilitation-guide.md` (§ Cómo acompañar errores comunes — "leer el error CON la alumna, no para ella").

Mejora visual brandbook: el marco retro de `title`, `section` y `welcome` ahora incluye el smiley pixel-art con sombra rosa, cursor estilo Windows-95 y composición letra A + squiggle amarillo (brandbook §00, §04, §05). Antes era solo un outline de ventana vacío.

Path renaming: la skill se renombró de `.agents/skills/slide-generator/` a `.agents/skills/skill-slide-generator/`. Todas las referencias actualizadas.

Razón: el slide-generator de la primera pasada estaba alineado con las 4 guías principales (5E, slides, visual-identity, lessons-learned) pero faltaba alineación con `glossary-guide.md`, `steam-woman-guide.md` completo, `facilitation-guide.md` y `time-distribution-guide.md`. La segunda pasada cierra esos huecos.

How to apply: ver `.agents/skills/skill-slide-generator/example.js` (3 demos: clase estándar, bienvenida, cierre).
