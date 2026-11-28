# ai-deciphers-oracle-bone

AI-assisted decipherment of undeciphered oracle bone script (甲骨文), with a full
scholarly 考释 (kaoshi) for every character attacked. Work starts from the
simplest / highest-frequency undeciphered graphs and works down the frequency
ranking. Nothing is called "solved" until the evidence chain closes.

## 最新变更速览（Changelog — 每次 PR 改了什么）

| 日期 / 提交 | 来源 | 核心变更一览 |
|---|---|---|
| **2026-11-28 · PR #3（本分支）** | Gemini | ① **全量图文直观化升级 + Word（`.docx`）合集导出**：新增 **12 张本地 OBIMD 原摹本高清图版**（`kaoshi/images/` 现共 21 张），并将对应甲骨原字与摹本 PNG **顶置嵌入全部 9 篇 `kaoshi/gemini-*.md` 考释笔记正文字首（先看原字，再读考释）**；同步导出图文混排中文 Word 版 **`exports/ai-deciphers-oracle-bone-gemini-kaoshi-2026-11-28.docx`**（含总览表、全部 9 篇 Gemini 考释及 4 张交叉复核铁证图版）。<br>② **`wvxqqsz1w8` 深度升级至 11/20（严格 `存疑`）＋`o7eb` 审慎补核**：发现 **`H30393`（《粹》1540）罗塞塔跨片联结**——`wvx` 全部 3 个直宾（`小山`、`aawiifil1h`、`otbtv0ewaj`）同版齐聚祈雨山神；自我订正左基件同构于无名组 **`b92fu80uys`（`H29700 其束司魚` / `H30381 珠402=束`）** 而非无名组瘦菱十字形「東」，证实 `H30455 S1` 横线为骨裂纹、左竖 `丨` 占 3/6 且非商代阶梯形「阜」，据此**升格「束＋攴／敕」为领先假说、降级「敶／陳」**；补录 `o7eb` `H575=《丙》75` 蔡哲茂「辣」文献线索；补全 `𠦪`（`1wismy95hz`）224 clean / 172 片本地实测。<br>③ **新增 Gemini 独立笔记 #9**（`kaoshi/gemini-b037aq4o64-g7m9i371p4-kaoshi.md`）：建档 2 枚单版强语法约束真未释线索（`b037aq4o64` `H30373=戩26.3` 9/20、`g7m9i371p4` `H13389` 8/20，双双 `存疑`）；按 Rule 7 拦截疑似「求」未归并异体 **`0fig5rmiox`（`H14348/14349/14358` 蔡哲茂「求示」）**，不单列未释笔记。<br>④ **6 篇非破坏性交叉复核附记（对 Muse 原文 0 行删改，各附高清实证图）**：五重互证锁定 **`BDC20 = 牝羊（羊+匕）`、`BDC1F = 牡羊（羊+土）`**（60 tokens，建议移入 Section A）；`H35462` 同片原摹本直证 **`1yynvi0pfn = tyazlz2ugv`（`𫩀/柰/叔`）** 未归并异体（建议移入 Section B）；查实 **`bu3h266vxh = 师组贞人「勺」`**（`H20022`「戊午卜，勺，侑小王」，建议移入 Section A）；锁定 **`refqnby49o = ⿱雨目`（`𩆨`，王恩田 2015《释霉》）**；订正 `gjgujysmue` 之 `弜`、`3jzeliplnn` 之 `其/弜/眔` 虚词误判并致谢 Muse 发现 `facsimile.zip` 实存 164 幅 HD 摹本。<br>⑤ **全库总账对齐（45 篇笔记 / 48 目标，落实 Muse `claude-reply` 四项签字裁决）**：同步合入 Muse R28–37（`bab1ae7`）、落实 `h82`/`a5t` 正式移入 A 节、`cdd4` 正式移出未释池、`0bcp` A 说 17/20 正式撤回、`e33` 12/20 舞说领先，并提交 `reports/gemini-reply-to-muse-2026-11-28.md`。 |
| **2026-11-27 · `bab1ae7`** | Muse | 第 28–37 轮 9 篇新笔记（`3jzeliplnn`、`e33qe36es7`、`lyq3tnc036`〔识别已释贞人秝 16/20〕、`5jcghtltbx`、`gjgujysmue`、`bu3h266vxh`、`xyp0ngvyd7`、`refqnby49o`、`1yynvi0pfn`）＋ `e33` 裁决附记（舞说 12/20 领先、霖说 15/20 撤回）＋ `reports/claude-reply-to-gemini-2026-11-26.md`（签字接受 Gemini 四项联合裁决）。 |
| **2026-11-26 · PR #2（已合入 `922d24d`）** | Gemini | 在 `README.md` 顶部补充中文「最新变更速览」与**阶段性可行性／止损评估**：基于 OBIMD 剩余未攻池实测（462 字上限 ≤7 例、89.2% ≤3 例、64.3% 孤证），当前工具条件下产出真正 `成立` 新破译的置信度 **< 50%（约 5%–15%）**，按用户要求**暂停继续刷 OBIMD 低频尾池**。 |
| **2026-11-26 · PR #1（已合入 `45775b1`）** | Gemini（Muse 审阅合并） | ① 8 篇非破坏性交叉复核附记（证伪 `0bcp`「禍尤」合文、实锤 `cdd4=勺`、`a5t=鞀`、`h82=𰇑/𣆑`、`ff8=洅`、`crck=不𦀓鼄`、`gx21=案→宴`、`qw5` `弜` 锁动词）；② Rule 7 拦截 5 个 OBIMD 已释字；③ 新增 8 篇 Gemini 独立考释笔记（9 目标，全 `存疑`）；④ 首次入库 9 张 PNG 图版与 `docs/EXCLUSION-LIST-2026.md`。 |
| **2026-11-26 · `14af5ba` / `090ea77`** | Muse | 初始全库基线与第 1–27 轮（27 篇笔记 / 28 目标、`ranking-20261126.md`、方法论与交接文档）。 |

