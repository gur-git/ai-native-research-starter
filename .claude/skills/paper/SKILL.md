---
name: paper
description: Structured, adversarial deep-read of one paper into context/knowledge/, with fetch-verified citations and a recorded researcher relevance judgment. Triggers on "read <paper>", when a source keeps recurring across the work, or when a paper looks keystone for the current research question.
---

# paper

One paper → one deep-read note in `context/knowledge/papers/<slug>.md`. Heavier than a passing citation; lighter than replication. You write the full note — the researcher contributes through conversation afterward, never by filling in sections.

## Steps

### 1. Resolve and fetch — hard precondition
- Resolve the paper to a fetchable source (DOI, stable identifier, URL, or a local file the researcher has pointed at) and fetch it.
- **If it does not resolve, STOP this item.** Flag it to the researcher as a possibly hallucinated reference and do not write anything about it. Never deep-read an unfetched paper.
- The same rule applies inside the note: any load-bearing citation you include must itself resolve to a fetchable source, or that claim is cut or marked "unverified" and flagged.

### 2. Read for structure
Extract from the fetched text, not from memory of the paper or others' descriptions of it:
- the central claim;
- how the paper shows it (method, data, argument);
- what is missing or weak;
- what reproducing it would actually take;
- how it bears on the current research question (per `state.md`).

### 3. Write the note
`context/knowledge/papers/<slug>.md`, opening with the inline status line:

```
Status: agent-drafted | <model>, <date>

# <short title> — <first author>, <year>
**Source**: <resolved identifier/URL, venue, date> · accessed <YYYY-MM-DD>

## Claim                      <1–3 sentences>
## How it shows it            <method, data, argument structure>
## What's missing / where it's weak    <adversarial — mandatory; name concrete gaps,
                               unsupported steps, unexamined alternatives; never a
                               paraphrase of the abstract>
## Reproducibility realism    <what materials/data/resources/effort replication would
                               take, judged against what the paper actually provides>
## Bearing on the current question     <how it touches the question in state.md>
## Researcher's relevance judgment     <empty until step 4 — marked "not yet discussed">
## Sources                    <per-claim: source + access date; any number restated
                               from a secondary source marked "secondary, not verified
                               against the original">
```

Rules for the note:
- Every load-bearing claim carries a source and access date or is marked "unverified."
- Numbers taken from a source that is itself citing another work are marked as secondary restatements.
- Write the whole note yourself; leave no sections as placeholders for the researcher except the relevance-judgment section, which records a conversation that has not yet happened.

### 4. Discuss in conversation
Enter conversation mode and say so. Walk the researcher through the claim, the weaknesses you found, and the reproducibility picture — pitched to their level per `context/profile.md`. Ask for their judgment of the paper's relevance to the current question. On release from conversation mode, transcribe that judgment into the note's relevance section, attributed to the researcher with the date. The judgment is theirs; you may disagree on record inside the note, but the recorded call is what they said.

### 5. Hand off, never self-close
- Update `state.md` if the paper changes the live picture (new thread, contradicted assumption).
- If the paper will be load-bearing — about to inform a design, a direction, or a claim — hand off to the **gate** skill. Only a gate can stamp the note; until then it stays `agent-drafted` and is visibly just AI output.
- This skill never marks anything understood, closed, or done.

## Guarantees
- No deep-read without a fetch; unresolved reference = STOP + hallucination flag.
- The adversarial section is mandatory and concrete.
- Relevance is the researcher's judgment, given in conversation, transcribed by you.
- Closure happens only through the gate skill.
