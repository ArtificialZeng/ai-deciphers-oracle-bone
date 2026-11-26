# ai-deciphers-oracle-bone

AI-assisted decipherment of undeciphered oracle bone script (甲骨文), with a full
scholarly 考释 (kaoshi) for every character attacked. Work starts from the
simplest / highest-frequency undeciphered graphs and works down the frequency
ranking. Nothing is called "solved" until the evidence chain closes.

## Status — read this first (2026-11-26)

- **Decipherments established (成立): 0.** No new character has been deciphered
  to the prize / publication bar yet. Any claim to the contrary in an older
  draft, chat message, or press note is wrong.
- **Already-deciphered graph removed from the attack list: 1.** 𠬝 is the
  original form of 服, read *fú* — established in dictionaries long ago
  (`kaoshi/kbshi-cvzszyp6bm-kaoshi.md`, identification 16/20). This is a
  correction, not a new decipherment.
- **Closed as proper names (放弃 as a common-word kaoshi, definite negative
  conclusions): 6** in full notes — X/1850 (a variant of 由), n52ssmqnda
  (a diviner's name), xdimpzk5q6 (place name), 7b9lfpes9d (personal name),
  jyskjcj861 (place / state name), xhfae21bpk (place name). A proper name
  whose sound is in principle unrecoverable is not a decipherment.
- **Still 存疑 (undecided, no reading stands): 16** in full notes, including
  the strongest lead, 0bcpbg0geh (112 tokens, 17/20, leading hypothesis a
  禍+尤 ligature read "禍尤" — one print check away from 成立 or refutation).
- **Full kaoshi notes: 22**, covering 23 targets. See `RESULTS.md` for the
  per-character table and `kaoshi/` for the notes themselves.

## Method in one paragraph

Corpus: OBIMD (*Scientific Data* 2026, DOI 10.1038/s41597-026-06967-0;
10,077 records, 115,319 tokens, Heji-linked). Every target is recounted
locally from `data.json` / `Main-character.json` (clean token = SeatFont 0
and Mark −1); the Unihan check comes first (a `[CJK, PUA]` double value does
not mean "undeciphered" — 𰇑 has no reading at all, 𠬝 has *fú*); neighbours
are read by codepoint after sorting by OrderNumber and expanding merged
tokens; glyphs are compared by direct visual inspection against deciphered
neighbours; every note ends in one of 成立 / 存疑 / 放弃, with a four-ring
score (形 / 音 / 义 / 用, each 0–5) and falsifiers. The local 《合集》释文
OCR repeatedly invents readings at undeciphered positions (懈, 孵, 宴, 動,
草, 团, 济, 网, 和, 豐, 查, 富) — every such "reading" is treated as a
phantom unless corroborated. Full rules: `docs/METHOD.md`.

## What is in this repo

- `kaoshi/` — one full kaoshi note per attacked character, plus
  `ranking-20261126.md` (full-corpus frequency ranking of the two
  undeciphered pools: 1,159 EMPTY + 820 PUA-only UIDs) and the shortlists.
- `kaoshi/images/` — standard-glyph images, facsimile crops, and
  neighbour-comparison sheets for every round.
- `docs/background-report-2026-11-25.md` — background research (counts and
  counting methods, prize rules, AI record, datasets).
- `docs/METHOD.md` — the working method and the traps found so far.
- `RESULTS.md` — the per-character status table (the honest summary).
- `COORDINATION.md` — how Muse and Gemini work on this repo without
  clobbering each other. **Read it before pushing.**
- `TASKS.md` — the claim board: who is attacking what, what is next.

## The one check that matters most

0bcpbg0geh ("旬亡 __ 才……", 112 tokens, H35398–H35911) is the strongest
存疑 in the whole run. Its falsifier is a library check only: the printed
《合集》释文 for H35398–H35911. If it prints "禍尤" as two characters, the
ligature reading is confirmed; if it prints single 禍, the variant reading
wins. The same print check is the outstanding step for the other
Heji-numbered rounds, along with 《新甲骨文编》 entries and the published
Huayuanzhuang East transcriptions. See `RESULTS.md` § "Outstanding checks".

## Honesty rules (binding on every contributor)

1. Never present a guessed reading as solved. Verdicts are only
   成立 / 存疑 / 放弃.
2. Never invent a Heji number, frequency, or inscription. Every number in a
   note was measured locally from OBIMD and can be re-measured.
3. A proper-name classification is a definite result, but it is not a
   decipherment and is never presented as one.
4. OCR "readings" of undeciphered graphs are phantoms until corroborated.
