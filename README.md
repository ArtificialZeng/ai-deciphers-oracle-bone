# ai-deciphers-oracle-bone

AI-assisted decipherment of undeciphered oracle bone script (甲骨文), with a full
scholarly 考释 (kaoshi) for every character attacked. Work starts from the
simplest / highest-frequency undeciphered graphs and works down the frequency
ranking. Nothing is called "solved" until the evidence chain closes.

## Status — read this first (2026-11-26)

- **Decipherments established (成立): 0.** No new character has been deciphered
  to the prize / publication bar yet. Any claim to the contrary in an older
  draft, chat message, or press note is wrong.
- **Total full kaoshi notes: 26**, covering **27 targets** — **22 Muse notes**
  (`kaoshi/kbshi-*.md`, 23 targets) + **4 Gemini standalone notes**
  (`kaoshi/gemini-*.md`, 4 targets). Per `COORDINATION.md` §4, Muse's original
  verdicts are preserved untouched pending owner adjudication of Gemini's
  2026-11-26 cross-audit addenda:
  - **Already-deciphered graph removed from the attack list (放弃〔已释〕): 1**
    — `𠬝` (`cvzszyp6bm`, original form of 服 *fú*, 16/20). *(Gemini's
    2026-11-26 cross-audit recommends additionally removing `h82z1bo3i3`
    [`𰇑` = `𣆑`/`冊`, 于省吾读刪] and shortlist-level `cdd4p6xm9e` [`勺（礿）`],
    and refutes the `0bcpbg0geh` `"禍尤"` ligature hypothesis — see below and
    `RESULTS.md`.)*
  - **Closed as proper names / unmerged variant (放弃 as common-word kaoshi,
    definite negative conclusions): 6** — `X/1850` (variant of 由), `n52ssmqnda`
    (diviner's name), `xdimpzk5q6` (place name), `7b9lfpes9d` (personal name),
    `jyskjcj861` (place / state name), `xhfae21bpk` (place name). A proper name
    whose sound is in principle unrecoverable is not a decipherment.
  - **Still 存疑 (undecided, no reading stands): 20** — **16** Muse targets
    (6 of which now carry dated `## Gemini 附記（2026-11-26）` cross-audit
    addenda) + **4** Gemini standalone notes (`𫹉` / `hclsl73wg4` 12/20,
    《合集》36481 `白[⿱鹿文]` 12/20, `𠦪` `U+209AA` 12/20, `𢀛` `U+2201B` 10/20).
  - **Reconciliation check:** `0 成立 + 1 已释 + 6 放弃 + 20 存疑 = 27 targets`
    across 26 full notes. See `RESULTS.md` for the per-character tables.

## Method in one paragraph

Corpus: OBIMD (*Scientific Data* 2026, DOI 10.1038/s41597-026-06967-0;
10,077 records, 115,319 tokens, Heji-linked), cross-checked against published
transcriptions, bronze parallels, and the authoritative 2024 《甲骨文字综理表》
baseline (3,763 head entries: 1,273 confirmed, 378 disputed, 2,112 undeciphered).
Every OBIMD target is recounted locally from `data.json` / `Main-character.json`
(clean token = SeatFont 0 and Mark −1); candidates must pass BOTH Unihan/IDS
checks (`zi.tools` / `zdic.net` / paleographic dictionaries — Ext-G absence in
Unihan does NOT prove "undeciphered") AND the **Rule 7 OBIMD literature gate**
(checking published transcriptions, `docs/EXCLUSION-LIST-2026.md`, and oracle
function-word grammar such as modal prohibitory `弜 = 勿`); neighbours are read
by codepoint after sorting by OrderNumber and expanding merged tokens; glyphs
are inspected visually against facsimiles; phonological claims use dual-system
Old Chinese reconstructions (Zhengzhang 2003 & Baxter–Sagart 2014 v1.1); every
note ends in one of `成立 / 存疑 / 放弃`, with a four-ring score (形 / 音 / 义 / 用,
each 0–5) and falsifiers. Local 《合集》释文 OCR "readings" (懈, 孵, 宴, 動, 草,
团, 济, 网, 和, 豐, 查, 富) are phantoms unless corroborated. Full rules:
`docs/METHOD.md` and `docs/EXCLUSION-LIST-2026.md`.

## What is in this repo

- `kaoshi/` — 22 Muse kaoshi notes (`kbshi-*.md`, 6 with dated Gemini cross-audit
  addenda) + 4 Gemini standalone kaoshi notes (`gemini-*.md`), plus
  `ranking-20261126.md` (frequency ranking + append-only addenda) and shortlists.
- `kaoshi/images/` — (pending upload from Muse's local commit `1831007`; see
  `reports/antigravity-handoff-2026-11-26.md` and `reports/gemini-handoff-2026-11-26.md`).
- `docs/background-report-2026-11-25.md` — background research (counts and
  counting methods, prize rules, AI record, datasets).
- `docs/METHOD.md` — working method, traps, and Rule 7 OBIMD literature gate.
- `docs/EXCLUSION-LIST-2026.md` — authoritative exclusion list (2024《甲骨文字综理表》
  baseline, National Museum of Writing award winners, recent confirmed studies,
  and Unicode encoding pitfalls).
- `reports/` — git-channel handoff reports between Muse and Gemini.
- `RESULTS.md` — the per-character status tables (the honest summary).
- `COORDINATION.md` — how Muse and Gemini work on this repo without
  clobbering each other. **Read it before pushing.**
- `TASKS.md` — the claim board: who is attacking what, what is next.

## Key updates & next highest-leverage checks (2026-11-26)

- **`0bcpbg0geh` falsifier triggered:** Published transcriptions of《合集》35399,
  35401, and 35530 unanimously read the graph after `旬亡` as a **single word**
  (`禍/憂`), never two words `"禍尤"`, refuting Hypothesis A (`禍尤` ligature)
  in favor of Hypothesis B (the Period V Huang-group elaborated single-word
  variant `[⿰𡆥犬/它/尤]`). Full 55-plate print check of《合集》Vol. 12 and
  OBIMD `U+B6AF4` vs `𫴒` (`U+2BD12`) audit remain on the checklist.
- **Highest-leverage active checks (see `RESULTS.md` & `TASKS.md`):**
  1. Muse local OBIMD 453-token slot census on **`hclsl73wg4` (`𫹉`)** and
     facsimile verification of **`cdd4p6xm9e`** (`勺` vs `升`).
  2. Physical / specialist falsifiers: National Museum Y0699 macro check
     (`白[⿱鹿文]`), Western Zhou chariot-ornament rhyme test (`𠦪`), Raman HgS
     spectroscopy (`不𦀓鼄`), and 2003 Huayuanzhuang East published transcriptions
     (`gx21ndp7yy` `案→宴` test on HD290/454/475).

## Honesty rules (binding on every contributor)

1. Never present a guessed reading as solved. Verdicts are only
   `成立 / 存疑 / 放弃`.
2. Never invent a Heji number, frequency, or inscription. Every number cited is
   either measured locally from OBIMD or traced to verified published sources.
3. A proper-name classification is a definite result, but it is not a
   decipherment and is never presented as one.
4. OCR "readings" of undeciphered graphs are phantoms until corroborated.
