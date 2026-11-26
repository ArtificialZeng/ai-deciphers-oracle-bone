# Results — per-character status (2026-11-26)

Source of truth for each row is the kaoshi note in `kaoshi/`. Scores are
形 / 音 / 义 / 用 (each 0–5, total /20). "—" means the note does not state a
total; read the note. **成立: 0.**

**Accounting & ownership note (per `COORDINATION.md` §4):**
- **Total full kaoshi notes: 26** (**22** Muse `kaoshi/kbshi-*.md` covering **23** targets + **4** Gemini `kaoshi/gemini-*.md` covering **4** targets = **27 targets** total).
- **Combined verdicts (preserving Muse's original verdicts pending owner adjudication of Gemini's 2026-11-26 audit addenda):**
  - **成立 (Established): 0**
  - **放弃（已释，移出攻击名单）: 1** (Muse: `𠬝`; Gemini cross-audit additionally recommends moving `h82z1bo3i3` [`𰇑` = `𣆑`/`冊`] to 已释 and documents refutation of `0bcpbg0geh` Hypothesis A `"禍尤"` ligature)
  - **放弃（专名／未并入异体定性，非破译）: 6** (Muse)
  - **存疑 (Undecided): 20** (16 Muse + 4 Gemini)
  - **Reconciliation check:** `0 + 1 + 6 + 20 = 27` targets across `22 + 4 = 26` full notes.

---

## A. Muse rounds 1–22 — Already deciphered, removed from the attack list (1)

| Target | Tokens | Verdict | Note |
|---|---|---|---|
| 𠬝 (cvzszyp6bm) | 41 / 36 片 | 放弃（已释）— 服的初文，读 *fú*，16/20 | `kbshi-cvzszyp6bm-kaoshi.md` |

*(Pending owner adjudication from Gemini 2026-11-26 audit: `h82z1bo3i3` [`𰇑` = `𣆑`/`冊`] is recommended for relocation from Section C into Section A; shortlist-level `cdd4p6xm9e` [140 例] is recommended for removal from the EMPTY pool as `勺（礿）` once Muse confirms local facsimiles.)*

## B. Muse rounds 1–22 — Closed as proper names / unmerged variant, definite negative conclusions (6)

| Target | Tokens | Classification | Score | Note |
|---|---|---|---|---|
| X/1850 | 61 例 | 由的未并入异体 | — | `kbshi-x1850-kaoshi.md` |
| n52ssmqnda | 35 / 34 片 | 贞人名；槽位订正为“卜 __ 貞”非“卜 __ 鼎” | 9/20 | `kbshi-n52ssmqnda-kaoshi.md` |
| xdimpzk5q6 | 14 / 6 片，全花东 | 地名；14 例全居在/才、自之后，“入自 __”与“入自西”逐字平行 | 8/20 | `kbshi-xdimpzk5q6-kaoshi.md` |
| 7b9lfpes9d | 9 / 9 片 | 人名（武丁期军事人物，与光平行），排除法收敛 | 8/20 | `kbshi-7b9lfpes9d-kaoshi.md` |
| jyskjcj861 | 12 / 10 片 | 地名/方国名；“來 自 __”一槽排他性为决定性证据 | 8/20 | `kbshi-jyskjcj861-kaoshi.md` |
| xhfae21bpk | 8 / 7 片 | 地名（田猎地/祈祷地；地方神名不能排除） | 9/20 | `kbshi-xhfae21bpk-kaoshi.md` |

Shortlist-level (no full note):
- `2lep30tiiz` (71 例，人名), `tq26tb9tj9` / `5i4ba39u9k` / `yo5h3qdl2s` (地名/先妣名).
- **`cdd4p6xm9e` (140 例，原短表判“最可能专名” — Gemini 2026-11-26 附记重大反转):** 已刊布释文《合集》313 (`佑勺岁于唐`)、《合集》380 (`〔之〕勺于且乙`) 及平行句《合集》5157 (`王賓武乙升伐，亡尤`) 表明其几乎肯定**非专名**，而是已释祭祀动词 **`勺（礿）`**（OBIMD 中或与 `升` 混并）；待 Muse 本地核验 `std_cdd4p6xm9e.png` 及 H35378/35383/35436 摹本。详见 `kaoshi/ranking-20261126.md` Gemini 附记。

## C. Muse rounds 1–22 — Still 存疑 (16; original Muse verdicts preserved, Gemini 2026-11-26 audit addenda noted)

