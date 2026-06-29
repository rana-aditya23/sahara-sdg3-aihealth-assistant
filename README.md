# SAHARA — Sustainable AI Health Awareness & Response Assistant

An AI-powered conversational assistant that gives people instant, trustworthy health guidance in plain language — without ever diagnosing them.

Built for the **1M1B AI for Sustainability Virtual Internship** (in collaboration with IBM SkillsBuild & AICTE).

**SDG Alignment:** SDG 3 — Good Health and Well-being

---

## The Problem

In rural areas, small towns, and dense urban slums, access to timely medical guidance remains a serious challenge. Doctors and clinics are often far away, expensive, or overcrowded, leaving people to rely on guesswork, neighbours, or unverified social media advice for basic health questions. As a result, minor and treatable symptoms are frequently ignored until they escalate into emergencies, while harmless symptoms sometimes cause unnecessary panic and hospital visits.

## The Solution

SAHARA is a conversational AI assistant that lets a user describe a symptom or health question in their own words, and responds with general self-care guidance, source-backed information, or a clear referral to professional care when needed.

### How it works — a four-stage AI pipeline

1. **Intent & entity extraction** — identifies the symptom type, duration, and severity cues from free-text input, so no medical terminology is required.
2. **Retrieval-Augmented Generation (RAG)** — matches the query against a curated knowledge base of verified public-health guidance, rather than generating open-ended answers. This keeps responses traceable to a real source and reduces the risk of AI hallucination.
3. **Rule-based safety / red-flag detection** — continuously scans every input for emergency indicators (breathlessness, chest pain, severe bleeding, etc.) and overrides the normal response with an urgent escalation message if detected.
4. **Grounded response generation** — delivers general self-care advice, cited information, or an urgent-care referral.

## Target Users

- Residents of rural and semi-urban areas with limited clinic access
- Students and first-time independent adults
- Community health workers (ASHA/ANM) who want a quick-reference companion during home visits

## Responsible AI Considerations

| Principle | How it's addressed |
|---|---|
| **Fairness** | Knowledge base avoids assuming urban-clinic access; covers common conditions across age and regional context |
| **Transparency** | Every response is labeled as general guidance, not a diagnosis, and explains why it was given |
| **Ethics** | Hard-coded refusal to diagnose or prescribe; automatic escalation for red-flag symptoms |
| **Privacy** | No storage of personal or health data; conversations are not linked to user identity |

## Try the Live Demo

Open [`sahara_prototype.html`](./sahara_prototype.html) in any browser — it runs entirely client-side (HTML/CSS/JavaScript), no installation or server required.

If GitHub Pages is enabled on this repo, the live link is:
`https://<your-username>.github.io/<repo-name>/sahara_prototype.html`

**Things to try in the demo:**
- *"I have a mild fever since morning"* → general guidance with a cited source
- *"I feel breathless and dizzy"* → automatic safety escalation to urgent care

## Screenshots

| Welcome | Guidance Response | Safety Escalation |
|---|---|---|
| ![Welcome](./screenshot_1_welcome.png) | ![Guidance](./screenshot_2_guidance.png) | ![Escalation](./screenshot_3_escalation.png) |

## Tech Stack

- **Prototype:** HTML, CSS, vanilla JavaScript (runs fully in-browser, no backend)
- **Presentation:** Generated with PptxGenJS
- **Conceptual production stack:** LLM (e.g. IBM Granite models), vector database for RAG knowledge base, lightweight web/SMS/WhatsApp interface for low-resource deployment

## Project Files

- `sahara_prototype.html` — interactive chatbot prototype
- `SAHARA_SDG3_Project.pptx` — full project presentation (problem, solution, design process, responsible AI, impact)
- `screenshot_*.png` — prototype screenshots

## Disclaimer

This is an educational prototype built for a virtual internship project. It does not store user data, provide medical diagnoses, or replace professional medical advice.

---

**Author:** Aditya Rana
**Internship:** 1M1B AI for Sustainability Virtual Internship (IBM SkillsBuild & AICTE)
