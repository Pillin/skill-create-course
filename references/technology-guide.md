# Technology Guide

## Purpose

Documents platform-specific considerations for courses that use specific technology. This file is a reference — not a default. The technology stack is captured in `course-requirements.md` during the interview. Never assume a platform.

---

## Technology is course-specific

The interview must establish:
- What devices and connectivity are available.
- What tools are allowed (and explicitly not allowed).
- Whether the course uses an auto-judge platform, a browser-based environment, local installation, or no code at all.

**Exercises, slides, and platform references must match what was agreed in the interview.** A course that uses paper-based exercises should not reference Dodona. A course with no internet access should not assume Kahoot online.

---

## Exercise platforms (when used)

### Auto-judge platforms
Used when: the course teaches programming and the mentor wants automated code feedback.

**Dodona (dodona.be)**
- Developed by Ghent University. Supports C++, Python, Java, and others.
- Exercises must produce deterministic output. The judge compares student output exactly against expected output.
- Students get immediate feedback after each submission.
- Allows self-paced retry — a UDL advantage worth naming explicitly.
- Error messages are in English — explain common ones in Spanish during early classes.
- Exercises not compatible with the judge (pseudocode, diagrams, written reflection): mark explicitly as "no se envía a Dodona."

**OmegaUp (omegaup.com)**
- Latin American platform, interface in Spanish.
- Same auto-judge model as Dodona.
- Better fit for courses targeting Spanish-speaking students who may struggle with English error messages.

**Replit / Ideone / other browser IDEs**
- Used when the course needs a coding environment but no auto-judge.
- Students write and run code in the browser without local setup.
- Useful for courses where setup friction would block learning.

**Codeforces / AtCoder**
- International competitive programming platforms.
- Not recommended as primary platforms for first-time programmers.
- Can be used as supplementary challenge resources for advanced students.

---

## AI/LLM API courses (when used)

### Recommended free classroom setup (as of 2026)
When a course teaches LLM API programming:
- **SDK:** OpenAI Python SDK.
- **Provider redirect:** Groq (free tier, fast inference) via `base_url="https://api.groq.com/openai/v1"`.
- **Model:** `llama-3.3-70b-versatile` (Groq's recommended general-purpose model as of 2026 — verify current availability).
- **API key:** Always instructor-provided or via environment variable. Never hardcoded in student exercises.
- **Advantage of Groq:** Free for classroom use, fast enough for live demos, compatible with the OpenAI SDK with minimal code changes.

### Latin American LLM context (for courses discussing AI in Chile/LATAM)
- **PatagonIA (Chile):** Under development. Not yet publicly available as of early 2026. Recommended as course content (discuss its existence and significance), not as a classroom tool.
- **Sabiá (Brazil) / Amazônia IA:** Latin American LLMs with regional training data. Check current availability before recommending as classroom tools.

---

## Presentation and visual tools

### Canva
- Preferred tool for creating visual slides when the Canva MCP connector is available.
- Use the `request-outline-review` → `generate-design-structured` flow for structured presentations.
- Apply the Niñas Pro brand kit if available.
- If no brand kit: use a clean, high-contrast template. See `references/visual-identity-guide.md`.

### PowerPoint / Google Slides
- Used when Canva is not available or the user prefers them.
- The `01-slides.md` file provides all content, layout suggestions, and image prompts needed to build the presentation manually.

---

## Kahoot
- Always load questions before class and test the entry link.
- Students join via PIN on their own devices.
- The projector shows the question — not the answer until revealed.
- Use Niñas Pro theme if available in the platform.
- If no internet or no devices: replace Kahoot with a whiteboard-based poll (show of hands, answer written on paper, etc.). Note the adaptation in `06-preparation-checklist.md`.

---

## No-technology courses
Some Niñas Pro courses (e.g., algorithm design, entrepreneurship, communication) may not use any code platform. In those cases:
- Exercises are paper-based, discussion-based, or use generic digital tools (Google Docs, Jamboard, etc.).
- The `01-slides.md` file is still the script — but the slides are used for facilitation, not code demos.
- The `03-exercises.md` file uses the same structure but without code solutions.
- Remove any platform-specific instructions from `facilitation-guide.md`.

---

## Classroom infrastructure checklist (to include in `06-preparation-checklist.md`)

For any course using technology:
- [ ] Projector functioning and connected.
- [ ] Internet connection verified (if using online platforms).
- [ ] Kahoot link tested from a student device.
- [ ] Course platform accessible (Dodona, OmegaUp, Replit, etc.) — not blocked by school firewall.
- [ ] Student accounts created (first class only, or any time a new platform is introduced).
- [ ] Backup plan documented if internet fails or platform is down.
