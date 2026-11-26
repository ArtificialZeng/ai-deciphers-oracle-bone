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
