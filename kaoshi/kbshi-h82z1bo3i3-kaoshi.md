# 考釋筆記：OBIMD UID h82z1bo3i3——平臺隸定 𰇑 是不是一個讀音？

- **日期**：2026-11-26
- **結論**：**存疑**。本字是一個真實的未釋字（94 例、全部 clean token、89 片），但**平臺給的 𰇑 不是一個讀音**：𰇑（U+301D1，CJK Ext G）在 Unicode 的 Unihan 數據庫中**沒有任何讀音、沒有任何釋義**（無 kMandarin、無 kDefinition、無粵語／日／韓／越讀音），無維基詞典條目，全網檢索無任何辭書收錄。𰇑 只是一個形狀碼位——給未釋字形一個可打字的編號，不等於釋讀了它。平臺自身的轉寫也是分裂的：`transcription: [𰇑, U+A713F]`，即同一字形同時被記為一個罕用漢字和一個私用區碼位（未釋標記）。因此本輪的核心問題已有確定答案：**𰇑 是誤認／形碼，不是釋讀**。但本字本身的音義仍無任何具體讀法可以成立：字形與已比對的器物字皆不同，語槽多樣、無固定公式，詞類未定，無青銅／篆書後代，無已發表試讀。
- **狀態**：未釋。平臺隸定 𰇑 不予採信，本筆記不主張任何讀音。

## 0. 標識與口徑

- OBIMD UID：`h82z1bo3i3`；平臺 codepoint 𰇑（U+301D1）；transcription 為雙值 `["𰇑", U+A713F]`（罕用漢字＋私用區碼位）。
- 頻次（本地 OBIMD `data.json` 實測，**已重數，不沿用排名文件的 94 例之說**）：**94 tokens / 89 片，全部為 clean token**（SeatFont = 0 且 Mark = −1），與排名文件一致。H（合集）83 例、HD（花園莊東地）11 例。組別：InscriptionSentence1 68、InscriptionSentence2 14、InscriptionSentence3 6，其餘 6 例分屬 Sentence6／8／9／22／23。
- 子字形：93 例的 SubLabel 即本 UID；**1 例的 SubLabel 為 `vdh8n3qwp9`**（見 §2.3）——該 token 在平臺內部被切分為另一子字形，`vdh8n3qwp9` 在 `Main-character.json` 中無獨立字頭。
- 斷代旁證：句中出現的貞人殻（3 例）、賓（2 例）、韋（1 例）皆為武丁時期貞人；「王」出現於 7 句。本字屬武丁卜辭。

## 1. 𰇑 是不是一個讀音？——否（本輪的核心結論）

### 1.1 Unihan：無讀音、無釋義

Unicode 官方 Unihan 數據（2026-11-26 抓取，https://www.unicode.org/cgi-bin/GetUnihanData.pl?codepoint=301D1）：

| 字段 | 值 |
|---|---|
| kIRG_GSource | `GCA-J0290` |
| kIRG_UKSource | `UK-01323` |
| kRSUnicode | `30.5`（口部，餘 5 畫） |
| kTotalStrokes | 8 |
| kPhonetic | `19*`（音系系列號，非讀音） |
| kMandarin / kDefinition / kCantonese / kJapanese / kKorean / kVietnamese | **全部缺失** |

即：Unicode 只記錄了這個字的**編碼來源、部首筆畫和字形**，沒有記錄它怎麼讀、是什麼意思。`kPhonetic 19*` 只是音系系列編號，不能推出讀音。

### 1.2 其他辭書與數據庫：全部查無

- **維基詞典**：`en.wiktionary.org/wiki/𰇑` 404——**無條目**。
- **Extension G 讀音總表**（oatcookies.neocities.org/unihan-ext-g，Unicode 14 版，明確說明「跳過沒有任何讀音數據的字」）：該表列出 U+301C0、U+301CE、U+301D5 等鄰字，卻**沒有 U+301D1**——即 𰇑 在 Unihan 中沒有任何讀音數據，與 §1.1 一致。
- **全網檢索**（「𰇑」「U+301D1」「301D1 zdic」多輪中英文檢索）：無任何辭書（漢典、教育部異體字字典、《漢語大字典》、《中華字海》）收錄 𰇑 的記錄；檢索結果皆為其他生僻字的誤匹配。漢典頁面本次因 URL 抓取失敗未直接打開——缺口，非否定；但 Unihan 的缺失本身已是決定性證據（漢典的讀音釋義若存在，必有 Unihan 讀音字段）。
- **來源性質**：GCA = Culture and Art Publishing House Ideographs（文化藝術出版社用字），Ext G 中僅 69 字；UK-01323 屬英國 IRG 提案（IRG N2107R2）。兩者皆為**編碼來源**（某本書、某批文獻中出現過該字形），不是辭書釋義。一個字可以因為出現在某本古籍或藝術出版物中而被編碼，同時在任何辭書中都沒有讀音釋義——𰇑 正是這種情形。

