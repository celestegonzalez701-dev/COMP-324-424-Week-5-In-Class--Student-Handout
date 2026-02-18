# COMP-324-424-Week-5-In-Class--Student-Handout

## The Case of the Flaky UI (group)

Today you will work in a small team (2–4) to solve mini challenges embedded throughout the Week 5 slides.

Your submission is a **single PDF** containing:

- your team’s answers
- one-sentence explanations (“why”) for each challenge
- your final reveal solution

**n.b.** responses must be typed and not handwritten.

## Team info

- Team name:
- Section/time:
- Members (names):

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

- Non-goal (out of scope):
- Constraint (time/device/a11y/data):
- Commit 1 message (render-only milestone):

Explanation (one sentence):

-

---

### Challenge 2 (Events): The Vanishing Submit — keyword `SUBMIT`

Answer (event to handle):

-

Explanation (one sentence):

-

---

### Challenge 3 (Targeting): The Wrong Suspect — keyword `CLOSEST`

1) Why is `e.target.dataset.id` missing?

-

2) One-line fix:

-

Explanation (one sentence):

-

---

### Challenge 4 (Delegation): The Listener Heist — keyword `DELEGATE`

- Ideal number of listeners:
- Where the listener should live:

Explanation (one sentence):

-

---

### Challenge 5 (State): Evidence vs Decoration — keyword `STATE`

Circle the ones that should be JavaScript state (copy them here):

-
-
-

Explanation (one sentence):

-

---

### Challenge 6 (Derived UI): The Missing Render — keyword `RENDER`

- Most likely cause (A/B/C):

Fastest evidence you’d check next:

-

Explanation (one sentence):

-

---

### Challenge 7 (A11y): The Truthful Toggle — keyword `ARIA-PRESSED`

- Attribute:
- Bonus: value when label says “Unfavorite”:

Explanation (one sentence):

-

---

### Challenge 8 (Debugging): Freeze the Scene — keyword `DEBUGGER`

1) Statement that pauses execution:

-

2) Two things to inspect while paused:

- 
- 

Explanation (one sentence):

-

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

1)
2)
3)
4)
5)
6)
7)

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
