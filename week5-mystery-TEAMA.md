# COMP-324 Week-5-In-Class--Student-Handout

## The Case of the Flaky UI (group)

Today you will work in a small team (2–4) to solve mini challenges embedded throughout the Week 5 slides.

Your submission is a **single PDF** containing:

- your team’s answers
- one-sentence explanations (“why”) for each challenge
- your final reveal solution

**n.b.** responses must be typed and not handwritten.

## Team info

- Team name: Team A
- Section/time: 001 / 4:15-6:45pm
- Members (names): Celeste Gonzalez

## How scoring works

Each challenge:

- +2 points: correct answer
- +1 point: explanation (“why”) is accurate and clear

Total points possible: 8 challenges × 3 points = **24 points**.

**n.b.** total points will be calculated relative to available listed credits for the assignment submission on Sakai.

## What to submit

Submit **one PDF per team**.

PDF requirements:

- File name: `week5-mystery-TEAMNAME.pdf`
    - e.g. Team name = ancientlives, filename = `week5-mystery-ancientlives.pdf`
- Must include: answers + explanations for Challenges 1–8 and the Final Reveal
- Must be readable (headings intact; tables not cut off)
- Must be typed and not handwritten

\newpage

## Answer sheet

### Challenge 1 (Planning): The Briefing — keyword `SCOPE`

Your three bullets:

- Non-goal (out of scope): User accounts/login and payments/checkout
- Constraint (time/device/a11y/data): Must support keyboard use of Enter and Tab and work with static data (no API)
- Commit 1 message (render-only milestone): Render the list view and detail panel from static JSON (no event handlers yet)

Explanation (one sentence):

- A tight MVP scope reduces complexity so the UI can be rendered correctly before layering on interactions.

---

### Challenge 2 (Events): The Vanishing Submit — keyword `SUBMIT`

Answer (event to handle):

- Handle `submit` on the form (not `click` on the button)

Explanation (one sentence):

- Handling `submit` makes Enter-key behavior reliable and `preventDefault()` stops the browser from reloading the page.

---

### Challenge 3 (Targeting): The Wrong Suspect — keyword `CLOSEST`

1) Why is `e.target.dataset.id` missing?

- Because the click may land on a nested element (like an icon or `<span>`), and that nested element doesn’t have the `data-id`

2) One-line fix:

- `const itemBtn = e.target.closest("button.card");`

Explanation (one sentence):

- `closest()` finds the nearest intended button ancestor so you consistently read the correct `dataset.id`.

---

### Challenge 4 (Delegation): The Listener Heist — keyword `DELEGATE`

- Ideal number of listeners: 1
- Where the listener should live: On the parent container that holds the list/grid of cards

Explanation (one sentence):

- With event delegation, one parent listener handles bubbled clicks and keeps working even after the list is re-rendered.

---

### Challenge 5 (State): Evidence vs Decoration — keyword `STATE`

Circle the ones that should be JavaScript state (copy them here):

- Selected item id
- Current search query
- Whether “Show favorites” is enabled

Explanation (one sentence):

- These are the changing “source of truth,” while DOM classes/labels should be derived from state during rendering.

---

### Challenge 6 (Derived UI): The Missing Render — keyword `RENDER`

- Most likely cause (A/B/C): A — You forgot to call `render()` after updating state

Fastest evidence you’d check next:

- Pause or log inside `render()` to confirm it runs immediately after the state update

Explanation (one sentence):

- The DOM won’t reflect new state unless `render()` runs to rebuild the UI from the updated values.

---

### Challenge 7 (A11y): The Truthful Toggle — keyword `ARIA-PRESSED`

- Attribute: `aria-pressed`
- Bonus: value when label says “Unfavorite”:  `aria-pressed="true"`

Explanation (one sentence):

- Toggle buttons should communicate their on/off state to assistive tech via `aria-pressed`, so “Unfavorite” implies it’s currently on.

---

### Challenge 8 (Debugging): Freeze the Scene — keyword `DEBUGGER`

1) Statement that pauses execution:

- `debugger;`

2) Two things to inspect while paused:

-  `event.target` (and what `closest(...)` returns)
- `state` (or the `dataset` values you’re extracting)

Explanation (one sentence):

- Pausing lets you inspect real runtime evidence (target, dataset, state) to pinpoint why the UI didn’t update.

\newpage

## Final Reveal — The Reliable UI Recipe

Fill the blanks using your case keywords.

1) For forms, handle `___` (and `preventDefault()`).
2) In list UIs, find the intended card with `e.target.___(...)`.
3) Prefer `___` over per-item listeners so re-rendering doesn’t break clicks.
4) Store truth in JavaScript `___` (not DOM classes).
5) After every state update: call `___()`.
6) For toggles: reflect truth with `___`.
7) When something is weird: use `___;` and inspect `___` first.

Your completed recipe:

1) `SUBMIT`
2) `CLOSEST`
3) `DELEGATE`
4) `STATE`
5) `RENDER`
6) `ARIA-PRESSED`
7) `DEBUGGER` and `STATE`

\newpage

## Rubric outline
This in-class group submission will be reviewed and assessed based on the following combined rubrics.

### Universal rubric dimensions (used for most deliverables)
Score each 0–3.

- **Correctness**: are answers correct and consistent with the Week 5 material?
- **Clarity**: is the PDF readable and well-structured (labels, headings, complete sections)?
- **UX & accessibility**: responses demonstrate correct baseline a11y thinking (e.g., form submit, keyboard behavior, `aria-pressed`).
- **Debugging/engineering practice**: explanations reference evidence-based debugging (state inspection, breakpoints/logs) rather than guessing.

Approximate mapping:

- 3 = strong
- 2 = adequate
- 1 = weak
- 0 = missing

### Mystery Game — Case of the Flaky UI (group)
Score each 0–3.

- **Completeness**: all Challenges 1–8 + Final Reveal are answered; each has a one-sentence “why”.
- **Reasoning quality**: explanations are accurate (not just “because slides said so”) and show cause→effect understanding.
- **Terminology & precision**: uses correct terms (`submit`, `closest`, delegation, state vs derived UI, `render()`, `aria-pressed`, `debugger`).
- **Team coherence**: answers are consistent across the document (no contradictions across challenges).
