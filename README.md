# MindCheck — Mental Health Check-in & Support

A lightweight, single-page web app that gives people a private, low-pressure way to reflect on their mental state and connects them to verified, real crisis resources and mental health professionals in India.

**Live demo:** [add your published link here]

---

## Why I built this

Suicide prevention and mental health tooling is an area where careless design does real harm. Most "mental health quiz" projects either:
- present themselves as diagnostic (dangerous — an unvalidated quiz telling someone they have depression can do more harm than good), or
- bury crisis resources at the bottom of a results page, arriving too late for someone in acute distress.

I wanted to build something that took those failure modes seriously rather than just shipping a feature checklist.

## What it does

- **Reflective check-in, not a diagnosis.** A short questionnaire (inspired by widely used screening instruments like PHQ-9/GAD-7) that groups responses into themes — mood, anxiety, stress, sleep, etc. — with explicit, repeated framing that this is a self-reflection tool, not a clinical assessment.
- **Immediate crisis escalation.** If a response to the suicidal-ideation question indicates real risk, the app interrupts the quiz flow *immediately* and surfaces crisis helplines — it doesn't wait for a final score. This mirrors the escalation pattern used in production mental health products.
- **Persistent crisis access.** A sticky banner with the national emergency number (112) and the government mental health helpline (KIRAN) stays visible on every screen, not just a results page.
- **Verified resources only.** Every helpline listed (KIRAN, Vandrevala Foundation, iCall, Sanjivini Society) was checked against current, sourced information — nothing invented.
- **Honest data boundaries.** The psychologist directory doesn't fabricate real people's names or contact details. Instead it ships as a clearly-labeled template pointing to legitimate directories, so real, vetted professionals can be added deliberately.

## Design decisions worth calling out

| Decision | Why |
|---|---|
| No "diagnosis" language anywhere | An AI-generated quiz claiming clinical authority is a misuse risk, not a feature |
| Crisis check happens mid-quiz, not just at the end | Someone in acute distress may not finish the quiz — the safety net can't be back-loaded |
| No backend, no data leaves the browser | Removes a whole category of privacy/security concerns for a sensitive-topic tool |
| Directory is a template, not real names | Fabricating professional contacts is a trust and safety failure, even with good intentions |

## Tech stack

Plain HTML/CSS/JavaScript — no framework, no build step, no dependencies. Runs anywhere as a single file.

## What I'd do next

- Localize helpline info by state/region
- Add a "share with a friend" flow that doesn't require the sender to explain why
- Explore whether a licensed clinician could review/validate the check-in questions before wider release

---

*This is not a substitute for professional mental health care. If you or someone you know is in immediate danger, contact local emergency services.*
