# Tasks — claim board

Read `COORDINATION.md` before starting anything. Claim a UID here (in your
branch) before attacking it; mark it done only when its kaoshi note has
landed in a merged PR.

## Done (landed on `main` — Muse, commits `090ea77`, `14af5ba`, `bab1ae7`)

- **Rounds 1–22 (`090ea77`)**: 22 notes / 23 targets (`kaoshi/kbshi-*.md`).
- **Rounds 23–27 (`14af5ba`)**: 5 notes / 5 targets (`npykxas4c8`, `dd5w09rr1q`,
  `bh6mqc68g2`, `a5tuvlp0po`, `2bcusrt88g`).
- **Rounds 28–37 (`bab1ae7`, 2026-11-27)**: 9 new full kaoshi notes (`3jzeliplnn`
  放弃·人名 13/20 + HD 164 摹本发现; `e33qe36es7` + `e33` 裁决附记〔**舞说 12/20 领先**，原 15/20 霖说撤回〕; `lyq3tnc036` 放弃·已释贞人秝 16/20; `5jcghtltbx` 存疑 7/20; `gjgujysmue` 存疑 7/20; `bu3h266vxh` 放弃·贞人名 9/20; `xyp0ngvyd7` 放弃·地名 8/20; `refqnby49o` 存疑 7/20; `1yynvi0pfn` 存疑 9/20) + `reports/claude-reply-to-gemini-2026-11-26.md`（签字批准 Gemini PR #1 四项联合裁决：`0bcp` A 说撤回、`h82` & `a5t` 移入 Section A、`cdd4` 移出未释池）。
- **Muse totals on `main`**: **36 notes / 37 targets** — 成立 0, 已释移出 4 (`𠬝`, `秝`, `𰇑`, `鞀`), 专名/异体放弃 11, 存疑 22.

## Done (merged into `main` at `45775b1` & `922d24d` via PR #1 & #2 — Gemini)

- **PR #1 (`45775b1`, 2026-11-26)**: 8 cross-audit addenda, 8 standalone Gemini
  notes (9 targets), 9 PNG sheets, `docs/METHOD.md` Rule 7, `docs/EXCLUSION-LIST-2026.md`,
  5 Rule-7 interceptions (`e33`, `pmjq`, `01v0`, `dzob`, `gbjr`).
- **PR #2 (`922d24d`, 2026-11-26)**: Chinese Changelog in `README.md` + empirical
  < 50% stopping assessment for the OBIMD low-frequency tail.

## In review (PR #3 branch `gemini/wvx-deep-kaoshi-and-audits-2026-11-28` — Gemini)

*(Combined repo totals once PR #3 merges: **45 full notes / 48 targets** — **成立: 0**,
已释移出 4, 专名/异体放弃 11, 存疑 33 [22 Muse + 11 Gemini].)*

- **12 new high-res OBIMD PNG evidence sheets** (`kaoshi/images/` now totals **21**
  Gemini PNGs) + **top-of-note inline `![...](images/...)` embeds across ALL 9
  `kaoshi/gemini-*.md` notes** (先看原字图版，再读考释) + **Word (`.docx`) edition**
  at `exports/ai-deciphers-oracle-bone-gemini-kaoshi-2026-11-28.docx`.
- **Deep upgrade of `wvxqqsz1w8` (10→11/20, `存疑`) & `o7eb365hnf` (11/20, `存疑`)**
  in `kaoshi/gemini-o7eb365hnf-wvxqqsz1w8-kaoshi.md` (`H30393` Rosetta link,
  `b92fu80uys` base correction, `束+攴/敕` promoted, `敶/陳` downgraded, `H575=丙75`
  「辣」 ref) + OBIMD `1wismy95hz` (`224 clean / 172 plates`) added to `gemini-u209aa-kaoshi.md`.
- **Gemini standalone note #9** (`kaoshi/gemini-b037aq4o64-g7m9i371p4-kaoshi.md`):
  single-plate high-constraint leads `b037aq4o64` (`H30373=戩26.3`, 9/20, `存疑`) &
  `g7m9i371p4` (`H13389`, 8/20, `存疑`).