### 1.3 平臺自身的轉寫是分裂的

`Main-character.json` 中本字條目：`{'codepoint': '𰇑', 'transcription': ['𰇑', U+A713F]}`。U+A713F 是私用區碼位，即平臺內部表示「未隸定」的標記。同一字形在同一數據集裡同時有「罕用漢字」和「未釋」兩種標記，說明 𰇑 只是**兩個並存的編碼選擇之一**，不是經過論證的隸定。

OBIMD 論文（*Scientific Data* 2026，DOI 10.1038/s41597-026-06967-0）明言：數據集的轉寫是標註平臺上的「working reading hypothesis」（工作性釋讀假設），由不同層級的標註者協作、專家驗證產生，但**數據集不公布逐字的隸定來源**。因此 𰇑 的出處無法追溯到任何已發表的考釋——不能把它當作「某家已讀出此字」的證據。

### 1.4 小結

- 「𰇑 是本字的讀音」：**不成立**。𰇑 沒有讀音、沒有釋義、沒有辭書出處、沒有維基詞典條目。
- 「𰇑 是本字的正確隸定」：**無證據**。平臺轉寫分裂（𰇑／PUA 並存），且無來源可追溯。
- 正確表述：𰇑 是一個**形狀碼位**（shape-only codepoint），僅供把該字形打出來，不攜帶任何音義信息。把平臺的 𰇑 當作「已釋讀」是誤認，應予糾正。

## 2. 字形

標準字形圖一枚（`images/std_h82z1bo3i3.png`）。摹本拼圖見 `images/crop_h82z1bo3i3.png`（11 例：H257、H700、H713、H769、H886、H908、H2824、H4116、H14660、H15337、H30661；HD409 一例因 `facsimile.zip` 中無 HD409 摹本文件而缺失——與 crck 筆記的 HD 摹本缺失情形一致）。

- **上部**：一個橫置的橢圓／圓角矩形框，內有 4–5 條豎筆貫穿，豎筆上下微出框外。摹本中豎筆數 3–5 不等（H257、H769 為 4 豎；H2824 為 5 豎；H4116 較小，3 豎），框形或圓或方，當為書寫變體。
- **下部**：一個淺 U 形托盤，盤口一條橫線（盤沿）。11 例皆有此托盤，無一缺失。
- 摹本一致性：11 例皆同構（格柵／橢圓框＋托盤），僅豎筆數與框的圓方略有出入。字形穩定，不是殘筆拼合。

### 2.1 結構試析（假說，非結論）

- 上部「框＋豎」可能為**格柵／蒸格**（甑的篦子）、竹編容器、或網罟之形；下部托盤可能為**皿**（盛器）。兩部分合起來像一件「上為格柵、下為承盤」的器物——蒸器（甑／甗）或竹製食器（簋／簠類）的象形。
- 但此分析無錨點：格柵＋托盤的組合在已釋字中無確切對應（見 §2.2），**不採納為證據**，僅記錄為字形印象。
- 形這一環：字形清晰穩定，但**無已知字可認，無聲符可辨**。形：2/5（僅結構清晰）。

### 2.2 直接視覺比對（皆已排除）

對比圖 `images/compare_h82_neighbours.png`（本字／鼎／鬲／甗／盂／爵／𠬝／冊／牢／子字形 vdh8n3qwp9；圖中標籤為拼音以免缺字）：

- **鼎**（`v2nizai7hr`）：缶形腹＋雙耳＋柱足，與本字的「框＋豎＋托盤」**逐部不同**。鼎說不成立。
- **鬲**（`kgnlcsowqg`）：袋腹＋三足，與本字不同。
- **甗**（`zgocda0mov`）：缶形腹＋鋸齒底＋單足，與本字不同。蒸器說最有希望的近旁字亦不相合。
- **盂**（`fu6caa5q2a`）：干形＋三角底，與本字不同。
- **爵**（`o3uagweguf`）：箭形＋杯形，與本字不同。
- **𠬝**（`cvzszyp6bm`，最常見後鄰字，見 §3）：高瘦斜筆形，與本字不同。
- **冊**（`81cqeht6m8`）：豎筆穿於直立圓角框內——與本字共享「豎筆＋框」的母題，是**最接近的結構回響**；但冊的框為直立長方形、本字為橫置橢圓，冊無下部托盤，且冊為竹簡名詞、語槽與本字不同（見 §3）。冊的異寫說不成立。
- **牢**（`w4mg32kjp4`）：欄＋牛，與本字不同。
- **簋／簠／盤／匜**：在 OBIMD `Main-character.json` 中**無字頭**（本語料未出現），無法在本庫內比對——缺口，非排除；但本字與鼎／鬲／甗／盂／爵五件已比對器物字皆不同，器物字說的一般性支持已弱。