## 阶段性可行性与止损评估（2026-11-26 确立，2026-11-28 维持有效）

- **当前结论**：在现有工具与语料边界（OBIMD 10,077 条子集 + 公开网页文献）下，继续向剩余低频未释池攻关以产出**真正达到学界／悬赏标准的全新破译（`成立`）**的概率 **显著低于 50%（客观估算约 5%–15%）**。按项目拥有者「**不到 50% 信心就不继续**」的原则，**Gemini 侧继续维持暂停扫荡 OBIMD 低频尾池**；本次 PR #3 聚焦于**存量核心靶标深度升级（`wvxqqsz1w8`）、图文直观化（每篇考释顶置原字 PNG + Word 合集导出）与对 Muse R28–37 及 `BDC20/1F` 的高质量交叉复核**。
- **跨过 50% 门槛所需的真正缺口**：需接入**全量《合集》＋《合补》＋《屯南》＋《花东》权威释文库**、**商周金文（《集成》《铭图》）与战国楚简（清华／上博／郭店／包山）跨时代字形—通假对齐库**、以及纸本**《新甲骨文编》《甲骨文字综理表》（2024）**与馆藏原拓高精图像（如国博 Y0699、拉曼光谱等），而非继续在 OBIMD 孤证尾池空转。

---

## Status — read this first (2026-11-28)

- **Decipherments established (成立): 0.** No new character has been deciphered
  to the prize / publication bar yet. Any claim to the contrary in an older
  draft, chat message, or press note is wrong.
