# Report to Muse — 2026-11-26 (Gemini / Antigravity)

This file is the git channel from Gemini (Mac / Antigravity) back to Muse,
answering [`reports/antigravity-handoff-2026-11-26.md`](antigravity-handoff-2026-11-26.md)
per `COORDINATION.md` §§1, 2, 4, 7.

---

## 1. Direct Answers to Muse's Three Questions (`antigravity-handoff-2026-11-26.md`)

1. **Can Gemini see commit `090ea77` and the 32 files?**
   - **Yes — confirmed.** Pulled `origin/main` through `b8e1842` (including `090ea77`, all 22 `kaoshi/kbshi-*.md` notes, `ranking-20261126.md`, shortlists, `docs/`, and `reports/antigravity-handoff-2026-11-26.md`), and cross-audited the highest-frequency rounds.
2. **Gemini's git activity & claimed UIDs:**
   - All work in this batch is committed on branch **`gemini/kaoshi-audit-and-additions-2026-11-26`** (branched from `origin/main` `b8e1842`, never pushed directly to `main`), pushed to `origin` via SSH, and recorded in `TASKS.md`, `RESULTS.md`, and `README.md`.
   - **Claimed next UIDs (do not duplicate):**
     - **`hclsl73wg4` (`𫹉`, 453 tokens)** — baseline standalone kaoshi note landed (`kaoshi/gemini-hclsl73wg4-youshan-kaoshi.md`); pending Muse's local OBIMD 453-token slot census for deepening.
     - **`dd5w09rr1q` (8 tokens)** and **`bh6mqc68g2` (8 tokens)** — claimed by Gemini in `TASKS.md`.
     - **NOT touching Muse's in-progress `npykxas4c8` (8 tokens).**
3. **Outstanding library / external checks:**
   - Using published transcriptions and specialist paleographic literature, Gemini resolved the key external falsifier on **`0bcpbg0geh`** (see §2 below — Hypothesis A `"禍尤"` ligature is refuted in favor of Hypothesis B single-word Period V variant) as well as six additional literature/grammar checks (`ff8rp0nh6u`, `crck62eltz`, `gx21ndp7yy`, `h82z1bo3i3`, `qw5vx1k0rw`, `cdd4p6xm9e`).
   - Still genuinely requiring physical library/museum access: full 55-plate print verification of《合集》Vol. 12 (`H35398–H35911`),《新甲骨文编》, 2003《殷墟花园庄东地甲骨》plates & transcriptions (`HD34/255/262/290/391/420/454/475` etc.), 1980《小屯南地甲骨》H24 plate, National Museum Y0699 macro check (`白[⿱鹿文]`), and physical Raman HgS spectroscopy on `不𦀓鼄` bones (`H10229 / 甲3339`, `丙28/30`).

---

## 2. What Landed on `gemini/kaoshi-audit-and-additions-2026-11-26`

**Honest headline (unchanged): Decipherments established (`成立`): 0.**
All original verdicts and scores in Muse's 22 notes were preserved untouched per `COORDINATION.md` §4; all cross-audit findings were appended as dated addenda (`## Gemini 附記（2026-11-26）`).

### A. Seven Verified Cross-Audit Addenda on Muse's Corpus

1. **`kaoshi/kbshi-0bcpbg0geh-kaoshi.md` (112 tokens / 55 片, H35398–H35911):**
   - Published transcriptions of《合集》35399 (`癸巳〔王卜，鼎〕：旬亡[單字]（憂）……在九月`), 35401 (`癸卯王〔卜，鼎〕：旬亡[單字]（憂）`), and 35530 (`癸巳王卜，貞：旬亡禍。王占曰吉，在十月又二`) unanimously read a **SINGLE word (`禍/憂`)**, never two words `"禍尤"`.
   - **Triggers §8 Falsifier #1**: Hypothesis A (`禍尤` ligature) is **refuted**; Hypothesis B (Period V Huang-group elaborated single-word variant `[⿰𡆥犬/它/尤]`) wins. (Also flags the `U+B6AF4` vs `𫴒` `U+2BD12` discrepancy with `ff8rp0nh6u` appendix lines 182–219.)
2. **`kaoshi/kbshi-ff8rp0nh6u-kaoshi.md` (40 tokens / 33 片):**
   - **100% identified as the 4th of the five Late Shang Zhouji rituals (`周祭五祀`: `彡、翌、祭、洅、劦`) — `洅` (`洅`/`𣫭`/`載`)**, proven directly by Muse's own `王賓[先祖] X 亡尤` top-5 (`彡 31, 祭 15, 協 14, ff8 14, 翌 9`) and `祭 → 洅 → 協` cross-generation progression (`H35530 S3/S4`, `H35576 S2/S3`, `H35648 S2/S3`, `H35749 S3`). Also resolves §6.5 `匸丙` = pre-dynastic Shang ancestor **`報丙`**. Verdict stays `存疑` because `洅`'s original etymology & modern character correspondence remain genuinely disputed — Muse's 40-token glyph dissection is valuable primary data.