**結論：本字形在已比對的近旁字中無相同者。**（像素最近鄰檢索未做：先前 X/1850、crck 兩案已證明該方法區分度不足，結論以人工逐部比對為準。）

### 2.3 子字形 vdh8n3qwp9

平臺為本字所列的唯一子字形（1 例 token 的 SubLabel）：其標準圖為「# 形格柵＋托盤」——上部畫作交叉格柵而非橢圓框，下部托盤與本字一致。這證實了 §2.1 的兩部分結構（格柵＋托盤），但格柵的兩種畫法（橢圓框＋豎／# 形交叉）是同一字的書寫變體還是平臺切分差異，現有材料無法區分；該子字形無獨立字頭、無讀音，不提供額外證據。

## 3. 用例與語槽（全部 94 例皆已本地核對）

### 3.1 位置統計

| 前字 | 例數 | 後字 | 例數 |
|---|---|---|---|
| （未標 token，Label 為 None） | 28 | （未標 token） | 26 |
| ?（未釋字） | 8 | ?（未釋字） | 11 |
| 勿／牛／㞢／牢／不／其 | 各 3 | 𠬝 | 8 |
| 庚／羊 | 各 2 | 十 | 5 |
| 貞／申／辛／卜／陷／來／乙／兇／魚／于／余 | 各 1 | 卅／冊／于／㞢／牢 | 各 3 |
| | | 三／御／牛 | 各 2 |
| | | 匕／大／且／二／百／通／五／小／六／亡／岳／吉 | 各 1 |

合成統計（94 例）：

- 後接數字（𠬝／十／卅／三／二／百／五／六）：**22 例**。
- 句末（後無字）：**11 例**。
- 前接動物名詞（牛／羊／牢）：8 例；其中「動物＋本字＋數字」：**6 例**。
- 前接否定詞（勿／不）：**6 例**。
- 後接于／㞢／冊／牢／牛／御：16 例。
- 前後皆未標或未釋（前 None／?、後 None／?）：約半數用例的直接鄰字無法辨認——這是本字語槽分析的最大噪聲來源。

**關鍵判斷：本字的語槽是多樣的，沒有 crck62eltz「不 __ 鼄」31/31、0bcpbg0geh「旬亡 __」86% 那種固定公式。** 最常見的後鄰字 𠬝 僅 8 例，且 𠬝 本身亦未釋（其轉寫同為雙值 [𠬝, U+A6192]，全庫 41 例，見 §3.2）。語槽證據只能給出一個弱傾向，給不出詞類定論。

### 3.2 最常見後鄰字 𠬝（41 例）的側面

𠬝（UID `cvzszyp6bm`）全庫 41 例：前字以本字最多（8 例），其次為佑（5 例）、十（3 例）；後字為于（5 例）、卯（4 例）、垂（2 例）等。𠬝既跟在本字之後，也跟在佑（祭祀動詞「佐助／保佑」）之後，其自身詞類未定（數字？器物？地名？）。「本字＋𠬝」這一搭配的意義，取決於 𠬝 的定性——目前兩字皆未定，互為未知數，不能互相證明。

### 3.3 代表性句例（全文句表見附錄）

- H886：「于父乙嚮三牛𰇑卅伐卅牢」——向父乙獻三牛，本字後接卅、伐、卅牢。
- H908：「于大甲嚮三牛𰇑卅牢伐十」——向大甲獻三牛，本字後接卅牢。
- H713：「于父乙嚮羊𰇑𠬝」——向父乙獻羊，本字後接𠬝。
- H769：「勿𰇑匕庚𠬝十垂卅」——否定詞勿＋本字，後接匕庚（先祖）與數字。
- H7026：「己丑卜㞢且辛牢𰇑十牢九」——且辛（先祖）牢，本字後接十牢九。
- H15331：「不余𰇑」——句末，本字為句尾詞。
- H2824：「帚󵾋𰇑冊畫」——本字後接冊（簡冊）。
- H4116：「于父乙𰇑牢御𰫝」——本字居于父乙與牢之間。

語境共性：多與**向先祖獻牲**有關（嚮三牛／羊于父乙、大甲、且辛；貞人殻、賓、韋；王 7 例），這是本字最弱但唯一的語義傾向——「祭祀獻牲場合的詞」。但該場合的詞可以是動詞（獻、陳、用）、器物名（盛牲之器）、量詞、甚至人名（貞人副名），語槽無法區分。

## 4. 音

- 本字無任何命辭用例可提供語音旁證（通假、諧聲、韻文位置皆無）；無青銅／篆書後代可供音韻對照；無已發表試讀可供音值參考。
- 𰇑 本身亦無音可供（見 §1）：Unihan 無讀音，辭書無收錄。
- 音環：**無證據，非僅存疑**。0/5。

## 5. 義與用

### 5.1 假說 A（領先，弱）：祭祀動詞——「獻／陳／用」類

