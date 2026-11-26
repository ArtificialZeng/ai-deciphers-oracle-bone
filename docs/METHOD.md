# Method — working rules (2026-11-26)

## Corpus

OBIMD, *Scientific Data* 2026, DOI 10.1038/s41597-026-06967-0
(Hugging Face `KLOBIP/OBIMD`, CC-BY 4.0): 10,077 records, 115,319 tokens,
Heji-linked, with explicit markers for undeciphered / disputed graphs.
It is the only openly downloadable, Heji-linked corpus with such markers.
*Heji* itself is print / library; no single open download. HUST-OBC
(140,053 images) was tried first from the image side and abandoned for
screening: a filename search for the Heji marker returned 0 hits — no
inscription context is recoverable from it.

## Pools and counting

- EMPTY: platform `transcription` empty — 1,159 UIDs, 235 in running text.
- PUA-only: transcription non-empty but no CJK character — 820 UIDs,
  275 in running text.
- Clean token = SeatFont = 0 and Mark = −1. Every frequency in a note was
  recounted locally from `data.json` / `Main-character.json`; ranking
  figures are never copied forward without recounting.
- The earlier "435 PUA-only" figure could not be reproduced under any
  definition and is retired — do not cite it.

## The Unihan check comes first

An OBIMD transcription `[CJK, PUA]` double value does not mean
"undeciphered" — it is only the platform's working-reading marker. Check
Unihan (and dictionaries) for the CJK character first:

- 𰇑 (U+301D1, CJK Ext G): no reading, no definition in Unihan — a shape
  code only. The platform's 𰇑 for h82z1bo3i3 is a misidentification.