- **6 new non-destructive `## Gemini 附記（2026-11-28）` addenda** on Muse notes
  (`kbshi-bdc20-bdc1f`, `kbshi-1yynvi0pfn`, `kbshi-bu3h266vxh`, `kbshi-refqnby49o`,
  `kbshi-gjgujysmue`, `kbshi-3jzeliplnn`; 0 deleted lines across all Muse files).
- **Reconciled governance docs & handoff reply**: `README.md`, `RESULTS.md`,
  `TASKS.md`, `docs/METHOD.md` (Rule 6 HD 164 files + `眔` + same-plate facsimile
  rule), `docs/EXCLUSION-LIST-2026.md` (`e33` softened per Muse adjudication +
  new Rule-7 catches incl. `0fig5rmiox ≈ 求示` + 6 additional known UIDs), and
  `reports/gemini-reply-to-muse-2026-11-28.md`.

## Pending adjudication / Blocked (do not re-attack)

- **Pending Muse / owner joint adjudication (from Gemini 2026-11-28 addenda):**
  - `BDC20` (`nms96pmn1w`, 41 clean) & `BDC1F` (`wq47pyztal`, 19 clean) → recommended for **Section A (`牝羊` / `牡羊`, 60 tokens)** (`audit_bdc20_bdc1f_vs_yang.png`).
  - `bu3h266vxh` (`U+F9109`, 6 clean) → recommended for **Section A (师组贞人 `勺`, `H20022`)** (`audit_bu3h_shao_and_refqn_yumu.png`).
  - `1yynvi0pfn` (`U+A6D81`, 6 clean) → recommended for **Section B (unmerged duplicate of `tyazlz2ugv` `𫩀/柰/叔`, proven on same-plate `H35462`)** (`audit_1yynvi0pfn_vs_tyazlz2ugv.png`).
- **Blocked by Rule 7 (DO NOT create standalone undeciphered notes):**
  - **`0fig5rmiox`** (`U+F3206`, 5 clean / 4 片: `H14348/14349/14350/14358`) — high-risk suspected unmerged variant of `求` (`求示`, 蔡哲茂 1987; `audit_0fig5rmiox_vs_qiu.png`).
  - Newly confirmed Rule-7 known UIDs: `9c9zf6hv2z` (`掫/驟`), `97dgghy3oj` (`斝`), `ig9oetqcmy` (`麓`), `oqwz3j1hh1` (`祀`), `kk9zxal8u7` (`宋`), `xeyf2mkerf` (`柚`).
  - Earlier Rule-7 / signed exclusions: `cdd4p6xm9e` (`勺`), `a5tuvlp0po` (`鞀`), `h82z1bo3i3` (`𰇑`=`𣆑`/`冊`), `lyq3tnc036` (`秝`), `e33qe36es7` (`舞` leading — closed/do not re-attack), `pmjqw82db0` (`衛`), `01v0id7th0` (`黍`), `dzob6ag7n1` (`最/子`), `gbjr7sabn4` (`豕`).

## In progress / Standing pause policy

- **Gemini: REMAINS PAUSED on sweeping the low-frequency OBIMD tail** under the
  owner's 50% breakthrough-confidence stopping rule (2026-11-26). All `clean ≥ 6`
  viable OBIMD candidates are now attacked or intercepted. Gemini will NOT claim
  further low-frequency OBIMD tail UIDs unless new primary corpora (full 《合集》+
  《合补》+《屯南》+《花东》 transcriptions, Shang-Zhou bronzes, Warring States Chu
  slips, or physical museum/library plates) are introduced.
- **Action needed from Muse on next pull:** Run `git pull origin main` inside
  Muse's VM clone so `docs/EXCLUSION-LIST-2026.md` and `docs/METHOD.md` Rule 7
  are present locally (Muse's R35–37 notes reported the file was still absent
  in Muse's local VM clone!).

## Remaining operational & physical checks

1. **Muse 173 PNG images (`kaoshi/images/`, local commit `1831007`):**
   Still pending bundle upload/transfer from Muse's VM (`oracle-kaoshi-rounds-1-22.bundle`, 5.8 MB).
2. **Printed library & museum checks:** See `RESULTS.md` Outstanding checks
   (《合集释文》, 《丙编》75, 《花东》2003, 《新甲骨文编》, 《甲骨文字综理表》2024,
   国博 Y0699, 西周车饰铭文, 小屯南地 H24, 拉曼光谱).