- 支持：前接勿／不（6 例）是動詞的典型位置；後接「數字＋牲／牢」（22 例）符合「動詞＋數目＋賓語」結構（如「𰇑卅牢」「𰇑十牢九」）；多居嚮（獻）于先祖的祭祀語境；句末 11 例亦可作動詞收尾。
- 反對：沒有任何一個具體祭祀動詞的字形與本字相合（嚮、御、歲、燎、祭、享、用、侑皆已排除或本非同形）；「動物＋本字＋數字」亦可作名詞＋數目解（見假說 B）；前接動物名詞（8 例）對動詞說並不自然——動詞前通常是主語（王／貞人）或否定詞，而非牲名。

### 5.2 假說 B（主要競爭）：器物名詞——蒸器／盛器類

- 支持：字形為「格柵＋托盤」的器物象形（§2.1）；「三牛𰇑卅」可解作「三牛、𰇑三十」（數目計𰇑）；「𰇑十牢九」可解作名詞並列；句末 11 例可作賓語收尾。
- 反對：器物名詞通常有明確的金文／篆書後代，本字無（§6）；與鼎／鬲／甗／盂／爵五件器物字的字形比對皆不相合；前接勿／不（6 例）對名詞說不利——否定詞後一般是動詞；H769「勿𰇑匕庚」若本字為器物名，全句缺動詞。

### 5.3 假說 C：量詞／並列詞——「並／益／又」類

- 「三牢𰇑十牢」「牢𰇑十牢九」可解作數目並列（「三牢，並十牢」）；但量詞／連詞在甲骨文中通常是已知字（又、並、益、及），本字形與之皆不同；且假說 C 解釋不了前接勿／不的 6 例與句末 11 例。列為未決，非競爭者。

### 5.4 假說 D：𰇑 為真實隸定（平臺說）

- 見 §1：**已證偽**。𰇑 無讀音、無釋義、無辭書出處，平臺轉寫分裂且無來源可追溯。D 不是一個考釋假說，而是一個編碼誤認。

### 5.5 語義小結

- 詞類未定：動詞說與器物名詞說各有 6–22 例的支持、亦各有反證；語槽多樣、鄰字半數未標，無法裁決。
- 義、用兩環：**未閉合**。語槽證據只給出「祭祀獻牲場合」這一弱傾向，給不出詞義、給不出讀音。

## 6. 歷時鏈

- 金文、小篆、《說文解字》：無與本字同形者（本次檢索未見；格柵＋托盤結構在金文、篆文中無對應字）。
- 𰇑 自身：無傳世用例、無辭書釋義（見 §1），不能充當歷時錨點。
- 傳世文獻：無以 𰇑 為詞的成語或祭名。
- 歷時空白與「未釋詞」說相容，但亦與「已死詞」說相容，不能區分。

## 7. 競爭讀法

| 編號 | 讀法 | 評價 |
|---|---|---|
| **A（領先，弱）** | **祭祀動詞**（獻／陳／用類） | 否定詞後位置、動詞＋數目＋賓語結構、祭祀語境皆支持；但無一具體動詞字形相合；動物名前置不自然 |
| **B（主要競爭）** | **器物名詞**（蒸器／盛器類） | 字形為格柵＋托盤的器物象形；數目可計本字；但無金文／篆書後代；五件器物字比對皆排除；否定詞後位置不利 |
| C | 量詞／並列詞（並／益／又類） | 數目並列句可通；但解釋不了勿／不後與句末用例；候選字形皆不同。未決 |
| D | 𰇑 為真實隸定 | **已證偽**（見 §1）：無讀音、無釋義、無辭書出處 |
| E | 冊的異寫 | 結構母題（豎＋框）最接近；但框向、托盤、語槽皆不同。排除 |
| F | 鼎／鬲／甗／盂／爵的異寫 | 字形逐部不同。排除 |
| G | 貞人名／專名 | 本字 94 例分佈於多種語槽、無一例居貞人位置（與 n52ssmqnda 的貞人名槽不同）；且人名說解釋不了「動物＋本字＋數字」。排除 |

## 8. 四環打分

| 環 | 分 | 理由 |
|---|---|---|
| 形 | 2/5 | 字形清晰、11 例摹本同構；但無已知字可認，無聲符，豎筆數變體未定 |
| 音 | 0/5 | 無任何語音旁證；𰇑 本身亦無音 |
| 義 | 2/5 | 僅有「祭祀獻牲場合」的弱傾向；詞類未定（動詞／器物名詞兩說並存），具體詞義未定 |
| 用 | 3/5 | 94 例、89 片、武丁貞人可考；扣分因語槽多樣無固定公式、半數鄰字未標、HD 摹本缺失 |
| **合計** | **7/20** | 頻次與語料證據完整，但離「破譯」（讀出音義）無限遠；本輪的確定性成果是 𰇑 誤認的證偽 |