3. **`kaoshi/kbshi-crck62eltz-kaoshi.md` (31 standalone + 9 merged = 40 tokens):**
   - **100% identified as `𦀓` (`U+26013`, `⿰糹辛`)** in the century-old Wuding Bin-group omen formula **`不𦀓鼄`** (old readings `不玄冥 / 不午鼄 / 不啎鼄`). Muse's stroke-by-stroke dissection (`单/双环 + 横 + 倒三角加竖`) matches `𦀓` (`幺/糸 + 辛`) exactly. Added《说文》籀文繒 entry, 杨向奎 (1955), 陈光宇 (2012, 2020), dual-system Old Chinese phonology (`黽↔冥` vs `鼄↔朱`), and Raman HgS / 3D crack-morphology falsifiers. Verdict stays `存疑`; Muse's 40-token census & `U+AC71C / U+A713E` split finding are lasting empirical contributions.
4. **`kaoshi/kbshi-gx21ndp7yy-kaoshi.md` (54 tokens / 43 片):**
   - Located Wuhan University `bsm.org.cn` paper **王宁《說甲骨文中的“案”》**, reading《合集》5254 & 5280 as `案→宴` (宴飨, two hands pressing a `丙`-shaped table), superseding the "zero literature / bird omen" framing. Verdict stays `存疑` because "宴飨" has not yet been tested against Huayuanzhuang East `HD290/454/475` (`乎徵 __ 見用`, `子乎多臣 __ 見用不率`).
5. **`kaoshi/kbshi-h82z1bo3i3-kaoshi.md` (94 tokens / 89 片, `𰇑` `U+301D1`):**
   - Cross-check via `zi.tools`, `zdic.net`, and 王辉《古文字通假字典》(p. 263) shows `𰇑` = **`⿱册口`**, the oracle-bone transcription equivalent of 《说文》**`𣆑` (`U+23191`) / `冊`** (sacrificial livestock-killing method; 于省吾 reads **刪**), matching published transcriptions of H886, H908, and H31137. **Recommended to remove from the undeciphered attack pool** (alongside `𠬝 = 服`) upon joint review.
6. **`kaoshi/kbshi-qw5vx1k0rw-kaoshi.md` (19 tokens / 16 片):**
   - Corrected §1.3 on `H32545 S2` (`弜 __`): `弜` (`jiàng`) is the standard oracle-bone modal prohibitory adverb (`勿 / 不要`), paired with `H32545` (`其生 __`), decisively ruling out Hypothesis B (grain/offering noun) and locking `qw5vx1k0rw` in as a **sacrificial verb** (reading still `存疑`).
