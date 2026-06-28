---
name: update
description: Walk upstream methodology changes with the researcher — fetch update documents from the source repo, converse item by item (adopt / skip / adapt, the researcher's call each time), apply adoptions to workspace machinery, and move the source pin forward deliberately. Triggers on "update" or "check for updates", and on the session-start discovery check finding the pin behind; offer the walk — never run it unprompted, and never re-offer a version the researcher has declined.
---

# update — walk upstream methodology changes

The downstream channel. The methodology behind this workspace evolves; this skill is how changes arrive — through conversation, never silent application. Adoption decisions are researcher-reserved.

**Discovery is proactive.** The session-start check (`CLAUDE.md` §Session ritual) compares the pin against the source `updates/` and offers this walk when the pin is behind — so the researcher need not remember to ask. The offer never nags: never start the walk unprompted, and if the researcher declines, record a one-line note in `context/records/` (`update walk declined YYYY-MM-DD at pin <hash>`) so the same updates are not re-offered every session — only a *newer* document past that point re-triggers the offer.

## 1 · Read the pin

Read the **Source pin** block in `CLAUDE.md`: `source_repo`, `pinned_commit`, `updates_path`.

- If `pinned_commit` is `TODO`, resolving it with the researcher is step one: explain what the pin is for (it anchors which upstream changes have already been incorporated), propose pinning to the source repo's current commit, and record their decision. Do not proceed on a TODO pin.

## 2 · Fetch and select

Fetch the `updates_path` directory from `source_repo`. Update documents are numbered, immutable once published, and written for you, the agent: each states what changed, why (with evidence links), and what to ask your researcher. A document may have an attachments folder beside it (`NNNN-files/`) carrying the exact content of any whole files it installs.

Select the documents that apply: those cut *after* your current pin — i.e., your `pinned_commit` falls in the document's `applies_from` range (at or before the commit named there). Walk them in ascending number. If none apply, say so, confirm the pin is current against the fetched commit, and stop. If a fetch fails, stop and report — never reconstruct an update document or an attachment from memory.

## 3 · Walk each document, item by item

Enter conversation mode for the walk (adoptions are researcher-reserved decisions). For every item in every applicable document, in order:

1. **What changed** — the concrete difference, in plain terms.
2. **Why** — relay the document's reasoning and its evidence links honestly, including weak or contrary evidence. Do not advocate beyond what the links support.
3. **What the document says to ask** — put its question to the researcher directly.

Then the researcher decides, per item:

- **Adopt** → you apply the concrete edit. **Machinery only**: skills, `CLAUDE.md` sections, workspace conventions. Where the item installs a whole file, fetch its exact content from the document's attachments folder (`NNNN-files/<name>`) — never reconstruct it from the document's prose. Never touch the researcher's research content (`state.md` substance, `context/knowledge/`, records, FRICTION entries) on an update's authority.
- **Skip** → one line in `context/records/` — item, date, "skipped by researcher" — so future updates know not to re-ask.
- **Adapt** → apply the researcher's variant and record the delta in `context/records/` in the same entry style. Never partially apply an item without recording exactly how the applied form differs from the upstream form.

Do not batch ("adopt all?"); each item gets its own decision. You may advise per item and disagree on record; the call is theirs.

## 4 · Move the pin

Only after all applicable documents are walked: update `pinned_commit` in `CLAUDE.md` to the commit you fetched, and say so out loud — which commit, from which, what was adopted/skipped/adapted in summary. Never re-pin silently, never mid-walk, and never if any item was left undecided (leave the pin where it is and record the open items instead).

Write one entry in `context/records/` summarizing the update session (documents walked, per-item outcomes, old pin → new pin), opening with a status line: `agent-drafted — <date>`. This entry is a record, not a closure: nothing here gets marked understood or done — if an update touches material the researcher should re-verify, hand that to the **gate** skill rather than stamping anything yourself.

## 5 · Close: the upstream side

Before ending, check `FRICTION/` for entries that predate this update and bear on what just changed (friction the upstream change addresses, or contradicts). Note to the researcher that these existed before the update — the maintainers read `FRICTION/` by arrangement, so the timing context matters; there is no send mechanism and nothing to transmit.

## Updating the template itself (maintainer use)

The starter **template** is this process's first consumer: the methodology's maintainer applies each new update document to the template before any user ever sees it — that application is the document's test run. When the copy you are updating *is* the template (the maintainer says so; the giveaway is an unfilled skeleton `profile.md` in the template repo):

- There is no researcher interview — the maintainer authored the change. Walk the items as a checklist, applying each; the maintainer may still adapt an item on contact (that usually means the *document* needs fixing before publication, while it still can be — documents are immutable only once published).
- **Do not write `context/records/` entries** — in the template those are content that would ship to every future user. Record the update session in the commit message instead.
- Closing steps, in addition to the pin move: bump `starter_version` in `CLAUDE.md` (patch for wording, minor for behavior, major for workspace-shape breaks).

## Friction to watch

In the moment (CLAUDE.md §Friction capture): an upstream change the researcher found confusing, or adopt/skip friction on a particular item. Tag value or usability.

## Hard lines

- Never apply an upstream change without the researcher's per-item decision (template mode excepted — the maintainer authored the change).
- Never re-pin silently or partially.
- Never edit research content under this skill — machinery only; in template mode, never write `context/records/` entries.
- Never edit an upstream update document or attachment from a consuming repo; corrections upstream are a new update.
- Never mark anything understood, closed, or done here; that is the gate skill's alone.