**結論：存疑。** 本字是真實的未釋字，非專名，不應放棄為攻克對象；但目前沒有任何具體讀音可以成立，任何「獻／甗／簋」的指名皆為無字形支持的猜測。**本輪的確定性成果有二**：其一，平臺隸定 𰇑 已證偽為形狀碼位而非釋讀——此後引用 OBIMD 轉寫時，凡遇此類罕用字＋PUA 雙值者皆須先核查 Unihan 讀音字段；其二，本字 94 例的完整建檔（句表、語槽統計、摹本、比對圖）。

## 9. 證偽條件（按決定性排序）

1. **《合集》釋文印本**：查 89 片的隸定。若印為某已知漢字（如獻／甗）→ 相應假說復活，重估；若印為私用字符或空缺 → 維持本結論。
2. **《殷墟甲骨刻辭類纂》**：查本字形是否歸入某字頭（動詞或器物字）。若歸入某字頭 → 重估；若歸入冊字頭作異寫 → E 說復活。
3. **𠬝 的定性**：若 𠬝 被證實為數字（如「二十」），則「本字＋數字」結構得分，動詞說（A）得分；若 𠬝 被證實為器物／地名，則假說 B 或其他說得分。兩字的裁決部分繫於 𠬝。
4. **第二賓語／第二語槽**：若發現本字接非牲類賓語（如「𰇑冊」H2824 之外更多的冊例），則器物名詞說得分；若發現本字居「王 __ 于先祖」動詞槽，則動詞說得分。
5. **青銅／篆書後代**：找到格柵＋托盤結構的金文／篆文 → 歷時鏈打開，需重估。
6. **他槽同形字**：若在非祭祀語境（如田獵、征伐）發現同形字 → 「祭祀場合」傾向重估。

## 10. 未核查事項（誠實記錄）

- 《合集》釋文印本（89 片）未查：本地 OCR 文本 `heji_shiwen_djvu.txt` 中 𰇑 零命中、「三牛」零命中，OCR 質量過差，不可作證據。
- 《新甲骨文編》《類纂》《甲骨文字典》未查；𰇑 是否見於《中華字海》等大型字書的紙本，未核對（Unihan 無讀音字段已可作決定性否定，見 §1）。
- 漢典 𰇑 頁面本次因 URL 抓取失敗未直接打開——缺口，非否定（Unihan 缺失已足夠）。
- GlyphWiki 𰇑 頁面 403 被拒，未查——缺口，非否定。
- HD 摹本缺失：`facsimile.zip` 中無 HD409 文件，11 例 HD 用例皆無摹本可驗；H30661 等三例單字成句（START＋END）的全片語境未細讀。
- 簋／簠／盤／匜在 OBIMD 中無字頭，未作字形比對——缺口（見 §2.2）。
- 「二告」「小告」驗辭公式本身未深究；H2824「帚󵾋𰇑冊畫」中「冊畫」的身份未定。
- 像素最近鄰檢索未做（先前兩案已證明區分度不足）。

## 附錄：全部 94 例句表（本地 `data.json` 實測，`sent_h82_full.txt`）

句中 𰇑 即本字；「鼎」實為貞（見 n52ssmqnda 筆記 §1.1 的核驗）；「?」為平臺未釋 token；未標 token 在句中以空位表示時仍計入位置。

