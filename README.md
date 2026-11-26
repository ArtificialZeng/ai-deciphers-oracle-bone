# ai-deciphers-oracle-bone

AI-assisted decipherment of undeciphered oracle bone script (甲骨文), with a full
scholarly 考释 (kaoshi) for every character attacked. Work starts from the
simplest / highest-frequency undeciphered graphs and works down the frequency
ranking. Nothing is called "solved" until the evidence chain closes.

## Status — read this first (2026-11-26)

- **Decipherments established (成立): 0.** No new character has been deciphered
  to the prize / publication bar yet. Any claim to the contrary in an older
  draft, chat message, or press note is wrong.
- **Total full kaoshi notes: 35**, covering **37 targets** — **27 Muse notes**
  (`kaoshi/kbshi-*.md`, 28 targets, rounds 1–27) + **8 Gemini standalone notes**
  (`kaoshi/gemini-*.md`, 9 targets). Per `COORDINATION.md` §4, Muse's original
  verdicts are preserved untouched pending owner adjudication of Gemini's
  2026-11-26 cross-audit addenda:
  - **Already-deciphered graph removed from the attack list (放弃〔已释〕): 1**
    — `𠬝` (`cvzszyp6bm`, original form of 服 *fú*, 16/20). *(Gemini's
    2026-11-26 cross-audit + local OBIMD facsimile check additionally recommends
    removing `h82z1bo3i3` [`𰇑` = `𣆑`/`冊`, 于省吾读刪], `a5tuvlp0po` [`鞀`/`大鞀`,
    裘锡圭考定打击乐器/乐祭名], and shortlist-level `cdd4p6xm9e` [visually
    confirmed pure 3-stroke `勺（礿）`], refutes the `0bcpbg0geh` `"禍尤"`
    ligature hypothesis, and intercepts 5 additional Rule-7 OBIMD known
    characters including `e33qe36es7 = 舞` — see `RESULTS.md`.)*
  - **Closed as proper names / unmerged variant (放弃 as common-word kaoshi,
    definite negative conclusions): 8** — `X/1850` (variant of 由), `n52ssmqnda`
    (diviner's name), `xdimpzk5q6` (place name), `7b9lfpes9d` (personal name),
    `jyskjcj861` (place / state name), `xhfae21bpk` (place name), `dd5w09rr1q`
    (personal name `子__`), `2bcusrt88g` (place / state name). A proper name
    whose sound is in principle unrecoverable is not a decipherment.
  - **Still 存疑 (undecided, no reading stands): 28** — **19** Muse targets
    (7 of which now carry dated `## Gemini 附記（2026-11-26）` cross-audit
    addenda) + **9** Gemini targets (`𫹉`/`hclsl73wg4` 12/20, 《合集》36481
    `白[⿱鹿文]` 12/20, `𠦪` `U+209AA` 12/20, `𢀛` `U+2201B` 10/20, plus 5 newly
    profiled facsimile-verified OBIMD survivors: `3xbmgmm4j0` 11/20,
    `aelrb19u0i` 10/20, sister pair `o7eb365hnf` 11/20 & `wvxqqsz1w8` 10/20,
    and `o68jkkro3f` 10/20).
  - **Reconciliation check:** `0 成立 + 1 已释 + 8 放弃 + 28 存疑 = 37 targets`
    across `27 + 8 = 35` full notes. See `RESULTS.md` for the per-character tables.

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
团, 济, 网, 和, 豐, 查, 富, 男) are phantoms unless corroborated. Full rules:
`docs/METHOD.md` and `docs/EXCLUSION-LIST-2026.md`.

## What is in this repo

- `kaoshi/` — 27 Muse kaoshi notes (`kbshi-*.md`, 7 with dated Gemini cross-audit
  addenda) + 8 Gemini standalone kaoshi notes (`gemini-*.md`, covering 9 targets),
  plus `ranking-20261126.md` (frequency ranking + append-only addenda) and shortlists.
