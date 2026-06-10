---
name: session
description: End-of-session ritual — update the state.md cursor from what actually happened, propose context/records/ entries the gates didn't already capture, draft FRICTION/ entries, run light drift checks, and land themed commits. Triggers when the session is wrapping up, the researcher says "wrap up", or a natural stopping point is reached; a lite form (cursor re-ground only) runs whenever the thread drifts mid-session.
---

# session

Close the session so the next one can start cold from `state.md` and lose nothing. Two layers of ownership run through every step: **you write everything directly** — no document is ever handed to the researcher to fill — but **decision-substance must come from the researcher's words** in this session's conversation. Transcribe what was decided; never write a direction, commitment, or verdict that was not actually said. If a needed conclusion was never reached, record it as an open thread, not a decision.

## Lite form (mid-session drift)

When the thread has drifted from the current question: reload `state.md`, restate the current question and next step in one or two lines in chat, and continue. No file edits unless something is plainly stale.

## Full ritual

### 1. Update `state.md` — the cursor

Rewrite freely from what actually happened this session; date the update. Fields: current question · where the work stands · decided directions (researcher's, from their words) · dead ends · open threads · next step. Keep it small: **point into `context/`** for substance (a record, a stamped note) rather than restating it. Decided directions go in only if the researcher decided them in conversation; anything you concluded alone stays an open thread.

### 2. Propose `context/records/` entries

Scan the session for things produced that gates and decision records did not already capture: a direction the researcher chose outside a formal gate, an override, a result worth remembering, a divergence between your advice and their call. Draft each as a record entry and propose it in chat before writing. Do **not** mark anything understood, closed, or done here — that is the `gate` skill's sole route; if something looks ready to close, say so and offer a gate instead.

### 3. Draft `FRICTION/` entries — in the background

Write dated entries on how the *methodology* behaved this session: what helped, what chafed, what was ignored or overridden, ceremony that bought nothing. Rules:

- **Methodology only — never research content.**
- Each entry readable out of context (a maintainer with no access to this workspace should understand it).
- Status line on each: `agent-drafted YYYY-MM-DD`.
- Do this without being asked and without making it an event. Once written, mention it in one line and invite — don't nag — the researcher to add their own observations; if they voice any, write them down in their words, marked as theirs.

### 4. Light checks — surfaced only when they fire

Run silently; say something only if a check trips. At most one or two notices per session, one line each:

- **Exploration share.** If everything lately has been refinement of a single thread, say so: some effort should aim at no current deliverable.
- **Unstamped stretch.** If a stretch of sessions has produced work with no gates, note it: "a lot here is unstamped — want a gate pass over what we're relying on?"
- **Periodic review (~monthly).** When enough has accumulated in `context/records/` since the last review, propose the review conversation: walk the records together — what got delegated and might be atrophying, what got easier, where overrides cluster. A conversation, not a form; its conclusions come from the researcher and are recorded like any decision.

### 5. Commit (if the repo uses git)

- Group the session's changes into themed commits — one conceptual move each, not one blob.
- Commit locally. **Never push to any remote without the researcher's explicit confirmation**, this session, for this push.

## Hard lines

- Never close, stamp, or mark anything done from this skill — hand off to `gate`.
- Never write a decision, direction, or verdict the researcher did not voice.
- Never put research content in `FRICTION/`.
- Never require the researcher to read or write a file; everything above reaches them through chat.