| Target | Tokens | Muse leading hypothesis (original) | Score | Gemini 2026-11-26 audit addendum | Note |
|---|---|---|---|---|---|
| ⟨礻+升⟩ | 1 例（孤证） | 存疑异写：更可能是升加义符的异写，非新字 | — | — | `kbshi-sheng-kaoshi.md` |
| gx21ndp7yy | 54 / 43 片 | 名词，兆物类；主槽“鼎王叀吉”约 30 例 | — | **附记**：检出王宁《說甲骨文中的“案”》（`案→宴` 释 H5254/5280）；花东 HD290/454/475「見用」槽未验，仍 `存疑` | `kbshi-gx21ndp7yy-kaoshi.md` |
| fi0wiw1adi | 13 / 10 片，全花东 | 白色可数牲畜（首选假说，物种未定）；形义冲突 | 形2 音0 义3 用3 | — | `kbshi-fi0wiw1adi-kaoshi.md` |
| BDC20 | 41 / 25 片，全花东 | 可数祭品（牲畜/谷物未定）；HD243 与 BDC1F 并列各数五，证实非同词 | — | — | `kbshi-bdc20-bdc1f-kaoshi.md` |
| BDC1F | 19 / 17 片 | 同上，较弱 | — | — | `kbshi-bdc20-bdc1f-kaoshi.md` |
| 0bcpbg0geh | 112 / 55 片 | 原最强假说：禍+尤合文，读“禍尤”，“旬亡禍尤” | 17/20 | **附记（触发 §8 证伪条件 1）**：《合集》35399/35401/35530 刊布释文一律作**单字「禍/憂」**，绝无「禍尤」→ **A 说合文证伪，B 说第五期黄组单字繁化异体胜出**；另提示 `ff8` 附录 `𫴒` (`U+2BD12`) 编码差异 | `kbshi-0bcpbg0geh-kaoshi.md` |
| crck62eltz | 31 独＋9 併（共 40 例） | 动词未定：知觉动词+鼄 vs 移动动词+地名鼄 | 8/20 | **附记**：锁定为武丁宾组百年悬案 **`不𦀓鼄`**（`𦀓` `U+26013`，`⿰糹辛`；杨向奎 1955 vs 陈光宇 2012/2020）；补双系古音与拉曼光譜证伪，仍 `存疑` | `kbshi-crck62eltz-kaoshi.md` |
| h82z1bo3i3 | 94 / 89 片 | 动词/器物名未定；平台隶定 𰇑 原判仅形码 | 7/20 | **附记（建议移入 A 节已释）**：`zi.tools`/汉典/王辉《古文字通假字典》(p. 263) 证实 `𰇑`=`⿱册口` = 《说文》**`𣆑` (`U+23191`)/`冊`**（于省吾读「刪」），吻合 H886/H908/H31137 刊布释文 | `kbshi-h82z1bo3i3-kaoshi.md` |
| qw5vx1k0rw | 19 / 16 片 | 祭祀动词 vs 祭品名词，两说互斥 | 7/20 | **附记**：订正 `H32545 S2` `弜 __`——`弜` 为禁止副词「勿/不要」，**排除祭品名词说、锁定祭祀动词**；读音未定，仍 `存疑` | `kbshi-qw5vx1k0rw-kaoshi.md` |
| gtysuhhw3p | 17 / 13 片 | 移动动词领先 | 7/20 | — | `kbshi-gtysuhhw3p-kaoshi.md` |
| ff8rp0nh6u | 40 / 33 片 | 祭祀动词或“協”类连词；与協共享两排他性语槽 | 9/20 | **附记**：**100% 锁定为晚商周祭五祀第四祀 `洅`（`洅`/`𣫭`/`載`）**，并解开 §6.5 `匸丙` = **`報丙`**；本源构形与今字仍争议，维持 `存疑` | `kbshi-ff8rp0nh6u-kaoshi.md` |
| 4a6130bz6w | 14 / 10 片，全花东 | 动词领先（巳/子₂之后只接动词，花东子₂+人名式为合集例、互补分布） | 7/20 | — | `kbshi-4a6130bz6w-kaoshi.md` |
| 4zv87269nu | 12 / 12 片 | 徠 lái 有三重反证；穀物名词说保留 | 7/20 | — | `kbshi-4zv87269nu-kaoshi.md` |
| wpbo51inbu | 9 / 6 片 | 动词已定，无具体读法；OCR 读作“動”已证伪为幻影 | 7/20 | — | `kbshi-wpbo51inbu-kaoshi.md` |
| rp1zjtuksu | 11 / 7 片（9 clean） | 动词/人名并列领先；子形与槽位完全相关，一字还是两字未决 | 7/20 | — | `kbshi-rp1zjtuksu-kaoshi.md` |
| diesgffg1o | 9 / 9 片 | 和说三重反证；人名说与全部 9 例相容但无一例可证实 | 7/20 | — | `kbshi-diesgffg1o-kaoshi.md` |

## D. Gemini standalone kaoshi notes (2026-11-26) — Still 存疑 (4)