- `kaoshi/images/` — 9 verified PNG facsimile & audit evidence sheets committed
  by Gemini (`priority_audit_sheet.png`, `survivors_vs_known.png`, and real
  OBIMD facsimile crops for `cdd4p6xm9e`, `a5tuvlp0po`, `3xbmgmm4j0`,
  `aelrb19u0i`, `o7eb365hnf`, `wvxqqsz1w8`, `o68jkkro3f`). Muse's 173 PNGs from
  local commit `1831007` remain pending transfer from Muse's VM.
- `docs/background-report-2026-11-25.md` — background research (counts and
  counting methods, prize rules, AI record, datasets).
- `docs/METHOD.md` — working method, traps, and Rule 7 OBIMD literature gate.
- `docs/EXCLUSION-LIST-2026.md` — authoritative exclusion list (2024《甲骨文字综理表》
  baseline, National Museum of Writing award winners, recent confirmed studies,
  Rule-7 OBIMD interceptions, and Unicode encoding pitfalls).
- `reports/` — git-channel handoff reports between Muse and Gemini.
- `RESULTS.md` — the per-character status tables (the honest summary).
- `COORDINATION.md` — how Muse and Gemini work on this repo without
  clobbering each other. **Read it before pushing.**
- `TASKS.md` — the claim board: who is attacking what, what is next.

## Key updates & next highest-leverage checks (2026-11-26)

- **Local OBIMD corpus audited & 5 new genuine undeciphered UIDs profiled:**
  Gemini downloaded official `KLOBIP/OBIMD` (CC-BY 4.0) locally, completed the
  452-clean census of **`hclsl73wg4` (`𫹉`)** (39 negative-adverb co-occurrences;
  11 co-occurrences with single-graph `彡`), visually proved **`cdd4p6xm9e` =
  `勺（礿）`** (`crops_cdd4p6xm9e.png`), audited **`a5tuvlp0po` = 裘锡圭 `鞀`**
  (`crops_a5tuvlp0po.png`), closed the **`0bcpbg0geh` `U+B6AF4` vs `U+2BD12`**
  codepoint check, intercepted 5 unmerged known characters before attack (saving
  Muse from attacking `e33qe36es7 = 舞`), and produced full facsimile-backed
  kaoshi notes for **5 genuine undeciphered OBIMD survivors**: `3xbmgmm4j0`,
  `aelrb19u0i`, sister pair `o7eb365hnf` (`東+戉`) & `wvxqqsz1w8` (`東+攴`), and
  `o68jkkro3f`.
- **`0bcpbg0geh` falsifier triggered:** Published transcriptions of《合集》35399,
  35401, and 35530 unanimously read the graph after `旬亡` as a **single word**
  (`禍/憂`), never two words `"禍尤"`, refuting Hypothesis A (`禍尤` ligature)
  in favor of Hypothesis B (the Period V Huang-group elaborated single-word
  variant `[⿰𡆥犬/它/尤]`).
- **Highest-leverage remaining library / physical checks (see `RESULTS.md` & `TASKS.md`):**
  1. Printed 《合集释文》 lookups for Vol. 12 (`H35398–H35911`) and the 5 newly
     profiled OBIMD ranges (`H31994–33232`, `H12641–12665`, `H575–8132`,
     `H30329–30455`, `H471–15823`).
  2. Physical / specialist falsifiers: National Museum Y0699 macro check
     (`白[⿱鹿文]`), Western Zhou chariot-ornament rhyme test (`𠦪`), Raman HgS
     spectroscopy (`不𦀓鼄`), 2003 Huayuanzhuang East published transcriptions
     (`gx21ndp7yy` `案→宴` test on HD290/454/475), and full-《合集》 4D
     co-occurrence matrix (`𢀛方` vs `召方`).

## Honesty rules (binding on every contributor)

1. Never present a guessed reading as solved. Verdicts are only
   `成立 / 存疑 / 放弃`.
2. Never invent a Heji number, frequency, or inscription. Every number cited is
   either measured locally from OBIMD or traced to verified published sources.
3. A proper-name classification is a definite result, but it is not a
   decipherment and is never presented as one.
4. OCR "readings" of undeciphered graphs are phantoms until corroborated.
