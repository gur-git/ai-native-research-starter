---
name: gate
description: Run an interview — the verify event — that checks something about to be relied on: a knowledge note ready to close, a decision about to be committed, a result about to be claimed. The only mechanism that marks anything understood, closed, or done. Triggers when the researcher asks ("gate X"), when another skill hands off at a closure point, or when the agent offers one at a natural closure.
---

# gate

A gate is where the workspace's trust comes from: a passed gate stamps an artifact; nothing gets marked understood, closed, or done by any other route. It is an **interview, not an exam** — its output is a contribution to the research (a sharper formulation, a surfaced edge case, a gap that becomes a question), never just a verdict. It also carries the second output: the researcher's own development, measured by records, not impressions.

## 1 · Open

- The gate is the **verify event** (teaching's mirror) — read-only talk, and say so: you withhold and probe rather than explain, until the outcome step.
- Name what is being gated and why now (what the work is about to rely on).
- First gate ever in this workspace: explain the mechanism briefly — what a gate is, what a stamp means, that the researcher can close it at any time.

## 2 · Calibrate, then design the questions

Before the first question, read this topic's line in `state.md` `## Proficiency` and `context/profile.md`. **Open near the researcher's edge, not at the floor**: for material they command, skip the trivial and start where it gets non-obvious; for unfamiliar terrain, start lower and build up. The target is the productive-struggle band — they answer most of what you ask but are genuinely stretched on some (~85% success is where learning is fastest). A gate that never makes them work was too easy; one they cannot get traction on was too hard.

The questions are the ones the work genuinely needs answered next — not ones the notes could answer by pattern-matching. Across the gate, include:

- at least one **work-it-out** question (a derivation, application, or construction the researcher carries through themselves), and
- at least one **why / what-breaks-if…** probe (the answer becomes a constraint or a defense).

**The goal-gradient.** Early in a project, gates on knowledge legitimately lean test-like — articulating the answer is itself how the knowledge becomes whole — say this the first time it applies. Later, the same primitive probes designs, selections, and claims: the answers become the design's constraints and the claim's defenses.

## 3 · Conduct

- Ask one question at a time. Let the researcher commit to an answer before revealing anything — no hints, partial answers, or leading follow-ups before they have answered.
- **Adapt the difficulty as you go** — this is what one-at-a-time is *for*. A confident, correct answer → step up, go adjacent, or probe deeper; a struggle → ease back, scaffold, and correct from an openable source before moving on. Keep each next question in the band: stretching but reachable. Note where their command turned out stronger or weaker than the proficiency estimate said — you will revise it at close.
- Respond honestly to each answer: correct / partial / wrong, with the correction. Where the subject is at the research frontier, your own paraphrase is not a source — ground every correction in a source the researcher can open.
- When a correction or a worked-through gap is clearer as a picture, the **illustrate** skill can draw it — but at the frontier a diagram is never the source; the correction is still grounded in something the researcher can open.
- **A gap found is a finding, not a flunk.** Work it through in the conversation. If it traces to a flawed artifact (e.g., an unclear note), fix the artifact after the gate and note the revisit in the outcome.

## 4 · Close

- **You close by default** when the conversation has stopped producing value — when the next question would only test rather than build.
- You may vote to stay longer; say plainly what you think is still to be gained.
- **The researcher may override and close at any time.** First explain, *once* and briefly (not a lecture), what this stage is for and what closing early leaves unverified. If they persist or give a reason, honor it without further argument: this becomes a **researcher-overridden** close (see §5). Educate, don't enforce — the methodology makes the stake legible; it does not block a researcher who chooses to move on.

## 5 · Outcome

- The gate ran read-only (the verify event); the writes below happen only after the researcher releases it. On release, first summarize what the gate concluded — that summary is the input for the stamp and the record.
- **Genuine pass** (core questions answered with working understanding): stamp the artifact's inline status line — `gate-stamped YYYY-MM-DD` — and write `context/records/YYYY-MM-DD-<slug>.md`: what was gated, a transcript summary (questions, answers, corrections, findings), and the outcome.
- **Unresolved gaps**: no stamp, and never conclude "solid." Write the same record, listing what to revisit; the artifact's status line stays `agent-drafted`.
- **Researcher-overridden** (closed early on the researcher's call, per §4): no stamp. The artifact's status line reads `researcher-overridden YYYY-MM-DD`; record the one-line override and what was left unverified. Work that builds on it inherits the unverified flag.
- Either way, record gaps found and artifacts revised — these records are the raw material for the periodic development-review conversation.
- **Update the proficiency.** Revise this topic's line in `state.md` `## Proficiency` to reflect what the gate actually showed, and date it — this is what lets the next gate open at the right level, and it is itself a development signal (G24).

## Friction to watch

In the moment (CLAUDE.md §Friction capture): the gate reading test-like or patronizing for this researcher, a frontier-correction you cannot ground in an openable source, or an override that signals the gate was mistimed. Tag efficacy or usability.

## Hard lines

- No generous passes. A clean record is honest only if difficulty climbed to a real stretch; a run of easy passes means the gate never found the edge — calibrate upward and say so, don't just file the pass.
- Never close a gate *with a stamp* over unresolved gaps; never stamp anything by any route other than this skill.
- At the frontier, never correct from your own paraphrase alone — openable source or the correction is marked unverified.
- Explain an override's stake once, then honor it without further argument — record it and set the artifact to `researcher-overridden`.
