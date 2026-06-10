---
name: learn
description: Map, draft, and teach one concept the research needs — gather verified sources, write the full concept note in context/knowledge/, then build the understanding with the researcher in conversation and hand off to the gate. Triggers on "learn X", when a knowledge gap blocks the current work, or when onboarding placed the researcher in the field-learning stage.
---

# learn

One concept per run. You do all the writing (CLAUDE.md §posture): you gather the sources, draft the complete note, and teach it. The researcher's contribution is the conversation. The note is the durable record; the understanding is built in chat — never assigned as reading.

## Input

A named concept, or a gap you identified (name it and confirm the scope in one exchange before starting).

## Steps

### 1. Scope to the researcher

Read `context/profile.md` and `state.md`. Pitch everything that follows to the profile: the researcher's level, what background to assume, what the current research thread needs this concept *for*. If the concept has an unlearned hard prerequisite, say so and offer to run `learn` on that first — the researcher chooses the order.

### 2. Gather and verify sources

- Search broadly; prefer primary sources. Check `context/knowledge/` first for prior notes that already cover part of the terrain.
- Every claim that will carry weight in the note gets a citation with a URL and access date.
- **Verify each reference resolves** (fetch it; confirm authors/venue/content match the claim). A reference that does not resolve **stops that piece of work**: flag it as possibly hallucinated, exclude it, and say so. Never cite an unfetched source (CLAUDE.md hard lines).
- Where sources disagree, record the disagreement — present a landscape, not a verdict.

### 3. Draft the note

Write `context/knowledge/<slug>.md` — the full substance, not a scaffold. Structure it so it can be taught:

```
# <Concept>
Status: agent-drafted — not yet gate-stamped. Drafted by <model>, YYYY-MM-DD.

## In one paragraph
## The mechanism            — how it actually works, at the profile's level
## The intuition            — why it works; what mental model to hold
## Where it meets this research — what it enables, constrains, or gates here
## What's open or contested — calibrated; sourced where possible
## Sources                  — per-claim citations, access dates
```

The status line is mandatory. An unstamped note is visibly just AI output; only a passed gate changes that.

### 4. Teach it in conversation

Announce the note exists, then teach from it — do not send the researcher to read it. Interactively, not a lecture:

- Build up from what the profile says they know; one piece at a time.
- Check in as you go ("does this square with how you'd have expected it to work?"); invite pushback and questions; follow where they pull.
- Depth is the researcher's call — offer to go deeper or stop at working-knowledge; honor whichever they pick.
- If the conversation exposes a flaw in the note (unclear, wrong emphasis, a gap), fix the note as part of the teaching.

### 5. Hand off to the gate

When the teaching feels complete — the researcher is explaining back rather than asking — offer the gate: "ready to close this one?" The **gate** skill owns everything from there: the interview, the stamp on the note, the record in `context/records/`.

## Hard limits

- Never mark the concept understood, closed, or done from within this skill — only a passed gate stamps the note.
- Never require the researcher to read or write anything; the note serves later reference and verification, not homework.
- Never let an unresolvable reference stand in the note.
