---
name: onboard
description: Run the setup interview that introduces the workspace, learns who the researcher is, sets the interaction contract, and seeds context/profile.md and state.md. Triggers on the first session in this workspace (context/profile.md still a skeleton) or when the researcher says "start".
---

# Onboard — the setup interview

One staged conversation. The researcher writes nothing; everything they contribute arrives through chat and you transcribe it. Announce at the outset that this interview runs in **conversation mode** and say what that means: read-only, short conversational replies, nothing in the repo changes until they release the mode at the end.

Hold each stage to a few questions at a time. This is a colleague's first coffee, not a form.

## Returning researcher — import a card instead

If the researcher arrives with a **researcher card** from a previous project (ask early, or they volunteer it — a `researcher-card.md` they paste or point you at), do *not* run the cold interview. Instead:

1. Read the card — the person-level profile: who they are, background and level, interaction-contract defaults and recorded deviations, skill preferences. It carries no project content.
2. Run a *short* confirmation conversation (still conversation mode): what has changed since the card was written, and what this new project is about (the seed of `state.md`). People and preferences drift; this is also the moment to re-pitch level if their experience has moved on.
3. Still do Stage 1 (introduce the workspace, modes, gates — they may be on a different machine or have forgotten) and Stage 4 (skills, keyed to the new project's stage). Then write `context/profile.md` from the card as confirmed and seed `state.md` from the new project, per Stage 5's rules and status lines.

Only when there is no card do the full interview below.

## Stage 1 — Introduce yourself and the workspace

In researcher language, briefly:

- **Posture:** you work as their junior colleague — you do the searching, gathering, drafting, and write every document here; they steer, judge, and decide through conversation. You are never fully trusted: anything load-bearing gets verified independently before the work stands on it.
- **The two modes, by name:** *work mode* (default — you build and maintain) and *conversation mode* (read-only talk; you enter it for gates, for decisions that are theirs, and when they are thinking out loud; they release it explicitly).
- **Gates, one honest paragraph:** a gate is an interview-conversation at any point where something is about to be relied on. Nothing here gets marked understood, closed, or done except through one. They exist because this methodology tracks two outputs — the research artifact and the researcher's own growth — and the gates are how the second is built and measured. You are required to run them honestly: no generous passes, gaps are findings rather than failures, and they can override and close any gate (the override is recorded, never argued).
- **The skills, by name, one line each:** `learn` (map and draft one concept, then teach it), `gate` (the interview at closure points), `paper` (deep-read of a fetched source), `gather` (cited web research), `ideate` (diverge, they rank first, converge), `session` (end-of-session ritual), `update` (walk upstream methodology changes together), `researcher-card` (carry your profile to a new project's workspace). Promise to re-introduce each one the first time it becomes relevant — they never need to remember this list.

Do **not** lecture the gate-and-stamp mechanics here. They get demonstrated naturally at the first `learn` → `gate` cycle; say only that much.

## Stage 2 — Interview the researcher

Learn, in their own words:

- Who they are; background and level — what to assume, what to skip, what to build from scratch. This sets the pitch of every note and gate question you will ever produce here.
- Their **proficiency across the fields this research touches** — area by area, roughly (novice / working / proficient / expert). Frame it as "so I pitch things right and don't quiz you on what you already own," not a test. This seeds `profile.md`'s field proficiency and the per-topic proficiency in `state.md`, which calibrate how hard gates open (G24), and it is what the researcher card carries forward.
- Their research goals — what they want out of this work.
- Where the work stands: fresh start, or mid-project. If mid-project, take their account of progress so far — decided directions, dead ends and why, open threads. This becomes the seed of `state.md`; take it down faithfully.

## Stage 3 — The interaction contract

Propose the methodology's defaults plainly, then ask how they want to adjust:

- You do the heavy lifting; their contribution is conversation — they are never required to write or read a file.
- Chat-first: decisions, explanations, and reviews happen in dialogue, not documents.
- Gates at every closure; you close them by default when the conversation stops producing value, with their override on record at any time.
- Conversation mode triggers as introduced in stage 1.

Ask about cadence, how test-like or collegial they want gates to feel, and what (if anything) they want to keep doing themselves. Record their choices. Deviations from the defaults are signal, not error: note each in a dated `FRICTION/` entry (marked agent-drafted, methodology-only) and never argue against one.

## Stage 4 — Skills selection

Recommend which skills fit their stage — an early or learning-stage project leans on `learn`, `gate`, `paper`, `gather`; a project nearing commitment leans on `ideate` and gates over decisions. `session` and `update` apply to everyone. Parameterize from stage 2: the pitch level for notes and explanations comes from their stated background. Their selection and parameters go in the profile.

## Stage 5 — Close and write

1. Summarize back what was agreed — who they are, the contract, the skills in play, where the work stands — and ask them to release conversation mode. On release, restate the conclusions in one short summary; that summary is your input for the writes.
2. Write `context/profile.md` (who, goals, background and level, **field proficiency**, interaction contract including recorded deviations, skills in play) and seed `state.md` (current question, where the work stands, decided directions, dead ends, open threads, next step, **per-topic proficiency** from the fields named) **from their words** — transcribe, never invent; leave unknown sections explicitly open rather than filled. Both files carry an inline status line: `status: agent-drafted (onboarding transcript, YYYY-MM-DD)`. Onboarding stamps nothing — these files are not "closed"; only the `gate` skill ever marks anything understood, closed, or done.
3. Check the source pin in `CLAUDE.md`. If `pinned_commit` is still TODO, tell the researcher it blocks the `update` skill only — research can proceed — and note it in `FRICTION/`.
4. Tell them what happens next, in one or two sentences keyed to their stage and selected skills, and that you will introduce each mechanism the first time it is actually used.

## Friction to watch

In the moment (CLAUDE.md §Friction capture): the interview feeling like a form, or a proposed default rejected — record the deviation (Stage 3 already calls for this) and tag usability or value.
