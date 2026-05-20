# Interview Guide

## Purpose

Collect all information needed before generating any course files. Never assume. A short or vague answer is an invitation to ask a follow-up, not to proceed.

---

## Required questions

Ask all of these before starting. Group them naturally in conversation — do not dump them as a numbered list unless the user prefers that format.

### Course identity
- Course name and main topic.
- Audience and age range (default: Niñas Pro, girls 13–19, Chile).
- Number of sessions and format (e.g., 10 classes + opening ceremony + Demo Day).

### Time and schedule
- Total duration of each session.
- **Time distribution** — ask explicitly: how many minutes for lecture, how many for practice, and whether the Kahoot block is carved from those minutes or is additional.
  - This is a frequent source of ambiguity. "1.5h cátedra y 1.5h ejercicios con 15 min de Kahoot" means the Kahoot is within the 3 hours, not on top of them.
- Are there special sessions with a different time distribution? (e.g., sessions with inspirational talks)

### Learning context
- Modality: in-person, online, hybrid, or mixed.
- Prior knowledge level of the students.
- Number of students per session (approximate, for material planning).

### Content
- Source material: PDF, slides, syllabus, topic description, or course program.
  - If the user provides a PDF or slides: read it critically. Use it as input, not as a script. Reorganize, improve, or replace weak structure when pedagogically necessary.
- Mandatory topics or institutional requirements.
- Any topics to exclude.

### Technology
- Available devices and connectivity.
- Allowed tools and platforms (e.g., Dodona, OmegaUp, browser-only, local compiler, Replit, Kahoot, Google Colab, etc.).
- Any tools explicitly not allowed.
- See `references/technology-guide.md` for platform-specific considerations.

### Special sessions
- Are there inspirational talks by external guests? If yes: which sessions, how long, and who coordinates the guests.
- Are there Demo Day, ceremonies, or closing events? How are they structured?
- Does the course have a pilot class before full generation?

---

## How to handle source material

If the user provides a PDF, slide deck, or syllabus:

1. Read it fully before asking questions.
2. Identify what is strong (well-sequenced content, clear objectives, good examples) and what is weak (missing time distribution, no pedagogy, pure content dump).
3. Use it as a structural starting point, but always pedagogically redesign it for Niñas Pro.
4. Note explicitly in `course-requirements.md` what was preserved, what was reorganized, and what was added.

---

## Missing information protocol

If the user does not answer a critical question:
- Ask once more, more specifically.
- If still unanswered, make the most reasonable assumption for Niñas Pro context, document it in `course-requirements.md` under "Supuestos asumidos", and flag it for review.

Do not proceed to file generation with unresolved critical gaps (modality, duration, technology stack).