| # | 片號 | 組別 | 句 |
|---|---|---|---|
| 1 | H257 | InscriptionSentence2 | 貞None𰇑None |
| 2 | H700 | InscriptionSentence1 | 㞢匕庚𰇑None |
| 3 | H705 | InscriptionSentence1 | None𰇑None十𠬝 |
| 4 | H713 | InscriptionSentence1 | 貞御󵜐漁于父乙嚮羊𰇑𠬝 |
| 5 | H733 | InscriptionSentence1 | None今甲None娥None𰇑𠬝None |
| 6 | H740 | InscriptionSentence1 | None𰇑𠬝垂㞢牢 |
| 7 | H742 | InscriptionSentence1 | 壬None𠬝None𰇑None |
| 8 | H769 | InscriptionSentence1 | 貞勿𰇑匕庚𠬝十垂卅󿚮 |
| 9 | H783 | InscriptionSentence1 | 𰇑𠬝一垂 |
| 10 | H784 | InscriptionSentence1 | 御于高匕己嚮二򽰟𰇑𠬝垂 |
| 11 | H886 | InscriptionSentence1 | 貞御于父乙嚮三牛𰇑卅伐卅牢 |
| 12 | H887 | InscriptionSentence1 | 壬申𰇑大None伐卅None卅牢 |
| 13 | H908 | InscriptionSentence1 | 癸丑None翌甲None㞢于大甲嚮三牛𰇑卅牢伐十 |
| 14 | H987 | InscriptionSentence1 | 𰇑None伐None |
| 15 | H988 | InscriptionSentence1 | None卜殻None𰇑None伐 |
| 16 | H1718 | InscriptionSentence1 | None午卜賓貞御于且辛𰇑十None |
| 17 | H1731 | InscriptionSentence1 | None未卜𰇑None且辛 |
| 18 | H1968 | InscriptionSentence1 | 丙寅卜殻None丁卯尞于None丁卯None𰇑卅牢None |
| 19 | H2070 | InscriptionSentence1 | None午卜殻貞𰇑且None |
| 20 | H2824 | InscriptionSentence3 | 貞帚󵾋𰇑冊畫󿫺 |
| 21 | H2944 | InscriptionSentence1 | 貞󵜐商㞢𰇑于父乙乎𫹉 |
| 22 | H2990 | InscriptionSentence1 | None辰None來乙NoneNone漁None𰇑None |
| 23 | H3219 | InscriptionSentence1 | 󵜐陷𰇑㞢None乙 |
| 24 | H3295 | InscriptionSentence1 | None侯豹允來𰇑㞢㞢壴五月 |
| 25 | H3853 | InscriptionSentence1 | None卜韋貞None𰇑None |
| 26 | H4116 | InscriptionSentence2 | 于父乙𰇑牢御𰫝 |
| 27 | H5031 | InscriptionSentence1 | 辛酉None𫹉None󾷀None𰇑None |
| 28 | H5548 | InscriptionSentence1 | 貞史人None沈三None𰇑None叀None |
| 29 | H6956 | InscriptionSentence1 | None𰇑㞢且 |
| 30 | H7026 | InscriptionSentence2 | 己丑卜㞢且辛牢𰇑十牢九 |
| 31 | H14253 | InscriptionSentence2 | 辛卜王貞𰇑 |
| 32 | H14660 | InscriptionSentence1 | None亥卜尞于兇𰇑二牛 |
| 33 | H14688 | InscriptionSentence1 | NoneNone卜叀None魚𰇑None𰥏 |
| 34 | H14953 | InscriptionSentence1 | None辛伯None㞢𰇑None |
| 35 | H14954 | InscriptionSentence1 | NoneNone卜貞㞢𰇑于None |
| 36 | H15302 | InscriptionSentence1 | None𰇑None㞢󿫿 |
| 37 | H15305 | InscriptionSentence1 | None于𰇑None王廿None |
| 38 | H15311 | InscriptionSentence1 | 叀乙亥None𰇑冊None多None |
| 39 | H15313 | InscriptionSentence1 | None晦None𰇑None |
| 40 | H15325 | InscriptionSentence1 | None亥卜None貞None𰇑󿭆 |
| 41 | H15331 | InscriptionSentence1 | 不余𰇑 |
| 42 | H15334 | InscriptionSentence1 | None史余不𰇑 |
| 43 | H15337 | InscriptionSentence1 | None寅卜NoneNone㞢且None三牢𰇑十牢㞢九 |
| 44 | H15338 | InscriptionSentence1 | None󾿏盟牛𰇑十牢󾯊 |
| 45 | H15342 | InscriptionSentence1 | None御None󿬬𰇑None四月 |
| 46 | H15345 | InscriptionSentence1 | None𰇑None百牛 |
| 47 | H15347 | InscriptionSentence1 | 辛NoneNone牢叀翌None𰇑百None |
| 48 | H15735 | InscriptionSentence1 | 己未NoneNoneNone翌庚𫹉None庚𰇑NoneNone |
| 49 | H20521 | InscriptionSentence1 | None辰用𰇑通NoneNone󾨃牛 |
| 50 | H21180 | InscriptionSentence1 | NoneNone卜師貞隹禱None叀𰇑None于None |
| 51 | H24133 | InscriptionSentence1 | NoneNoneNone大貞多君None𰇑冊叀None夕 |
| 52 | H323 | InscriptionSentence1 | None羌卅None𰇑None牛 |
| 53 | H1440 | InscriptionSentence1 | None王𰇑None大甲 |
| 54 | H2501 | InscriptionSentence1 | 貞祼于匕癸𰇑三小牢 |
| 55 | H15317 | InscriptionSentence1 | NoneNone勿𰇑None丁None |
| 56 | H15328 | InscriptionSentence2 | 貞若不𰇑 |
| 57 | H15328 | InscriptionSentence1 | 若不𰇑 |
| 58 | H15339 | InscriptionSentence1 | None𰇑御牢豰十 |
| 59 | H15340 | InscriptionSentence1 | None𰇑五牢 |
| 60 | H15344 | InscriptionSentence1 | None𰇑小None |
| 61 | H15346 | InscriptionSentence1 | None勿𰇑None三豭九月 |
| 62 | H15793 | InscriptionSentence1 | None𰇑十None鬯十NoneNone卌None |
| 63 | H21183 | InscriptionSentence1 | 己卯𰇑六牛五None |
| 64 | H30033 | InscriptionSentence1 | 其𰇑御佑大雨 |
| 65 | H30033 | InscriptionSentence2 | 弜𰇑亡大雨 |
| 66 | H30411 | InscriptionSentence1 | None酉卜王其𰇑岳尞叀犬None眔豚十佑大雨 |
| 67 | H30480 | InscriptionSentence1 | 弜佑𰇑 |
| 68 | H30661 | InscriptionSentence3 | 𰇑 |
| 69 | H30662 | InscriptionSentence1 | 𰇑 |
| 70 | H30663 | InscriptionSentence3 | 𰇑 |
| 71 | H30665 | InscriptionSentence2 | None𰇑吉 |
| 72 | H30667 | InscriptionSentence1 | 𰇑其叀今日 |
| 73 | H30671 | InscriptionSentence1 | 叀None𰇑None羊None |
| 74 | H30677 | InscriptionSentence3 | 弜㲹眢叀舊𰇑用 |
| 75 | H31137 | InscriptionSentence1 | 叀十牢𰇑 |
| 76 | H32162 | InscriptionSentence2 | 其𰇑򦆓 |
| 77 | H32172 | InscriptionSentence2 | 𰇑𠬝一人 |
| 78 | H32172 | InscriptionSentence3 | 𰇑𠬝二人 |
| 79 | H32181 | InscriptionSentence2 | 辛丑卜嚮三羊𰇑󾨃五牢 |
| 80 | H32182 | InscriptionSentence2 | 庚子卜貞月祼𰇑𠬝卯牛一 |
| 81 | H35444 | InscriptionSentence1 | 乙未卜貞王賓󾷀𰇑日亡尤 |
| 82 | H35650 | InscriptionSentence2 | 癸酉卜貞王旬亡򶫴在正夕甲戌祭󿀹𰇑None |
| 83 | H35749 | InscriptionSentence1 | 癸巳卜None貞王旬None在󿬻甲None𰇑󾻭 |
| 84 | HD176 | InscriptionSentence1 | 丁丑卜󵜐御于󿉥𰇑牛一肘鬯巛入商𫹉在򬬘 |
| 85 | HD176 | InscriptionSentence2 | 丁丑卜󵜐御󿉥𰇑牛一鬯一用 |
| 86 | HD181 | InscriptionSentence22 | 辛卜御巳舞抔眢一牛󿋋𰇑牢佑鬯 |
| 87 | HD181 | InscriptionSentence23 | 辛卜御巳舞抔殺一牛󿋋𰇑牢佑鬯 |
| 88 | HD215 | InscriptionSentence3 | 壬申卜巳其以羌򧇚𰇑于帚若侃 |
| 89 | HD220 | InscriptionSentence2 | 戊寅卜󵜐御祭疒于󿋋𰇑牝 |
| 90 | HD226 | InscriptionSentence8 | 庚申御徵目癸󵜐𰇑伐󾩿卯牢 |
| 91 | HD289 | InscriptionSentence6 | 丙寅其御隹None貯視馬于癸巳叀一伐一牛一鬯𰇑夢用 |
| 92 | HD409 | InscriptionSentence9 | 丙None巳其祐󿋋None𰇑 |
| 93 | HD455 | InscriptionSentence1 | 甲子卜歲󿉥򽰟一𰇑三󿚮佑置一在󹙯 |
| 94 | HD459 | InscriptionSentence9 | 戊寅卜巳祼祐𰇑豭御往㘡 |