| Target | Corpus / Frequency | Core finding & status (verdict strictly `存疑`) | Score (形/音/义/用) | Note |
|---|---|---|---|---|
| **`𫹉`** (`U+2BE49`, `⿰酉彡`, OBIMD `hclsl73wg4`) | OBIMD 453 例 / 全语料 ~2,000+ 例 | 商代高频酒祭动词（《合集》22159/27167/10076、小屯南地 H24、西周《繁卣》）；梳理朱凤瀚（2002）与吴俊德（2014「酬/醻」说）及双系上古音；待 Muse 本地 453 例全槽统计 | **12/20** (3/2/3/4) | `gemini-hclsl73wg4-youshan-kaoshi.md` |
| **《合集》36481 `白[⿱鹿文]`**（电子权代 `𪊓` `U+2A293` `⿸鹿文`） | 《合集》36481（国博 Y0699）＋金文《伯其父簠》等 | 双系上古音证伪阳部「慶」说；提出分层假说——**字源释 `麐`（从鹿文声），辞例读被俘危方方伯人名 `伯麐`**（与 `伯印`、`髦` 排比）；待国博 Y0699 原骨微距验「文」vs「心」 | **12/20** (3/4/3/2) | `gemini-heji36481-luwen-kaoshi.md` |
| **`𠦪`** (`U+209AA`, 《说文》呼骨切) | 《合集》63/10067/10076/14368 ＋《献侯鼎》《叔簋》《叔夨方鼎》 | 梳理冀小军（1991 改夲声释禱）→ 董莲池（2008）→ 刘云（2022 祈求 vs 告事）vs「大祓」说双系上古音；提出决定性证伪点——检核金文车饰词属幽部 `燾/幬` 还是物部 `笰/茀` | **12/20** (3/2/3/4) | `gemini-u209aa-kaoshi.md` |
| **`𢀛`** (`U+2201B`, `𢀛方`) | 武丁期战争卜辞高频（代表例《合集》6057 正） | 第四阶方国专名警示案例；澄清六派假说（邛/共/曷/棹→召/銚/築/鬼方）纯粹双系上古音，提出 `𢀛方` vs `召方` 四维定量共现矩阵验证蓝图 | **10/20** (2/1/3/4) | `gemini-u2201b-gongfang-kaoshi.md` |

## E. Counts (for orientation, not a result)

- **Authoritative 2024 baseline — 《甲骨文字综理表》 (2024, 中西书局):**
  **3,763** deduplicated head entries = **1,273** confirmed deciphered +
  **378** disputed + **2,112** undeciphered. See `docs/EXCLUSION-LIST-2026.md`.
- Earlier survey ranges (for comparison with `docs/background-report-2026-11-25.md`):
  ~4,500–4,600 distinct single characters; ~1,500 loosely deciphered;
  ~1,170 strictly confirmed in Liu Zhao 2014. "接近 6000" = 《甲骨文字形表》
  6,211 glyph entries (4,024 single characters + 2,187 variants) — a
  glyph-entry count, not a single-character count.
- OBIMD pools: 1,159 EMPTY + 820 PUA-only UIDs; 490 UIDs still had clean
  tokens > 0 after Muse's rounds 1–22 (must now pass `docs/METHOD.md` Rule 7
  literature gate). Active claims (see `TASKS.md`): Muse `npykxas4c8`;
  Gemini `hclsl73wg4` (`𫹉`), `dd5w09rr1q`, `bh6mqc68g2`.

## Outstanding checks (library / museum / local OBIMD work)

1. **Local OBIMD checks (Muse VM, see `reports/gemini-handoff-2026-11-26.md` §3):**
   `hclsl73wg4` 453-token full slot census; `std_cdd4p6xm9e.png` & H313/380/35378/35383/35436
   crops (`勺` vs `升`); `0bcpbg0geh` `U+B6AF4` vs `𫴒` (`U+2BD12`) data-hygiene audit;
   hand off 173 PNG images (`kaoshi/images/`).
2. **Printed 《合集》 Vol. 12 (`H35398–H35911`) & 《新甲骨文编》:**
   Although published transcriptions of H35399/H35401/H35530 already refute
   the `0bcpbg0geh` `"禍尤"` ligature, full 55-plate print verification
   (including H35426) and 《新甲骨文编》 headword lookups remain useful.
3. **《殷墟花园庄东地甲骨》 (2003) & Zhu Qixiang 《校釋》:**
   Especially testing 王宁's `案→宴` reading of `gx21ndp7yy` on HD290/454/475,
   plus `fi0wiw1adi`, `BDC20/BDC1F`, `xdimpzk5q6`, `4a6130bz6w`.
4. **Physical & specialist-plate falsifiers for Gemini's standalone notes & audits:**
   - National Museum Y0699 high-res macro check (`白[⿱鹿文]` lower radical `文` vs `心`).
   - Western Zhou chariot-ornament inscription check for `𠦪` (`燾/幬` vs `笰/茀`).
   - 1980 《小屯南地甲骨》 H24 plate check for `[甲寅，酉彡五牢]`.
   - Raman HgS cinnabar spectroscopy & 3D crack-morphology statistics on `不𦀓鼄` bones (《合集》10229 / 甲3339, 《丙》28/30).
5. **《甲骨文字综理表》 (2024)** per-entry lookup; spot-check OBIMD Heji mapping
   at H5250 and H30528 against printed 《合集》.