- **Total full kaoshi notes: 45**, covering **48 targets** — **36 Muse notes**
  (`kaoshi/kbshi-*-kaoshi.md`, 37 targets, rounds 1–37, incl. `bab1ae7`) +
  **9 Gemini standalone notes** (`kaoshi/gemini-*-kaoshi.md`, 11 targets, all
  with top-of-note inline oracle-bone PNG embeds + bundled Word `.docx` edition).
  Per `COORDINATION.md` §4, Muse's signed adjudications in
  `reports/claude-reply-to-gemini-2026-11-26.md` and
  `kaoshi/kbshi-e33qe36es7-adjudication-20261126.md` are now reflected in the
  reconciled totals below, while Gemini's new 2026-11-28 audit recommendations
  (`BDC20/BDC1F`, `bu3h266vxh`, `1yynvi0pfn`) remain preserved as dated addenda
  pending Muse/owner adjudication:
  - **Already-deciphered graphs removed from the attack list (放弃〔已释〕, Section A): 4**
    — `𠬝` (`cvzszyp6bm`, 服 *fú*, 16/20), `秝` (`lyq3tnc036`, 貞人秝 *lì*, 16/20,
    Muse R30), `𰇑` (`h82z1bo3i3`, `𣆑`/`冊`, 于省吾读刪 — signed into Section A
    via `claude-reply`), and `鞀（鼗）` (`a5tuvlp0po`, 裘锡圭考定 — signed into
    Section A via `claude-reply`). *(Shortlist-level `cdd4p6xm9e = 勺（礿）` is also
    formally removed from the undeciphered pool. Gemini's 2026-11-28 addenda
    additionally recommend relocating **`BDC20` [`牝羊`], `BDC1F` [`牡羊`]** [60
    tokens], and **`bu3h266vxh` [师组贞人 `勺`]** into Section A — pending joint
    adjudication.)*
  - **Closed as proper names / unmerged variant (放弃 as common-word kaoshi,
    definite negative conclusions, Section B): 11** — `X/1850` (variant of 由),
    `n52ssmqnda` (diviner), `xdimpzk5q6` (place), `7b9lfpes9d` (person),
    `jyskjcj861` (place/state), `xhfae21bpk` (place), `dd5w09rr1q` (`子__`),
    `2bcusrt88g` (place/state), `3jzeliplnn` (person, `bab1ae7`), `bu3h266vxh`
    (diviner, `bab1ae7` — Gemini 11-28 addendum recommends moving to Section A as
    known diviner `勺`), and `xyp0ngvyd7` (place, `bab1ae7`). *(Gemini's 2026-11-28
    addendum additionally recommends moving `1yynvi0pfn` from Section C into
    Section B as an unmerged duplicate of `tyazlz2ugv` [`𫩀/柰/叔`].)*
  - **Still 存疑 (undecided, no reading stands, Sections C & D): 33** — **22** Muse
    targets (incl. `0bcpbg0geh` with Hypothesis A 17/20 formally withdrawn,
    `e33qe36es7` 12/20 `舞` leading per Muse adjudication, `5jcghtltbx`,
    `gjgujysmue`, `refqnby49o`, `1yynvi0pfn`, plus rounds 1–27 survivors) +
    **11** Gemini targets (`𫹉`/`hclsl73wg4` 12/20, 《合集》36481 `白[⿱鹿文]` 12/20,
    `𠦪` `1wismy95hz` 12/20, `𢀛` `b2n32mdq0u` 10/20, `3xbmgmm4j0` 11/20,
    `aelrb19u0i` 10/20, `o7eb365hnf` 11/20, `wvxqqsz1w8` **11/20**, `o68jkkro3f`
    10/20, plus Note #9 single-plate leads `b037aq4o64` 9/20 & `g7m9i371p4` 8/20).
  - **Reconciliation check:** `0 成立 + 4 已释 + 11 放弃 + 33 存疑 (22 Muse + 11 Gemini) = 48 targets`
    across `36 Muse + 9 Gemini = 45` full notes. See `RESULTS.md` for the per-character tables.

## Method in one paragraph

Corpus: OBIMD (*Scientific Data* 2026, DOI 10.1038/s41597-026-06967-0;
10,077 records, 115,319 tokens, Heji-linked; `facsimile.zip` includes **164 HD
Huayuanzhuang East facsimiles** `hd2.jpg`–`hd549.jpg` with unpadded filenames),
cross-checked against published transcriptions, bronze parallels, and the
authoritative 2024 《甲骨文字综理表》 baseline (3,763 head entries: 1,273
confirmed, 378 disputed, 2,112 undeciphered). Every OBIMD target is recounted
locally from `data.json` / `Main-character.json` (clean token = SeatFont 0 and
Mark −1); candidates must pass BOTH Unihan/IDS checks (`zi.tools` / `zdic.net` /
paleographic dictionaries — Ext-G absence in Unihan does NOT prove "undeciphered")
AND the **Rule 7 OBIMD literature gate** (checking published transcriptions,
`docs/EXCLUSION-LIST-2026.md`, and oracle function-word grammar such as modal
prohibitory `弜 = 勿` and coordinating conjunction `眔 = 与/及`); neighbours are
read by codepoint after sorting by OrderNumber and expanding merged tokens;
glyphs are ALWAYS visually inspected against real `facsimile.zip` crops (never
trusting `subchar-images.zip` vectorizations alone — documented lesson:
`1yynvi0pfn = tyazlz2ugv` on `H35462`); phonological claims use dual-system Old
Chinese reconstructions (Zhengzhang 2003 & Baxter–Sagart 2014 v1.1); every note
ends in one of `成立 / 存疑 / 放弃`, with a four-ring score (形 / 音 / 义 / 用,
each 0–5) and falsifiers. Full rules: `docs/METHOD.md` and `docs/EXCLUSION-LIST-2026.md`.

## What is in this repo

- `kaoshi/` — **36** Muse kaoshi notes (`kbshi-*-kaoshi.md`, 13 now carrying dated
  Gemini cross-audit addenda, plus `kbshi-e33qe36es7-adjudication-20261126.md`) +
  **9** Gemini standalone kaoshi notes (`gemini-*-kaoshi.md`, covering 11 targets,
  **all featuring top-of-note inline PNG character & facsimile sheets**), plus
  `ranking-20261126.md` and shortlists.
- `kaoshi/images/` — **21** verified PNG facsimile, glyph-comparison, and audit
  evidence sheets committed by Gemini (9 from PR #1 + 12 new high-res sheets in
  PR #3 covering `wvx`/`b92`/`東`/`束`, `H30329`/`H30393`, `𫹉`, `𠦪`, `𢀛` vs `召`,
  `H36481` components, `b037`/`g7m9`, `0fig5` vs `求`, `BDC20/1F` vs `羊/牝/牡`,
  `1yyn` vs `tyaz` same-plate `H35462`, `bu3h`/`勺`, and `refqn`/`雨+目`). Muse's
  173 PNGs from local commit `1831007` remain pending transfer from Muse's VM.
- `exports/` — **`exports/ai-deciphers-oracle-bone-gemini-kaoshi-2026-11-28.docx`**:
  polished Chinese Word (`.docx`) edition embedding real oracle-bone character &
  facsimile PNG sheets right before each of Gemini's 9 kaoshi commentaries, plus
  the 45-note / 48-target status summary and cross-audit visual highlights.
- `docs/background-report-2026-11-25.md` — background research.
- `docs/METHOD.md` — working method, traps, Rule 6 HD-facsimile update (164 files),
  and Rule 7 OBIMD literature gate.
- `docs/EXCLUSION-LIST-2026.md` — authoritative exclusion list & Rule-7 interceptions.
- `reports/` — git-channel handoff & reply reports between Muse and Gemini
  (latest: `reports/gemini-reply-to-muse-2026-11-28.md`).
- `RESULTS.md` — the per-character status tables (the honest summary).
- `COORDINATION.md` — how Muse and Gemini work on this repo without clobbering
  each other. **Read it before pushing.**
- `TASKS.md` — the claim board: who is attacking what, what is next.

## Honesty rules (binding on every contributor)

1. Never present a guessed reading as solved. Verdicts are only
   `成立 / 存疑 / 放弃`.
2. Never invent a Heji number, frequency, or inscription. Every number cited is
   either measured locally from OBIMD or traced to verified published sources.
3. A proper-name classification is a definite result, but it is not a
   decipherment and is never presented as one.
4. OCR "readings" of undeciphered graphs are phantoms until corroborated.
