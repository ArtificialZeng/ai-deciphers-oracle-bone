# Coordination — Muse and Gemini on this repo

This repo is maintained by two agents at the same time: **Muse** (second
brain / verification, working from its own VM) and **Gemini** (working via
the user's Mac / Antigravity). The user is the owner and final arbiter.
The rules below exist because the two agents cannot see each other's live
work — the repo itself is the only shared channel.

## 1. The repo is the channel

- All results, notes, and status go through git. No result counts as
  delivered until it is committed on a branch and the branch is visible on
  GitHub (or, failing that, as a git bundle whose link is handed to the user).
- A claim made in chat but not in the repo does not exist for the other agent.
- If you cannot push (no credentials, auth rejected), say so plainly in
  `TASKS.md` / in your message to the user, and hand over a bundle. Never
  report a push that did not happen. (Precedent, 2026-11-20 BioXArena:
  Muse's local commits existed but the remote log showed 0 — that failure
  mode must not repeat silently.)

## 2. Branches, never direct pushes to main

- `main` is integration only. Nobody pushes to `main` directly.
- Branch naming: `muse/<topic>-<date>` for Muse, `gemini/<topic>-<date>`
  for Gemini. This PR: `muse/kaoshi-rounds-1-22-2026-11-26`.
- One character / one round = one commit (or one small commit series), with
  the kaoshi note + its images + the ranking addendum together, so a round
  can be reviewed or reverted as a unit.
- Merge only by PR, reviewed by the user (or by the other agent, explicitly
  at the user's request). Never force-push `main`. Never rewrite a branch
  the other agent has already pulled — if a branch is stale, rebase onto the
  new `main` and say so in the PR.

## 3. Claiming work — check before you start

- Before attacking a character, read `TASKS.md` and the open PRs/branches.
  If a UID is listed as in progress, do not attack it in parallel.
- Claim a UID by adding a row to `TASKS.md` (UID, agent, date, status) in
  your own branch, and say so in the PR description. A claim lasts until
  its kaoshi note lands or the agent reports it blocked.
- The closed-target list in `RESULTS.md` (already-deciphered, proper-name,
  or 存疑-with-note) must not be re-attacked as a new character. Re-opening
  a closed target needs a new piece of evidence, stated in the PR.

## 4. File ownership (to avoid edit conflicts)

- `kaoshi/kbshi-<uid>-kaoshi.md` + its images: owned by the agent that wrote
  the round. The other agent does not edit the note's verdict or scores;
  corrections go in as a dated addendum at the end of the note, or as a
  review comment on the PR.
- `kaoshi/ranking-20261126.md`: append-only addenda, one per round, dated.
  Never rewrite another round's addendum.
- `RESULTS.md` / `TASKS.md`: updated by whoever lands a round, in the same
  PR as the round. If both agents land rounds the same day, the second PR
  rebases the table — last writer re-checks the counts, never blind-merges.
- `README.md` status block: updated with every landed round; the numbers
  (成立 / 已释 / 放弃 / 存疑) must always add up to the number of targets
  with full notes.

## 5. Honesty rules (binding, same as README)

- Verdicts only 成立 / 存疑 / 放弃. No guessed reading presented as solved.
- No invented Heji number, frequency, or inscription.
- A proper-name classification is not a decipherment.
- Local 《合集》释文 OCR "readings" of undeciphered graphs are phantoms
  unless corroborated (documented cases: 懈, 孵, 宴, 動, 草, 团, 济, 网,
  和, 豐, 查, 富).
- The 0bcpbg0geh 禍尤 hypothesis (17/20) stays 存疑 until the print check
  in `RESULTS.md` is done. Neither agent upgrades it alone.

## 6. What each agent does

- **Muse**: OBIMD transcription-side screening and full kaoshi notes
  (this PR: rounds 1–22), verification of claims, ranking maintenance.
  Muse cannot run anything on the user's Mac and cannot control other
  models there; coordination is via git and files only.
- **Gemini**: per the user's direction on his side (Mac / Antigravity).
  Gemini's plan, branches, and results should be recorded in `TASKS.md`
  the same way so Muse can avoid duplicating them. If Gemini's work is in
  a different repo or directory, the user (or Gemini) should note the
  location here — Muse will not guess it.
