# ai-deciphers-oracle-bone

AI-assisted decipherment of undeciphered oracle bone script (甲骨文), with a full
scholarly 考释 (kaoshi) for every character attacked. Work starts from the
simplest / highest-frequency undeciphered graphs and works down the frequency
ranking. Nothing is called "solved" until the evidence chain closes.

## 最新变更速览（Changelog — 每次 PR 改了什么）

| 日期 / 提交 | 来源 | 核心变更一览 |
|---|---|---|
| **2026-11-26 · PR #2（本分支）** | Gemini | 在 `README.md` 顶部补充中文「最新变更速览」与**阶段性可行性／止损评估**：基于 OBIMD 剩余未攻池实测（462 字上限 ≤7 例、89.2% ≤3 例、64.3% 孤证），当前工具条件下产出真正 `成立` 新破译的置信度 **< 50%（约 5%–15%）**，按用户要求**暂停继续刷 OBIMD 低频尾池**，同步更新 `TASKS.md` 与 `reports/gemini-handoff-2026-11-26.md`。 |
| **2026-11-26 · PR #1（已合入 `45775b1`）** | Gemini（Muse 审阅合并） | ① **8 篇非破坏性交叉复核附记**（对 Muse 原笔记 0 行删改）：证伪 `0bcpbg0geh`「禍尤」合文说并闭环 `U+B6AF4` 码位；本地 10 幅摹本实锤 `cdd4p6xm9e = 勺（礿）`；查实 Muse R26 `a5tuvlp0po = 裘锡圭「鞀」`、R8 `h82z1bo3i3 = 𰇑（𣆑/冊）`；锁定 `ff8rp0nh6u = 洅`（及 `匸丙 = 報丙`）、`crck62eltz = 不𦀓鼄`、`gx21ndp7yy = 王宁「案→宴」`、`qw5vx1k0rw` 禁止副词 `弜` 锁动词。<br>② **Rule 7 预筛拦截 5 个 OBIMD 未归并已释字**：`e33qe36es7 = 舞`（原 Muse 下轮 #2！）、`pmjqw82db0 = 衛`、`01v0id7th0 = 黍`、`dzob6ag7n1 = 最/子`、`gbjr7sabn4 = 豕`。<br>③ **新增 8 篇 Gemini 独立考释笔记（覆盖 9 个目标，全部严格 `存疑`）**：`𫹉`（452 clean 本地全槽实测）、《合集》36481 `白[⿱鹿文]`、`𠦪`、`𢀛方`（`𢀛` vs `召` 分期互补首测），以及 5 个附全套原摹本裁图的真未释字 `3xbmgmm4j0`、`aelrb19u0i`、姊妹同基字组 `o7eb365hnf`（`東+戉`）& `wvxqqsz1w8`（`東+攴`）、`o68jkkro3f`。<br>④ **首次入库 9 张本地实测 PNG 图版**（`kaoshi/images/`），新增 `docs/METHOD.md` Rule 7 与 `docs/EXCLUSION-LIST-2026.md`。 |
| **2026-11-26 · `14af5ba`** | Muse | 第 23–27 轮（5 篇新笔记：`npykxas4c8`、`dd5w09rr1q`、`bh6mqc68g2`、`a5tuvlp0po`、`2bcusrt88g`），全库二次重排。 |
| **2026-11-26 · `090ea77` / `b8e1842`** | Muse | 初始全库基线（第 1–22 轮 22 篇笔记 / 23 目标、`ranking-20261126.md`、方法论与交接文档）。 |

## 阶段性可行性与止损评估（2026-11-26 — 按 50% 信心阈值暂停攻关）

- **当前结论**：在现有工具与语料边界（OBIMD 10,077 条子集 + 公开网页文献）下，继续向剩余低频未释池攻关以产出**真正达到学界／悬赏标准的全新破译（`成立`）**的概率 **显著低于 50%（客观估算约 5%–15%）**。按项目拥有者「**不到 50% 信心就不继续**」的原则，**Gemini 侧现暂停继续扫荡 OBIMD 低频尾池**。
- **量化依据（OBIMD `data.json` 本地实测）**：
  1. **已攻高优池破译率 `0 / 37`**：双方已完成全部 `clean ≥ 8` 的高价值候选与 5 个 5–7 例真未释动词，最佳成果稳定在 10–12/20（`存疑`），证实仅靠 OBIMD 可以精准锁死「形」与「义／用」槽位，但**无法闭合「音」环与商→周→战国→《说文》演变链**。
  2. **剩余 462 个未攻 UID 频次断崖**：`clean = 7` 仅 **4 字**、`6` 仅 **6 字**、`5` 仅 **13 字**、`4` 仅 **27 字**、`3` 为 **45 字**、`2` 为 **70 字**、`1`（孤证）高达 **297 字（64.3%）**——即 **89.2%（412/462）样本量 ≤ 3 例**，且前 20 名中绝大多数呈显性专名槽（`卜__貞`、`子__`、`于__`、`在__`、`伐__`、`帚__`）或未归并已释异体。
  3. **跨过 50% 门槛所需的真正缺口**：需接入**全量《合集》＋《合补》＋《屯南》＋《花东》权威释文库**、**商周金文（《集成》《铭图》）与战国楚简（清华／上博／郭店／包山）跨时代字形—通假对齐库**、以及纸本**《新甲骨文编》《甲骨文字综理表》（2024）**与馆藏原拓高精图像（如国博 Y0699、拉曼光谱等），而非继续在 OBIMD 孤证尾池空转。

---

## Status — read this first (2026-11-26)

- **Decipherments established (成立): 0.** No new character has been deciphered
  to the prize / publication bar yet. Any claim to the contrary in an older
  draft, chat message, or press note is wrong.
- **Total full kaoshi notes: 35**, covering **37 targets** — **27 Muse notes**
  (`kaoshi/kbshi-*.md`, 28 targets, rounds 1–27) + **8 Gemini standalone notes**
  (`kaoshi/gemini-*.md`, 9 targets). Per `COORDINATION.md` §4, Muse's original
  verdicts are preserved untouched pending Muse/owner adjudication of Gemini's
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

## Honesty rules (binding on every contributor)

1. Never present a guessed reading as solved. Verdicts are only
   `成立 / 存疑 / 放弃`.
2. Never invent a Heji number, frequency, or inscription. Every number cited is
   either measured locally from OBIMD or traced to verified published sources.
3. A proper-name classification is a definite result, but it is not a
   decipherment and is never presented as one.
4. OCR "readings" of undeciphered graphs are phantoms until corroborated.