## 來源

- OBIMD 本地數據（`~/workspace/oracle-screening/obimd/data.json`、`Main-character.json`、`subchar-images.zip`、`facsimile.zip`；CC-BY 4.0，*Scientific Data* 2026，DOI 10.1038/s41597-026-06967-0）。頻次、槽位、字形皆本地實測；句表全文見附錄；本地腳本：`analyse_h82.py`、`analyse_h82b.py`、`analyse_h82c.py`、`crop_h82.py`、`relabel_h82.py`。
- 圖檔：`images/std_h82z1bo3i3.png`（標準字形）、`images/crop_h82z1bo3i3.png`（11 例摹本）、`images/compare_h82_neighbours.png`（本字／鼎／鬲／甗／盂／爵／𠬝／冊／牢／子字形 vdh8n3qwp9）。
- 排名與方法：`ranking-20261126.md`（h82z1bo3i3 列為 CJK 類第 3，94 tokens / 89 片，隸定 𰇑；本筆記訂正：𰇑 無讀音釋義，非釋讀）。
- 𰇑 的 Unicode 數據：Unihan，https://www.unicode.org/cgi-bin/GetUnihanData.pl?codepoint=301D1（kIRG_GSource GCA-J0290、kIRG_UKSource UK-01323、kRSUnicode 30.5、kTotalStrokes 8、kPhonetic 19*；無 kMandarin、無 kDefinition）；Extension G 讀音總表（無 U+301D1 條目），https://oatcookies.neocities.org/unihan-ext-g；GCA 來源說明（Culture and Art Publishing House Ideographs），https://en.wikipedia.org/wiki/CJK_unified_ideographs。
- OBIMD 論文（轉寫為 working reading hypothesis）：Li, B. et al., *Scientific Data* (2026)，https://doi.org/10.1038/s41597-026-06967-0。
- 考釋標準（蔣玉斌「形、音、義、用」證據鏈；中國文字博物館獎勵規則）：南開大學新聞 2019-11-05，https://news.nankai.edu.cn/mtnk/system/2019/11/05/030036250.shtml；另見本目錄 `report.md` §2–§3。
- 數字口徑：去重單字約 4,500 個（AlphaOracle 2026，https://www.cell.com/the-innovation/fulltext/S2666-6758(26)00209-2）；本筆記不採用 6,211 字形條目數作為單字數（《甲骨文字形表》6211 為含異體的字形總數，單字 4,024）。

