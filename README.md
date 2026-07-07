# Swift AI Mission — UX Detective: Squad Mode (Grade 8–9)

A 30-minute, offline, browser-based group game for squads of **3 students**. Having caught UX criminals solo, the squad now runs a design studio: they pick a real school problem, build a working UI mock, and prove it commits **zero of the 8 UX Crimes**.

## How to play

Open **`index.html`** in any modern browser — no server, login, or internet needed.

## The 8 screens

1. **Welcome** — enter the studio.
2. **Assign Roles** — each student names themselves as **Product Lead**, **Designer**, or **Critic / User Tester**. Names are reused throughout.
3. **Pick Your Case** — debate and lock one of three school problems.
4. **Crime Briefing** — predict which of the 8 UX crimes threaten the chosen problem (High / Medium / Low risk).
5. **The Studio** — a drag-and-drop + smart-prompt UI builder with a 12-minute sandclock timer. ~30 pre-styled components; the prompt box parses multiple components and custom text in one sentence.
6. **The Crime Audit** — the Critic runs the 8-crime checklist against the built UI (Committed / Avoided + evidence).
7. **Verdict & Skill Ratings** — studio badge tier plus star ratings across Empathy, Communication, Problem-Solving, Collaboration, Design Thinking.
8. **Debrief** — role-specific takeaways and a downloadable report card.

## Features

- Detective "classified case file" theme with a magnifying-glass cursor.
- Typewriter narration, hover-magnified cards, and a pinned, tappable 8-Crimes reference rail.
- Progress auto-saves to `localStorage`.

## Structure

```
index.html                  # the entire game (self-contained)
Assets/                     # theme + character artwork
UX_Detective_Squad_Mode.md  # the game design document
```

Built for the Swift AI · UX Investigations Unit.
