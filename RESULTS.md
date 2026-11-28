# Results — per-character status (2026-11-28, Muse rounds 1–37 + Gemini Batch 1–3)

Source of truth for each row is the kaoshi note in `kaoshi/`. Scores are
形 / 音 / 义 / 用 (each 0–5, total /20). "—" means the note does not state a
total; read the note. **成立: 0.**

**Accounting & ownership note (per `COORDINATION.md` §4):**
- **Total full kaoshi notes: 45**, covering **48 targets** — **36** Muse `kaoshi/kbshi-*-kaoshi.md` notes covering **37** targets (rounds 1–37, commits `090ea77`, `14af5ba`, `bab1ae7`; `kbshi-e33qe36es7-adjudication-20261126.md` is a dated adjudication addendum to `e33qe36es7`, not a 37th target note) + **9** Gemini `kaoshi/gemini-*-kaoshi.md` notes covering **11** targets (all with top-of-note inline PNG visual sheets and bundled in `exports/ai-deciphers-oracle-bone-gemini-kaoshi-2026-11-28.docx`).
- **Combined verdicts (applying Muse's signed adjudications in `reports/claude-reply-to-gemini-2026-11-26.md` & `kbshi-e33qe36es7-adjudication-20261126.md`, while preserving Muse's original verdicts untouched pending joint adjudication of Gemini's new 2026-11-28 addenda):**
  - **成立 (Established): 0**
  - **放弃（已释，移出攻击名单，Section A）: 4** — `𠬝` (`cvzszyp6bm`), `秝` (`lyq3tnc036`, Muse R30), plus `h82z1bo3i3` (`𰇑`=`𣆑`/`冊`) & `a5tuvlp0po` (`鞀`) formally relocated per Muse's signed `claude-reply-to-gemini-2026-11-26.md` §2. *(Shortlist-level `cdd4p6xm9e = 勺（礿）` is also formally removed from the undeciphered pool. Gemini's 2026-11-28 addenda additionally recommend relocating `BDC20` [`牝羊`], `BDC1F` [`牡羊`] [60 tokens], and `bu3h266vxh` [师组贞人 `勺`] into Section A — pending Muse/owner adjudication.)*
  - **放弃（专名／未并入异体定性，非破译，Section B）: 11** (Muse rounds 1–37; Gemini's 2026-11-28 addendum additionally recommends relocating `1yynvi0pfn` from Section C into Section B as an unmerged duplicate of `tyazlz2ugv` [`𫩀/柰/叔`])
  - **存疑 (Undecided, Sections C & D): 33** — **22** Muse targets (incl. `0bcpbg0geh` Hypothesis A 17/20 withdrawn & `e33qe36es7` 12/20 `舞` leading) + **11** Gemini targets
  - **Reconciliation check:** `0 + 4 + 11 + 33 (22 Muse + 11 Gemini) = 48` targets across `36 + 9 = 45` full notes.

---

## A. Already deciphered, removed from the attack list (4)

| Target | Tokens | Verdict & adjudication record | Note |
|---|---|---|---|
| **𠬝** (`cvzszyp6bm`) | 41 / 36 片 | 放弃（已释）— 服的初文，读 *fú*，16/20 | `kbshi-cvzszyp6bm-kaoshi.md` |
| **秝** (`lyq3tnc036`) | 7 / 7 片 | 放弃（已释）— 二禾之字，武丁宾组贞人「秝（*lì*）」，16/20（Muse R30，`bab1ae7`） | `kbshi-lyq3tnc036-kaoshi.md` |
| **𰇑** (`h82z1bo3i3`) | 94 / 89 片 | 放弃（已释）— `⿱册口` = 《说文》`𣆑` (`U+23191`)/`冊`（于省吾读刪，王辉《古文字通假字典》p.263）；Gemini 11-26 附记 + **Muse `claude-reply` §2.2 签字移入 A 节** | `kbshi-h82z1bo3i3-kaoshi.md` |
| **鞀（鼗）** (`a5tuvlp0po`) | 8 / 8 片 | 放弃（已释）— 裘锡圭考定打击乐器／乐祭名「鞀（大鞀）」（`H23610`/`H15802`/`H15805`，`crops_a5tuvlp0po.png`）；Gemini 11-26 附记 + **Muse `claude-reply` §2.3 签字移入 A 节** | `kbshi-a5tuvlp0po-kaoshi.md` |

- **Shortlist-level removal (signed via Muse `claude-reply` §2.4):** **`cdd4p6xm9e`** (EMPTY #1, 140 clean / 120 片) is visually confirmed via `kaoshi/images/crops_cdd4p6xm9e.png` and published `H313`/`H380` transcriptions as pure 3-stroke **`勺（礿）`** and formally **removed from the undeciphered pool**.
- *(Pending Muse/owner adjudication from Gemini 2026-11-28 addenda: **`BDC20` (`nms96pmn1w`, 41 clean) = `牝羊`（羊+匕）**, **`BDC1F` (`wq47pyztal`, 19 clean) = `牡羊`（羊+土）** [60 tokens, `kaoshi/images/audit_bdc20_bdc1f_vs_yang.png`], and **`bu3h266vxh` (`U+F9109`, 6 clean) = 师组贞人「`勺`」** [`H20022`「戊午卜，勺，侑小王」，`kaoshi/images/audit_bu3h_shao_and_refqn_yumu.png`] are recommended for relocation into Section A.)*

## B. Muse rounds 1–37 — Closed as proper names / unmerged variant, definite negative conclusions (11)

| Target | Tokens | Classification | Score | Gemini audit addendum | Note |
|---|---|---|---|---|---|
| X/1850 | 61 例 | 由的未并入异体 | — | — | `kbshi-x1850-kaoshi.md` |
| n52ssmqnda | 35 / 34 片 | 贞人名；槽位订正为“卜 __ 貞”非“卜 __ 鼎” | 9/20 | — | `kbshi-n52ssmqnda-kaoshi.md` |
| xdimpzk5q6 | 14 / 6 片，全花东 | 地名；14 例全居在/才、自之后，“入自 __”与“入自西”逐字平行 | 8/20 | — | `kbshi-xdimpzk5q6-kaoshi.md` |
| 7b9lfpes9d | 9 / 9 片 | 人名（武丁期军事人物，与光平行），排除法收敛 | 8/20 | — | `kbshi-7b9lfpes9d-kaoshi.md` |
| jyskjcj861 | 12 / 10 片 | 地名/方国名；“來 自 __”一槽排他性为决定性证据 | 8/20 | — | `kbshi-jyskjcj861-kaoshi.md` |
| xhfae21bpk | 8 / 7 片 | 地名（田猎地/祈祷地；地方神名不能排除） | 9/20 | — | `kbshi-xhfae21bpk-kaoshi.md` |
| dd5w09rr1q | 8 / 7 片 | 人名：某人“子__”之第二字，所指与读音不可恢复 | 9/20 | — | `kbshi-dd5w09rr1q-kaoshi.md` |
| 2bcusrt88g | 7 / 4 片 | 地名/方国名（鹿首加口，7/7 居“在/宅”后句末）；族名不能区分 | 9/20 | — | `kbshi-2bcusrt88g-kaoshi.md` |
| 3jzeliplnn | 7 / 5 片，全花东 | 人名（禾+口+刀，最可能为剌但未证实）；发现 `facsimile.zip` 实存 164 幅 HD 摹本（Muse R28，`bab1ae7`） | 13/20 | **11-28 附记**：订正 `其/弜` 模态副词与并列连词 `眔`（反强化人名定性）；致谢 HD 164 摹本发现 | `kbshi-3jzeliplnn-kaoshi.md` |
| bu3h266vxh | 6 / 6 片 | 贞人名（6/6 居序辞贞人位，原拟候选取「叩」未证实；Muse R34，`bab1ae7`） | 9/20 | **11-28 附记（建议移入 A 节已释）**：已刊《合集》20022「戊午卜，**勺**，侑小王」＋邻码 `U+F9109`≈`U+F90D1(勺)` 实锤为**师组贞人「勺」**，排除「叩」说（`audit_bu3h_shao_and_refqn_yumu.png`） | `kbshi-bu3h266vxh-kaoshi.md` |
| xyp0ngvyd7 | 6 / 6 片 | 地名（处所名，6/6 句末，H8221–H8232 出行片群；Muse R35，`bab1ae7`） | 8/20 | — | `kbshi-xyp0ngvyd7-kaoshi.md` |

Shortlist-level (no full note):
- `2lep30tiiz` (71 例，人名), `tq26tb9tj9` / `5i4ba39u9k` / `yo5h3qdl2s` (地名/先妣名).
- *(Pending Muse/owner adjudication from Gemini 2026-11-28 addendum: `1yynvi0pfn` [6 clean] is visually proven on same-plate `H35462` [`audit_1yynvi0pfn_vs_tyazlz2ugv.png`] to be an unmerged duplicate of `tyazlz2ugv` [`𫩀/柰/叔`, 163 clean] and recommended for relocation from Section C into Section B.)*

## C. Muse rounds 1–37 — Still 存疑 (22; original Muse verdicts preserved, signed adjudications & Gemini audit addenda noted)

| Target | Tokens | Muse leading hypothesis / adjudicated status | Score | Gemini audit addendum | Note |
|---|---|---|---|---|---|
| ⟨礻+升⟩ | 1 例（孤证） | 存疑异写：更可能是升加义符的异写，非新字 | — | — | `kbshi-sheng-kaoshi.md` |
| gx21ndp7yy | 54 / 43 片 | 名词，兆物类；主槽“鼎王叀吉”约 30 例 | — | **11-26 附记**：检出王宁《說甲骨文中的“案”》（`案→宴` 释 H5254/5280）；花东 HD290/454/475「見用」槽未验，仍 `存疑` | `kbshi-gx21ndp7yy-kaoshi.md` |
| fi0wiw1adi | 13 / 10 片，全花东 | 白色可数牲畜（首选假说，物种未定）；形义冲突 | 形2 音0 义3 用3 | — | `kbshi-fi0wiw1adi-kaoshi.md` |
| BDC20 | 41 / 25 片，全花东 | 原判可数祭品（物种未定）；HD243 与 BDC1F 并列各数五 | 形2 音0 义3 用4 | **11-28 附记（建议移入 A 节已释）**：五重互证锁定为**`牝羊`（羊+匕）**——`U+BDC18–BDC43` 纯羊部码段＋`羊` 双子形（`aoai`/`o6eq`）＋朱歧祥花东羊首短横＋`HD243/196/487` 实景摹本＋`xianqin.org`《花东》487「羊匕一」（`audit_bdc20_bdc1f_vs_yang.png`） | `kbshi-bdc20-bdc1f-kaoshi.md` |
| BDC1F | 19 / 17 片（11HD+6H） | 原判可数祭品（弱于 BDC20） | 形2 音0 义2 用2 | **11-28 附记（建议移入 A 节已释）**：同上五重互证锁定为**`牡羊`（羊+土）**，与 `BDC20` 合计 60 tokens 建议移入 Section A | `kbshi-bdc20-bdc1f-kaoshi.md` |
| 0bcpbg0geh | 112 / 55 片 | **Hypothesis A（禍尤合文，17/20）已于 `claude-reply` §2.1 正式撤回／证伪**；Hypothesis B（第五期黄组单字繁化异体）领先，维持 `存疑` | 原 17/20 撤回 | **11-26 附记（已获 Muse 采纳）**：H35399/35401/35530 刊布释文一律作单字「禍/憂」，OBIMD 全库作 `U+B6AF4`、零 `𫴒` | `kbshi-0bcpbg0geh-kaoshi.md` |
| crck62eltz | 31 独＋9 并（共 40 例） | 动词未定：知觉动词+鼄 vs 移动动词+地名鼄 | 8/20 | **11-26 附记**：锁定武丁宾组百年悬案 **`不𦀓鼄`**（`𦀓` `U+26013`，`⿰糹辛`；杨向奎 1955 vs 陈光宇 2012/2020）；仍 `存疑` | `kbshi-crck62eltz-kaoshi.md` |
| qw5vx1k0rw | 19 / 16 片 | 祭祀动词 vs 祭品名词，两说互斥 | 7/20 | **11-26 附记**：订正 `H32545 S2` `弜 __`——禁止副词 `弜` 排除名词说、锁定祭祀动词；仍 `存疑` | `kbshi-qw5vx1k0rw-kaoshi.md` |
| gtysuhhw3p | 17 / 13 片 | 移动动词领先 | 7/20 | — | `kbshi-gtysuhhw3p-kaoshi.md` |
| ff8rp0nh6u | 40 / 33 片 | 祭祀动词或“協”类连词；与協共享两排他性语槽 | 9/20 | **11-26 附记**：**100% 锁定晚商周祭第四祀 `洅`（`洅`/`𣫭`/`載`）**，解开 `匸丙 = 報丙`；本源构形争议仍 `存疑` | `kbshi-ff8rp0nh6u-kaoshi.md` |
| 4a6130bz6w | 14 / 10 片，全花东 | 动词领先（巳/子₂之后只接动词） | 7/20 | — | `kbshi-4a6130bz6w-kaoshi.md` |
| 4zv87269nu | 12 / 12 片 | 徠 lái 有三重反证；穀物名词说保留 | 7/20 | — | `kbshi-4zv87269nu-kaoshi.md` |
| wpbo51inbu | 9 / 6 片 | 动词已定，无具体读法；OCR“動”已证伪为幻影 | 7/20 | — | `kbshi-wpbo51inbu-kaoshi.md` |
| rp1zjtuksu | 11 / 7 片（9 clean） | 动词/人名并列领先；子形与槽位完全相关 | 7/20 | — | `kbshi-rp1zjtuksu-kaoshi.md` |
| diesgffg1o | 9 / 9 片 | 和说三重反证；人名说相容但未证实 | 7/20 | — | `kbshi-diesgffg1o-kaoshi.md` |
| npykxas4c8 | 8 / 6 片 | 人名/动词/地名三说无一能覆盖全部 8 例 | 7/20 | — | `kbshi-npykxas4c8-kaoshi.md` |
| bh6mqc68g2 | 8 / 8 片 | 人名领先；“御子 X 于”槽严格重数 11 例 | 7/20 | — | `kbshi-bh6mqc68g2-kaoshi.md` |
| **e33qe36es7** | 7 / 6 片 | **舞（从雨从無祈雨繁构）领先**，霖/霰为已刊竞争读法（Muse 11-26 裁决附记；原 15/20 霖说撤回；保留禁攻） | **12/20**（裁决分） | 最初由 Gemini PR #1 Rule 7 拦截；按 Muse 裁决维持 `存疑` 并软化 `EXCLUSION-LIST` 定性 | `kbshi-e33qe36es7-kaoshi.md` + `kbshi-e33qe36es7-adjudication-20261126.md` |
| **5jcghtltbx** | 7 / 7 片 | 人名（人/先祖名）领先，动词紧追（Muse R31，`bab1ae7`） | 7/20 | — | `kbshi-5jcghtltbx-kaoshi.md` |
| **gjgujysmue** | 6 / 1 片（HD191） | 动词已决，话题为每日用浅黑色马「騩」（Muse R33，`bab1ae7`） | 7/20 | **11-28 附记**：订正 §1.2 L44 `弜` 实为禁止副词（非贞人名），补录 `gmw.cn`《花东》191 线索；仍 `存疑` | `kbshi-gjgujysmue-kaoshi.md` |
| **refqnby49o** | 6 / 6 片 | 军事人员／征发域兼类假说（Muse R36，`bab1ae7`） | 7/20 | **11-28 附记**：构形锁定 **`⿱雨目`（`𩆨`）**，补录王恩田（2015《释霉》，`fdgwz.org.cn` 引 H5777/H7345）及丁山/郭沫若/饶宗颐诸说（`audit_bu3h_shao_and_refqn_yumu.png`）；仍 `存疑` | `kbshi-refqnby49o-kaoshi.md` |
| **1yynvi0pfn** | 6 / 6 片（黄组） | 祭名（原判米+示+爻形，与 𫩀 分立；Muse R37，`bab1ae7`） | 9/20 | **11-28 附记（建议移入 B 节未归并异体）**：`H35462` 同片原摹本正面对决直证与 `tyazlz2ugv`（`𫩀/柰/叔`, 163 例）完全同字（标准图描改失真所致），并补正 `ff8=洅`、`匸乙/匸丁=報乙/報丁`（`audit_1yynvi0pfn_vs_tyazlz2ugv.png`） | `kbshi-1yynvi0pfn-kaoshi.md` |

## D. Gemini standalone kaoshi notes (2026-11-26 / upgraded 2026-11-28) — Still 存疑 (9 notes / 11 targets, ALL with top-of-note PNG embeds)

| Target | Corpus / Frequency | Core finding & status (verdict strictly `存疑`) | Score (形/音/义/用) | Top-of-note visual & note |
|---|---|---|---|---|
| **`𫹉`** (`U+2BE49`, `⿰酉彡`, OBIMD `hclsl73wg4`) | OBIMD **452 clean / 381 片**（全语料 ~2,000+ 例） | 商代高频酒祭动词；本地全槽实测（否定副词共现 39 次实证纯动词；同句共现 `彡` 11 次证伪「`𫹉=彡`」说）；双系古音评述吴俊德（2014「酬/醻」）与朱凤瀚（2002） | **12/20** (3/2/3/4) | `crops_hclsl73wg4_youshan.png` · `gemini-hclsl73wg4-youshan-kaoshi.md` |
| **《合集》36481 `白[⿱鹿文]`**（权代 `𪊓` `U+2A293`） | 《合集》36481（国博 Y0699）＋《伯其父簠》等 | 双系上古音证伪阳部「慶」说；提出分层假说——字源释 `麐`（从鹿文声），辞例读被俘危方方伯 `伯麐`；待国博 Y0699 微距验「文」vs「心」 | **12/20** (3/4/3/2) | `components_heji36481_lu_wen_xin.png` · `gemini-heji36481-luwen-kaoshi.md` |
| **`𠦪`** (`U+209AA`, OBIMD `1wismy95hz`) | **OBIMD 224 clean / 172 片**＋《献侯鼎》《叔簋》《叔夨方鼎》 | 2026-11-28 补完 OBIMD 实测（`禾 66 + 雨 16 + 年 11 = 41.5%` 印证「祈求」义，前接 `𫹉` 16 次）；梳理冀小军（1991）→ 董莲池（2008）→ 刘云（2022）；车饰韵部（`燾/幬` vs `笰/茀`）证伪检验 | **12/20** (3/2/3/4) | `crops_u209aa_1wismy95hz.png` · `gemini-u209aa-kaoshi.md` |
| **`𢀛`** (`U+2201B`, `𢀛方`, OBIMD `b2n32mdq0u`) | OBIMD **54 clean / 44 片**（对比 `召` `vpcd7inkf9` **22 clean / 18 片**） | 第四阶方国专名警示案例；澄清六派假说双系上古音；OBIMD 首测证实 `𢀛` 显性宾组贞人（`爭4/殻3/賓1/古1`）vs `召` 零宾组贞人，首次量化印证分期互补线索 | **10/20** (2/1/3/4) | `crops_u2201b_gongfang_vs_zhao.png` · `gemini-u2201b-gongfang-kaoshi.md` |
| **`3xbmgmm4j0`** (`U+C9B7A` / `U+C9B76`) | OBIMD **5 clean / 3 片**（`H31994/31995/33232`，历二） | 真未释动词：全库 `其 X 眾` 仅 3 动词（`喪 5 / 雉 4 / 本字 2`），与 `弜` 配对锁死可控及物动词；原摹本证实双鸟／双羽置木／大之上 | **11/20** (3/1/3/4) | `crops_3xbmgmm4j0.png` · `gemini-3xbmgmm4j0-kaoshi.md` |
| **`aelrb19u0i`** (`U+BA204`) | OBIMD **5 clean / 5 片**（`H12641–H12665`） | 真未释气象修饰字：5/5（100%）紧接「雨」前，`[不/其/亦] X 雨` 全库第 4；座盘＋双曲臂＋方／菱块＋上曲钩，排除 `延/冓/登/足/豐` | **10/20** (3/0/3/4) | `crops_aelrb19u0i.png` · `gemini-aelrb19u0i-kaoshi.md` |
| **`o7eb365hnf`** (`U+B21AA`, `東/束+戉`) | OBIMD **7 clean / 5 片**（`H575=丙75`, `H1448/3158/7937/8132`，宾组） | 真未释祭祀动词：正反对贞 `勿 __ 于黄奭/大甲`，可带 `三牛/一牢`；2026-11-28 补核蔡哲茂《伊尹傳說的研究》引 `H575=丙75` 作「辣」，审慎改叙为跨期结构对照字组 | **11/20** (3/1/3/4) | `crops_o7eb365hnf.png` · `gemini-o7eb365hnf-wvxqqsz1w8-kaoshi.md` |
| **`wvxqqsz1w8`** (`U+FDBA2`, `b92[束?]+攴`) | OBIMD **6 clean / 4 片**（`H30329/30362/30454/30455`，无名组） | **2026-11-28 深度升级（10→11/20）**：发现 `H30393`（粹1540）罗塞塔跨片联结——全部 3 个直宾（`小山`/`aawi`/`otbt`）齐聚祈雨山神（同 `H30329` 3 枚 `岳` 圆底山基）；自我订正左基件＝无名组 **`b92fu80uys`**（`H29700 其束司魚`/`H30381 珠402=束`）非无名组瘦菱「東」、左竖 `丨` 占 3/6 非「阜」、`H30455 S1` 横线为裂纹→**升格「束+攴／敕」领先、降级「敶/陳」** | **11/20** (3/1/3/4) | `wvx_b92_dong_shu_compare.png` + `wvx_h30329_h30393_mountains.png` + `wvx_full_plates.png` · `gemini-o7eb365hnf-wvxqqsz1w8-kaoshi.md` |
| **`o68jkkro3f`** (`U+A98E4`) | OBIMD **5 clean / 5 片**（`H471/3254/15821–15823`） | 真未释宗庙酒礼动词：门/宀内含尖底 `酉`＋4–6 枚液滴，恒受 `其` 修饰并关联 `殺三牢 / 𭑈 / 箙一牛` | **10/20** (3/0/3/4) | `crops_o68jkkro3f.png` · `gemini-o68jkkro3f-kaoshi.md` |
| **`b037aq4o64`** (`U+C425F`) | OBIMD **2 clean / 1 片**（`H30373 = 《戩》26.3`，何组/无名组） | **新增（笔记 #9）**：单版强语法约束真未释动词——同版兼受双禁止副词 `勿 __ 工 □`、`弜 __ 箙 □` 100% 锁死可控及物动词；受限于单版 2 例与空音环 | **9/20** (3/0/3/3) | `crops_b037aq4o64_g7m9i371p4.png` · `gemini-b037aq4o64-g7m9i371p4-kaoshi.md` |
| **`g7m9i371p4`** (`U+A1F49`) | OBIMD **2 clean / 1 片**（`H13389`） | **新增（笔记 #9）**：单版强语法约束气象谓词——`貞茲云其 __ □` / `貞茲云 □ __`（S2 遭骨缘斜切）；严格区分 OBIMD 本地 `茲+云` 6 句/5 片与外部 `ntu.edu.tw` `H13392 貞茲云延雨` | **8/20** (2/0/3/3) | `crops_b037aq4o64_g7m9i371p4.png` · `gemini-b037aq4o64-g7m9i371p4-kaoshi.md` |

## E. Rule-7 OBIMD pre-screening interceptions & high-risk catches (DO NOT ATTACK as undeciphered)

### E.1 Batch 2 interceptions (2026-11-26, `kaoshi/images/survivors_vs_known.png`)

| OBIMD UID | Tokens | Actual known character / status | Key evidence |
|---|---|---|---|
| **`e33qe36es7`** | 7 clean | **领先读法「`舞`」（从雨从無繁构；未刊确证，Muse 11-26 裁决留存疑 12/20，保留禁攻）** | `H30029 乎__亡大雨`、`H30041 于翊日丙__又大雨`；详见 `kbshi-e33qe36es7-adjudication-20261126.md` |
| **`pmjqw82db0`** | 6 clean | **`衛`**（`韋 + 行`） | `H7888 師往衛` |
| **`01v0id7th0`** | 5 clean (HD) | **`黍`** | `HD218 / HD379 子其匄黍于帚` |
| **`dzob6ag7n1`** | 5 clean | **`最 / 子`** | `H30885 叀最至`、`HD291 子/最祝` |
| **`gbjr7sabn4`** | 5 clean | **`豕`**（竖立猪形异体） | `H32049 / H32050 卯三十豕` |

### E.2 Batch 3 high-risk interceptions (2026-11-28)

| OBIMD UID | Tokens | Actual known character / high-risk match | Key evidence |
|---|---|---|---|
| **`0fig5rmiox`** (`U+F3206`) | 5 clean / 4 片 | **高危疑似「`求`」（`aki498y6jc`）未归并异体——「`求示`」（伊尹舅示）** | 蔡哲茂（1987《殷卜辭「伊尹龜示」考》）已将 `H14348`、`H14349`、`H14358` 释为「求示」；原摹本与 `求` 极近（`kaoshi/images/audit_0fig5rmiox_vs_qiu.png`），**严禁单列未释笔记** |
| **`9c9zf6hv2z`** (`U+BEFC5`) | 4 clean / 4 片 | **`掫 / 驟`（大驟風）** | `H13359/13361/13364/13365 大__風` 气象既释字，见 `EXCLUSION-LIST-2026.md` |
| **`97dgghy3oj`** (`U+B057B`) | 5 clean / 2 片 (HD) | **`斝`（地名）** | `HD363 / HD480 在__ / 來狩自__` 花东既释地名 |
| **`ig9oetqcmy`** (`U+D00C9`) | 5 clean / 2 片 (HD) | **`麓`（地名）** | `HD375 / HD494 在__` 花东既释地名 |
| **`oqwz3j1hh1`** (`U+FE247`) | 3 clean / 3 片 | **`祀`** | `H4261 / H15502 / H30909` 未归并已释字 |
| **`kk9zxal8u7`** (`U+A986A`) | 3 clean / 2 片 | **`宋`** | `H30386 / H35673`（大宋／小乙宋／在宋）既释字 |
| **`xeyf2mkerf`** (`U+ABF69`) | 3 clean / 3 片 | **`柚`** | `H33082–33084 王翦__ / 敦__` 既释地名／方国名 |

## F. Counts (for orientation, not a result)

- **Authoritative 2024 baseline — 《甲骨文字综理表》 (2024, 中西书局):**
  **3,763** deduplicated head entries = **1,273** confirmed deciphered +
  **378** disputed + **2,112** undeciphered. See `docs/EXCLUSION-LIST-2026.md`.
- Earlier survey ranges: ~4,500–4,600 distinct single characters; ~1,500 loosely
  deciphered; ~1,170 strictly confirmed in Liu Zhao 2014; "接近 6000" =
  《甲骨文字形表》 6,211 glyph entries (4,024 single characters + 2,187 variants).
- OBIMD pools: 1,159 EMPTY + 820 PUA-only UIDs; `facsimile.zip` verified to
  contain **164 HD facsimiles (`hd2.jpg`–`hd549.jpg`)** alongside the H plates.
  All `clean ≥ 6` viable non-proper-name candidates in OBIMD are now exhausted
  or intercepted under Rule 7.

## Outstanding checks (library / museum / physical work)

1. **Muse 173 PNG images bundle (`kaoshi/images/`, local commit `1831007`):**
   **21** Gemini PNG sheets are now committed in `kaoshi/images/` (9 from PR #1 +
   12 from PR #3); Muse's 173 PNGs remain pending transfer from Muse's VM.
2. **Joint Muse/owner adjudication of Gemini 2026-11-28 addenda:**
   Confirm relocation of `BDC20` (`牝羊`) & `BDC1F` (`牡羊`) (60 tokens) and
   `bu3h266vxh` (`勺`) into Section A, and `1yynvi0pfn` (`tyazlz2ugv` duplicate)
   into Section B.
3. **Printed 《合集释文》, 《殷虚文字丙编》 (75), 《殷墟花园庄东地甲骨》 (2003), 《新甲骨文编》 & 《甲骨文字综理表》 (2024):**
   Especially: `b92fu80uys` (`H29700`/`H30381=珠402`/`H30484`) & `wvxqqsz1w8` (`H30329`/`H30362`/`H30454=京津3866`/`H30455`) under「束/敕/東」; `H575=丙75` (`o7eb365hnf`「辣」); `H30373=戩26.3` (`b037aq4o64`); `H13389` (`g7m9i371p4`); `H12641–H12665` (`aelrb19u0i`); `H31994/31995/33232` (`3xbmgmm4j0`); `H471/3254/15821–15823` (`o68jkkro3f`); Vol. 12 `H35398–H35911` (`0bcpbg0geh`); `HD290/454/475` (`gx21ndp7yy`).
4. **Physical & specialist-plate falsifiers:**
   - National Museum Y0699 high-res macro check (`白[⿱鹿文]` lower radical `文` vs `心`).
   - Western Zhou chariot-ornament inscription check for `𠦪` (`燾/幬` vs `笰/茀`).
   - 1980 《小屯南地甲骨》 H24 plate check for `[甲寅，酉彡五牢]`.
   - Raman HgS cinnabar spectroscopy & 3D crack-morphology statistics on `不𦀓鼄` bones (《合集》10229 / 甲3339, 《丙》28/30).
   - Full-《合集》 4D co-occurrence matrix & permutation test for `𢀛方` vs `召方`.
