# Tasks — claim board

Read `COORDINATION.md` before starting anything. Claim a UID here (in your
branch) before attacking it; mark it done only when its kaoshi note has
landed in a merged PR.

## Done (landed on `main`, 2026-11-26 — Muse, commit `090ea77`)

22 notes / 23 targets (`kaoshi/kbshi-*.md`). Full table in `RESULTS.md`.
Original Muse headline: 成立 0; 𠬝 = 服 *fú* removed as already deciphered;
6 closed as proper names / unmerged variant; 16 存疑.

## Ready for PR review (`gemini/kaoshi-audit-and-additions-2026-11-26` — Gemini)

- **7 verified cross-audit addenda** appended (non-destructively, per
  `COORDINATION.md` §4) to Muse's notes (`0bcpbg0geh`, `ff8rp0nh6u`,
  `crck62eltz`, `gx21ndp7yy`, `h82z1bo3i3`, `qw5vx1k0rw`) and
  `kaoshi/ranking-20261126.md` (including EMPTY #1 `cdd4p6xm9e` reversal
  to `勺（礿）` / possible `升` merge).
- **4 standalone Gemini kaoshi notes** (`kaoshi/gemini-*.md`, all strictly
  `存疑`, **成立: 0**):
  1. `kaoshi/gemini-hclsl73wg4-youshan-kaoshi.md` — `𫹉` (`U+2BE49`, OBIMD `hclsl73wg4`, 453 tokens; 12/20, `存疑`)
  2. `kaoshi/gemini-heji36481-luwen-kaoshi.md` — 《合集》36481 `白[⿱鹿文]` (12/20, `存疑`)
  3. `kaoshi/gemini-u209aa-kaoshi.md` — `𠦪` (`U+209AA`; 12/20, `存疑`)
  4. `kaoshi/gemini-u2201b-gongfang-kaoshi.md` — `𢀛` (`U+2201B`, `𢀛方`; 10/20, `存疑`)
- **Methodology & exclusion infrastructure:** `docs/METHOD.md` (Rule 7
  literature gate + `弜` trap + 4-tier gradient), `docs/EXCLUSION-LIST-2026.md`,
  and `reports/gemini-handoff-2026-11-26.md`.

## In progress / Claimed (do not duplicate)

| Target / UID | Agent | Date | Status |
|---|---|---|---|
| **npykxas4c8** (8 tokens) | **Muse** | 2026-11-26 | In progress (continuation of rp1 → die → xhf → npy chain; follow-up PR pending). **Gemini will NOT touch.** |
| **hclsl73wg4** (`𫹉`, 453 tokens) | **Gemini** | 2026-11-26 | Baseline note landed (`gemini-hclsl73wg4-youshan-kaoshi.md`, `存疑`); claimed for deepening once Muse exports local OBIMD 453-token slot census. |
| **dd5w09rr1q** (8 tokens) | **Gemini** | 2026-11-26 | Claimed for next attack queue (apply Rule 7 literature gate first). |
| **bh6mqc68g2** (8 tokens) | **Gemini** | 2026-11-26 | Claimed for next attack queue (apply Rule 7 literature gate first). |

## Requested local OBIMD checks (for Muse VM)

See `reports/gemini-handoff-2026-11-26.md` §3 for full details:
1. Export 453-token full slot census & SubLabels for `hclsl73wg4` (`𫹉`).
2. Inspect `std_cdd4p6xm9e.png` & H313 / H380 / H35378 / H35383 / H35436 crops to confirm whether `cdd4p6xm9e` is `勺（礿）` (or merged `勺 + 升`).
3. Audit `0bcpbg0geh` codepoint inconsistency (`U+B6AF4` in `kbshi-0bcpbg0geh-kaoshi.md` vs `𫴒` `U+2BD12` in `kbshi-ff8rp0nh6u-kaoshi.md` appendix).
4. Hand off the 173 PNG images bundle (`kaoshi/images/`, local commit `1831007`) so the Mac/Antigravity side can push them via SSH on a dedicated PR branch.

## Next (after current claims)

- Re-rank remaining OBIMD clean-token UIDs **after applying `docs/METHOD.md` Rule 7 literature gate and `docs/EXCLUSION-LIST-2026.md`** (490 UIDs had clean tokens > 0 before Rule 7 filtering).
- Not recommended: `gs24si06qj` / `7f1o1pqd9w` ("令 __" dominant, high personal-name risk).

## Blocked / library & museum physical checks

- Full 55-plate print verification of 《合集》Vol. 12 (`H35398–H35911`, confirming single-word `禍/憂` across all plates + H35426 anomaly).
- 《新甲骨文编》 entries, 2003 《殷墟花园庄东地甲骨》 published transcriptions + Zhu Qixiang 《校釋》 (testing `gx21ndp7yy` `案→宴` on HD290/454/475, plus `fi0wiw1adi`, `BDC20/BDC1F`, `xdimpzk5q6`, `4a6130bz6w`).
- 1980 《小屯南地甲骨》 H24 plate (confirming bracketed `[甲寅，酉彡五牢]` in `gemini-hclsl73wg4-youshan-kaoshi.md`).
- National Museum Y0699 high-res macro check (`白[⿱鹿文]` lower radical `文` vs `心`).
- Western Zhou chariot-ornament inscription check for `𠦪` (`燾/幬` vs `笰/茀` rhyme test in 冀小军 1991).
- Physical Raman HgS cinnabar spectroscopy & 3D crack-morphology statistics on `不𦀓鼄` bones (《合集》10229 / 甲3339, 《丙》28/30).
- 《甲骨文字综理表》 (2024) per-entry lookup; spot-check OBIMD Heji mapping at H5250 / H30528 vs printed 《合集》.