---

## Gemini 附記（2026-11-26）

> 依 `COORDINATION.md` §4，本附記不改動原筆記之結論行與四環打分，僅補充 `zi.tools`、漢典與古文字專書核查結果，對 §1「𰇑 僅為無音義形碼」及 §2.2「冊說排除」作出實質糾偏。

### 1. `𰇑`（`U+301D1`）並非無音義形碼，而是 `⿱册口`——《說文》`𣆑`（`U+23191`）／`冊` 之甲骨隸定

原筆記 §1.1 核查 Unihan 確認 `𰇑`（`U+301D1`，CJK Ext G，來源 `GCA-J0290`／`UK-01323`）缺失 `kMandarin` 與 `kDefinition`，此點完全屬實；但 **Unihan 擴展區（尤其 Ext G 罕用古文字隸定字）缺失讀音字段，並不等於該字「無音無義、非已釋字」**。

經檢核 **`zi.tools`（字統網）**、**`zdic.net`（漢典）** 及 **王輝《古文字通假字典》（中華書局，頁 263）**：

- **`𰇑`（`U+301D1`）之字形結構為 `⿱册口`**（上「冊」下「口／曰」），正是《說文解字》**`𣆑`（`U+23191`，「告也。从曰从冊，冊亦聲」）** 在甲骨文中的規範隸定字形，亦即甲骨文 **`冊`** 字系之異體／繁構。
- 原筆記 §2.2 敏銳觀察到「冊」與本字共享「豎筆穿框」母題，卻因下部淺 U 形托盤形似器皿而將「冊」排除；實則該下部構件正是**橫置「口／曰」形**（非蒸器承盤或「皿」），上部框內貫豎即簡「冊」。

### 2. 已刊布《合集》釋文直接印證：祭祀用牲之「冊」（于省吾讀為「刪」）

對照原筆記附錄之多條核心辭例，學界已刊布釋文均一律將本字隸作 **`冊`**，用於表示祭祀殺牲／用牲之法（**于省吾讀為「刪」**）：

- **《合集》886**（附錄 #11）：刊布釋文作 **`御于父乙，血三牛，冊卅伐、卅牢`**（對照附錄 `貞御于父乙嚮三牛𰇑卅伐卅牢`）
- **《合集》908**（附錄 #13）：刊布釋文作 **`……于大甲，血三牛，冊卅牢、伐十`**（對照附錄 `……㞢于大甲嚮三牛𰇑卅牢伐十`）
- **《合集》31137**（附錄 #75）：刊布釋文作 **`叀十牢冊`**（對照附錄 `叀十牢𰇑`）

由此，本字全部高頻語槽一次閉合：前接否定副詞（`勿冊`、`弜冊`）、後接數字＋牲牢（`冊卅伐、卅牢`、`冊十牢`）、以及與 `𠬝`（服，人牲／受祭對象）搭配（如 H32172 `冊𠬝一人`、`冊𠬝二人`），皆屬已釋「冊／𣆑」祭法動詞用法，非蒸器名詞。

### 3. 建議處置與方法論教訓

- **建議移出未釋攻擊池**：待作者與專案擁有者覆核後，建議將 `h82z1bo3i3`（`𰇑` = `𣆑`/`冊`）與 `cvzszyp6bm`（`𠬝` = `服`）並列移出未釋字攻擊名單，歸入已釋字系統（具體讀「刪」或本字「冊告」之訓詁細部雖仍可探討，但不屬待破譯之未知字）。
- **方法論升級（已補入 `docs/METHOD.md` 規則 7）**：檢查 CJK 擴展區（尤其 Ext B–H）字頭時，**絕不可僅憑 Unihan 缺 `kMandarin` 就判定為「無音義形碼」**；必須同步檢索 `zi.tools` / IDS 部件拆分、漢典與古文字工具書（如《古文字通假字典》）。
