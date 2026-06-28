---
name: gather
description: Targeted web research with per-claim cited evidence, synthesized as a landscape rather than a verdict. Triggers when the researcher asks to find out something, when a factual question needs grounding before the work can proceed, or when terrain needs mapping ahead of a decision.
---

# gather

Cited web research in service of the current question. This skill collects and structures evidence; it never selects the direction the evidence points to — selection is the researcher's (G13). Stay in work mode throughout; if the findings feed a decision or a closure, hand off (below).

## Steps

### 1. Plan the searches

State the target precisely: what question the gather answers and what would count as having answered it. Plan the searches — a handful for a narrow question, up to ~15 for terrain-mapping — and state the plan before running it. If the question is really a request for a decision ("which should I use?"), gather the comparison; the choice goes back to the researcher.

### 2. Run them

Web search for breadth, fetching specific URLs for depth. Prefer primary sources and recent material; seek corroboration from independent sources for anything that looks load-bearing.

### 3. Write findings per claim

One line per claim:

```
- [claim] — confidence: low/med/high — URL (accessed YYYY-MM-DD)
```

- Confidence reflects source quality and corroboration, not fluency.
- **No hallucinated URLs.** Only cite URLs a search or fetch actually returned. If a search finds nothing, write that down: what was searched, what came back empty. An empty result is a finding.
- Flag every claim that would need fetch-verification before the work can stand on it — the source fetched, read, and confirmed to actually *support the specific claim*, not merely that the URL resolves. Until then it is search-result-grade, not load-bearing.

### 4. Synthesize — a landscape, not a verdict

A short closing section that lays out the terrain: what exists, where the tension or disagreement is, what the live options are and what each costs. You may give your advice, marked as such and on record — but never answer "so what should I do"; selection and direction stay the researcher's. End by handing the terrain back. Where the terrain is clearer drawn — a comparison table, an options-vs-costs map — the **illustrate** skill can render it inline; the picture still lays out the landscape, it never makes the selection.

## Output

- **Small question, answered inline:** report the claims and synthesis in conversation; nothing written to the workspace unless the researcher will rely on it later.
- **Anything worth keeping:** a dated gather note in `context/knowledge/` (e.g. `YYYY-MM-DD-gather-<topic>.md`), opening with the inline status line:

  ```
  Status: agent-drafted — <model>, YYYY-MM-DD
  ```

  Structure: the question · searches run (including empty ones) · per-claim findings · landscape synthesis · claims needing fetch-verification.

## Hand-offs

- A note becomes understood/relied-on only through the **gate** skill — this skill never stamps, closes, or marks anything done.
- A single paper that deserves depth → the **paper** skill (fetch-before-write), not a gather line.
- If findings reshape the current question or open threads, propose a `state.md` update; the substance of any direction change is the researcher's call.

## Friction to watch

In the moment (CLAUDE.md §Friction capture): confidence tags read as noise, or search-grade findings the researcher will not trust without verification. Tag usability or integrity.

## Hard lines (inherited from CLAUDE.md)

- A citation that does not resolve stops that piece of work — flag it as possibly hallucinated.
- Load-bearing claims carry a real source and date or are marked "unverified."
- Never decide direction; lay out options and hand back.
