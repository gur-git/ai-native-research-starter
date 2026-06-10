---
name: update
description: Walk upstream methodology changes with the researcher — fetch update documents from the source repo, converse item by item (adopt / skip / adapt, the researcher's call each time), apply adoptions to workspace machinery, and move the source pin forward deliberately. Triggers on "update" or "check for updates"; if you notice the pin is behind, mention it and offer this skill — never run it unprompted.
---

# update — walk upstream methodology changes

The downstream channel. The methodology behind this workspace evolves; this skill is how changes arrive — through conversation, never silent application. Adoption decisions are researcher-reserved.

## 1 · Read the pin

Read the **Source pin** block in `CLAUDE.md`: `source_repo`, `pinned_commit`, `updates_path`.

- If `pinned_commit` is `TODO`, resolving it with the researcher is step one: explain what the pin is for (it anchors which upstream changes have already been incorporated), propose pinning to the source repo's current commit, and record their decision. Do not proceed on a TODO pin.

## 2 · Fetch and select

Fetch the `updates_path` directory from `source_repo`. Update documents are versioned and written for you, the agent: each states what changed, why (with evidence links), and what to ask your researcher.

Select the documents that apply: those whose `applies_from` commit is at or after the current `pinned_commit`. If none apply, say so, confirm the pin is current against the fetched commit, and stop. If a fetch fails, stop and report — never reconstruct an update document from memory.

## 3 · Walk each document, item by item

Enter conversation mode for the walk (adoptions are researcher-reserved decisions). For every item in every applicable document, in order:

1. **What changed** — the concrete difference, in plain terms.
2. **Why** — relay the document's reasoning and its evidence links honestly, including weak or contrary evidence. Do not advocate beyond what the links support.
3. **What the document says to ask** — put its question to the researcher directly.

Then the researcher decides, per item:

- **Adopt** → you apply the concrete edit. **Machinery only**: skills, `CLAUDE.md` sections, workspace conventions. Never touch the researcher's research content (`state.md` substance, `context/knowledge/`, records, FRICTION entries) on an update's authority.
- **Skip** → one line in `context/records/` — item, date, "skipped by researcher" — so future updates know not to re-ask.
- **Adapt** → apply the researcher's variant and record the delta in `context/records/` in the same entry style. Never partially apply an item without recording exactly how the applied form differs from the upstream form.

Do not batch ("adopt all?"); each item gets its own decision. You may advise per item and disagree on record; the call is theirs.

## 4 · Move the pin

Only after all applicable documents are walked: update `pinned_commit` in `CLAUDE.md` to the commit you fetched, and say so out loud — which commit, from which, what was adopted/skipped/adapted in summary. Never re-pin silently, never mid-walk, and never if any item was left undecided (leave the pin where it is and record the open items instead).

Write one entry in `context/records/` summarizing the update session (documents walked, per-item outcomes, old pin → new pin), opening with a status line: `agent-drafted — <date>`. This entry is a record, not a closure: nothing here gets marked understood or done — if an update touches material the researcher should re-verify, hand that to the **gate** skill rather than stamping anything yourself.

## 5 · Close: the upstream side

Before ending, check `FRICTION/` for entries that predate this update and bear on what just changed (friction the upstream change addresses, or contradicts). Note to the researcher that these existed before the update — the maintainers read `FRICTION/` by arrangement, so the timing context matters; there is no send mechanism and nothing to transmit.

## Hard lines

- Never apply an upstream change without the researcher's per-item decision.
- Never re-pin silently or partially.
- Never edit research content under this skill — machinery only.
- Never mark anything understood, closed, or done here; that is the gate skill's alone.