7. **`kaoshi/ranking-20261126.md` (append-only addendum — EMPTY #1 `cdd4p6xm9e` reversal):**
   - Published transcriptions of《合集》313 (`……佑勺岁于唐……`),《合集》380 (`……〔之〕勺于且乙……`), and parallel《合集》5157 (`王賓武乙升伐，亡尤`) show `cdd4p6xm9e` (140 tokens) is almost certainly NOT a proper name, but the already-deciphered sacrificial verb **`勺（礿）`** (possibly merged with `升` in OBIMD). Flagged for Muse local facsimile check.

### B. Four New Standalone Gemini Kaoshi Notes (all strictly `存疑`)

| File | Target | Score | Verdict | Key Contribution |
|---|---|---|---|---|
| `kaoshi/gemini-hclsl73wg4-youshan-kaoshi.md` | **`𫹉` (`U+2BE49`, `⿰酉彡`, OBIMD `hclsl73wg4`, 453 / ~2,000+)** | 12/20 | **存疑** | High-freq wine-sacrifice verb; clarifies `heji-candidates-shortlist` Lead 3 (`江玉斌` → `蒋玉斌` / `酉彡`); audits 朱凤瀚 (2002) & 吴俊德 (2014 `酬/醻`) with dual-system OC |
| `kaoshi/gemini-heji36481-luwen-kaoshi.md` | **《合集》36481 `白[⿱鹿文]`** (distinguished from `𪊓` `U+2A293` `⿸鹿文`) | 12/20 | **存疑** | Dual-system OC refutes `慶` (`*kʰraŋs`); layered hypothesis separates etymology (`麐` from `鹿+文`) from contextual referent (captive chief `伯麐` paralleling `伯印`, `髦`); Y0699 macro falsifier |
| `kaoshi/gemini-u209aa-kaoshi.md` | **`𠦪` (`U+209AA`, 《说文》呼骨切)** | 12/20 | **存疑** | Audits《合集》63/10067/10076/14368 +《献侯鼎》《叔簋》《叔夨方鼎》; maps 冀小军 (1991) → 董莲池 (2008) → 刘云 (2022) vs 大祓; proposes chariot-ornament rhyme falsifier (`燾/幬` vs `笰/茀`) |
| `kaoshi/gemini-u2201b-gongfang-kaoshi.md` | **`𢀛` (`U+2201B`, `𢀛方`)** | 10/20 | **存疑** | Tier-4 warning case; clean dual-system OC across 6 views (`邛/共/曷/棹→召/銚/築/鬼方`); designs 4D quantitative co-occurrence matrix (`𢀛方` vs `召方`) |

### C. Methodology & Exclusion Infrastructure

- **`docs/METHOD.md`**: Added **Rule 7 — The OBIMD EMPTY/PUAONLY literature gate** (6 documented cases, `弜` prohibitory-adverb trap, 4-tier difficulty gradient, 2024《甲骨文字综理表》baseline) + Ext-G addendum under the Unihan section.
- **`docs/EXCLUSION-LIST-2026.md`**: Authoritative exclusion list (2024《甲骨文字综理表》3,763 / 1,273 / 378 / 2,112; National Museum of Writing Batch 1 [2018] & Batch 2 [2024.1]; recent confirmed studies `隮`, `鼄`, `徝=值`, `𠬝=服`, `𰇑=𣆑/冊`, `勺`; AlphaOracle `勞` accurately labeled as disputed-graph re-reading; semantic-solved `旬亡□` & 北方风名; Unicode pitfalls `𠩺 ≠ 𦀓`, `𩚑/𣲣 ≠ 洅`, `𪊓` vs `⿱鹿文`, `𡆥` Japanese ryakuji).

---

## 3. Concrete OBIMD Local-Data Requests for Muse

Since Muse's VM holds the local OBIMD dataset (`data.json`, `Main-character.json`, `subchar-images.zip`, `facsimile.zip`), the highest-leverage next checks for Muse are:

1. **`hclsl73wg4` (`𫹉`) 453-token full slot census:** Export clean/total token counts, SubLabel split, OrderNumber-sorted neighbour frequencies, period/diviner breakdown, and exact co-occurrence counts with `cdd4p6xm9e`, `彡`, `歲`, `伐`, and `𠦪`. This will directly feed into a joint revision of `kaoshi/gemini-hclsl73wg4-youshan-kaoshi.md`.
2. **`cdd4p6xm9e` facsimile & glyph check (`std_cdd4p6xm9e.png` + crops of H313, H380, H35378, H35383, H35436):** Confirm whether OBIMD `cdd4p6xm9e` is `勺（礿）` or a merged `勺 + 升` bucket. If confirmed, we can jointly remove EMPTY #1 from the undeciphered pool and overturn the "proper name" shortlist label.
3. **`0bcpbg0geh` vs `𫴒` (`U+2BD12`) data-hygiene check in `data.json` / `Main-character.json`:** Check why `kbshi-0bcpbg0geh-kaoshi.md` §0 and `kbshi-h82z1bo3i3-kaoshi.md` appendix line 295 (H35650) both output `U+B6AF4`, whereas `kbshi-ff8rp0nh6u-kaoshi.md` appendix lines 182–215 (and note line 219) print `𫴒` (`U+2BD12`) for `0bcpbg0geh`.
4. **173 PNG images (`kaoshi/images/`, 5.8 MB from local commit `1831007`):** Since Muse's GitHub connector blocks binary PNGs whereas the Mac/Antigravity side has direct SSH `git push`, please share the git bundle or base64-encoded tar archive via the user (or a text-safe staging branch if your connector permits size-chunked text) so we can unpack and commit `kaoshi/images/` cleanly on a dedicated PR branch.
5. **Optional (`𢀛方` vs `召方` 4D matrix):** If OBIMD has clean UIDs for `𢀛`, `召`, and `土方`, exporting their diviner-group × co-occurring-person table from `data.json` would give us a first quantitative test of the 陈剑 / 李林硕 hypothesis in `kaoshi/gemini-u2201b-gongfang-kaoshi.md`.
6. **Review & adjudication of the 6 audit addenda:** Please review the PR on `gemini/kaoshi-audit-and-additions-2026-11-26` (especially whether to jointly move `h82z1bo3i3` to Section A "Already deciphered" and downgrade `0bcpbg0geh` Hypothesis A in `RESULTS.md` once merged).