- 𠬝 (U+20B1D): kMandarin *fú*, "submit", attested in 《说文》/《广韵》/
  《康熙字典》/《汉语大字典》 — already deciphered (服's original form).

> **2026-11-26 Gemini addendum to Unihan rule:** Unihan's lack of `kMandarin`
> for CJK Ext G `𰇑` (U+301D1) is factually true, **but Ext G absence in Unihan
> does NOT prove a graph is undeciphered**. Cross-checks via `zi.tools`,
> `zdic.net`, and 王辉《古文字通假字典》(p. 263) show `𰇑` = `⿱册口`, the
> oracle-bone transcription equivalent of 《说文》`𣆑` (U+23191) / `冊`
> (sacrificial livestock-killing method; 于省吾 reads 刪), directly matching
> published transcriptions of H886, H908, and H31137. Always run **Rule 7**
> below alongside Unihan.

## Reading a sentence

1. Sort by OrderNumber before counting neighbours.
2. Expand merged tokens first (祖乙 / 祖甲 / 十三月 / 五月 are single
   tokens on the platform).
3. Never trust the platform's first-choice display — verify every neighbour
   by its codepoint. Documented misreadings: 貞→鼎, 勿→匁, 伯→白, 巳→子,
   賓→𰌾, 茲→𢆶, 佑→又, 才→在, and the "卜 __ 鼎" slot is really
   "卜 __ 貞" (the token after a diviner name is 貞, codepoint 貞, whose
   standard glyph is 卜 over 鼎).
4. `is_pua` must cover Plane 10 or be replaced by the codepoint field
   (戎's first transcription item is U+AEED6, Plane 10).
5. Standard glyph images can contain strokes intruding from a neighbouring
   graph — verify any detached side component against facsimile crops.
   Facsimile crop coordinates can point at blank space (reverse side or
   coordinate error) — verify crops are readable before using them.
6. HD (Huayuanzhuang East) facsimiles are absent from `facsimile.zip`
   (0 HD files): for HD-only glyphs the glyph description rests on the
   standard image alone — record that honestly.

## The OCR phantom rule

The local 《合集》释文 OCR repeatedly invents readings at undeciphered
positions. Documented phantoms: 懈, 孵, 宴, 動, 草, 团, 济, 网, 和, 豐,
查, 富. Treat any OCR "reading" of an undeciphered graph as a phantom
unless corroborated. (動 was falsified four ways: CUHK 字库 has 0
oracle-bone examples of 動; 動 has 0 tokens in OBIMD; the shape fails;
the OCR gives two mutually exclusive readings of the same glyph.)

## Verdicts and scoring

- 成立 / 存疑 / 放弃 only. A proper-name classification (place, personal,
  diviner name) is a definite result but is filed as 放弃 as a common-word
  kaoshi — a name's sound is in principle unrecoverable and is not a
  decipherment.
- Four rings, each 0–5: 形 (form), 音 (sound), 义 (meaning), 用 (usage).
  Every note lists falsifiers and what was not checked.
- The prize bar (National Museum of Chinese Writing, ¥100,000 per
  undeciphered character): a formal 《甲骨文释读成果科学论证报告》 with
  two senior-expert recommendations, 形/音/义/用 as a mutually verifying
  chain. A single resemblance is only a hypothesis.

---

## The OBIMD EMPTY/PUAONLY literature gate (Rule 7 — added by Gemini, 2026-11-26)

**Never treat an OBIMD EMPTY or PUA-only UID as "genuinely undeciphered" or
"zero prior literature" without passing an external paleographic literature
gate.** Cross-auditing Muse's rounds 1–22 surfaced **six concrete failure
modes** where OBIMD's empty/PUA/Ext-G markup masked already-deciphered graphs,
known ritual formulas, or published scholarship:

1. **False-EMPTY already-deciphered verb (`cdd4p6xm9e`, 140 tokens, EMPTY #1):**
   Published transcriptions of《合集》313 (`贞：翌乙亥佑勺岁于唐……`) and《合集》380
   (`……〔之〕勺于且乙……`), plus parallel《合集》5157 (`王賓武乙升伐，亡尤`), show
   this graph is almost certainly the already-known sacrificial verb **`勺（礿）`**
   (possibly merged with `升` in OBIMD), NOT an undeciphered proper name.
2. **CJK Ext-G false-negative via Unihan-only lookup (`h82z1bo3i3`, `𰇑` U+301D1, 94 tokens):**
   Missing `kMandarin` in Unihan for Ext B–H characters does NOT mean "shape code
   only." IDS decomposition (`⿱册口`) + `zi.tools` / `zdic.net` / 王辉《古文字通假字典》
   (p. 263) + published H886/H908/H31137 transcriptions identify it as 《说文》
   **`𣆑` (U+23191) / `冊`** (sacrificial method; 于省吾 reads 刪).
3. **Unmerged Period V single-word variant misread as a ligature (`0bcpbg0geh`, 112 tokens):**
   Published transcriptions of《合集》35399, 35401, and 35530 unanimously read the
   graph after `旬亡` as a **single word** (`禍/憂`), never two words `"禍尤"`.
   Always check published Period V Huang-group variants before proposing a new
   ligature.
4. **Known Zhouji ritual slot misread as unknown conjunction (`ff8rp0nh6u`, 40 tokens):**
   The top-5 verbs in `王賓[先祖] X 亡尤` (`彡、翌、祭、ff8、協`) and the `祭 → X → 協`
   cross-generation cycle prove `ff8rp0nh6u` is the 4th of the five Zhouji rituals
   **`洅` (`洅`/`𣫭`/`載`)** (and `匸丙` = pre-dynastic ancestor **`報丙`**). Its
   *etymology* remains disputed (`存疑`), but its *ritual slot* is settled.
5. **Century-old named omen formula missed as "zero literature" (`crck62eltz`, 40 tokens):**
   `不 __ 鼄` is the famous Wuding Bin-group formula **`不𦀓鼄`** (`𦀓` U+26013,
   `⿰糹辛`, old readings `不玄冥 / 不午鼄 / 不啎鼄`; 杨向奎 1955; 陈光宇 2012,
   2020). Always cross-check standard oracle formulas and 《说文》籀文 before
   proposing ad-hoc verb guesses.
6. **Recent specialist paper missed by generic web search (`gx21ndp7yy`, 54 tokens):**
   Wuhan University Bamboo & Silk Center (`bsm.org.cn`) publishes **王宁《說甲骨文中的“案”》**,
   directly reading H5254/H5280 as `案→宴` (宴飨), replacing the "zero literature /
   bird omen" framing (while leaving HD290/454/475 as an open test).

### Mandatory pre-attack checklist (Rule 7 operational steps)

Before opening a new kaoshi note on any OBIMD UID:
1. Check `docs/EXCLUSION-LIST-2026.md` first (awarded graphs, confirmed recent
   decipherments, semantic-solved slots, Unicode proxy pitfalls).
2. For any CJK Ext B–H character, check **IDS decomposition + `zi.tools` +
   `zdic.net` + 《古文字通假字典》** — never stop at Unihan `kMandarin`.
3. Search published transcriptions of at least 3–5 representative Heji numbers
   on specialist sites (`bsm.org.cn`, `fdgwz.org.cn`, Academia Sinica, CNKI /
   《古文字研究》) using both modern conventional readings and structural IDS
   descriptions.
4. **Check standard oracle-bone function words — the `弜` prohibitory-adverb
   trap:** Never gloss high-frequency oracle-bone grammar particles by their
   《说文》 lexical gloss alone. Documented case (`qw5vx1k0rw`, H32545 S2 `弜 __`):
   **`弜` (`jiàng`)** is the standard modal prohibitory adverb (**`勿 / 不要`**),
   paired with `其` in positive/negative divination (`其 V / 弜 V`), NEVER the
   《说文》 adjective "strong (彊)" or a personal name here; recognizing `弜`
   immediately locks the following slot as a **verb** and excludes noun hypotheses.
5. For any phonological claim, provide **dual-system Old Chinese reconstructions**
   (Zhengzhang 2003 + Baxter–Sagart 2014 v1.1) and never mix Middle Chinese
   transcriptions into an Old Chinese table.

### Authoritative baseline and 4-tier difficulty gradient

- **Baseline corpus counts — 《甲骨文字综理表》 (2024, 中西书局):**
  **3,763** total head entries = **1,273** confirmed deciphered + **378**
  disputed + **2,112** undeciphered (details in `docs/EXCLUSION-LIST-2026.md`).
- **4-tier difficulty gradient (start at Tiers 1–2, treat Tier 4 as a warning):**
  - **Tier 1 (Data-hygiene / unmerged variants / false-undeciphered):** OBIMD
    EMPTY/PUAONLY graphs that turn out to be already deciphered (`𠬝`, `𰇑`, `勺`)
    or unmerged Period V variants (`0bcpbg0geh`). Value: cleaning the real attack
    pool.
  - **Tier 2 (High-frequency common words with formulaic slots & cross-period
    parallels):** Genuine high-value targets where ritual/syntactic role is clear
    and bronze/Warring States parallels exist (e.g., `𫹉` `hclsl73wg4`, `𠦪`
    `U+209AA`, `洅` etymology, `不𦀓鼄` physical test).
  - **Tier 3 (Low-frequency / single-fragment disputed graphs with tight
    phonological & structural constraints):** E.g., 《合集》36481 `白[⿱鹿文]`,
    where falsification hinges on targeted micro-inspection of original bone
    rubbings/photos.
  - **Tier 4 (Proper names — person, place, and polity names):** E.g., `𢀛方`
    (`U+2201B`), `n52ssmqnda`, `xdimpzk5q6`, `jyskjcj861`. Sound is in principle
    unrecoverable from shape alone; do NOT invent a 7th pictographic guess — only
    quantitative co-occurrence matrices (period × personnel × geography × variants)
    add verifiable value.
