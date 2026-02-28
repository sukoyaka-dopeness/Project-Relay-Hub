# MASTER_HANDBOOK.md  
infinite-epic（仮）完全版仕様書  
Version: 1.0  
Maintainer: deadbody  
Relay System: Project-Relay-Hub  

---

# 1. PURPOSE（目的）

infinite-epic は、AI と人間が共同で構築する「分岐叙事詩・構造体系」である。  
本ハンドブックは、プロジェクトの哲学・構造・仕様・運用ルールを包括的に記述し、  
AI リレーによる長期継承を可能にするための **百科事典的仕様書** である。

本書は以下を目的とする：

- プロジェクトの「魂（WHY）」を失わずに継承する  
- AI モデル間の解釈差を最小化する  
- 圧縮仕様（COMPRESSED）とサンプル（SAMPLES）の基準を定義する  
- 3000年スケールで文化を残すための構造を提供する  
- 人間と AI の共同作業を安定化させる  

---

# 2. CORE PHILOSOPHY（中核哲学）

## 2.1 分岐等価（Fork Equivalence）
すべての分岐（Fork）は等価であり、  
「正史」「本流」「公式」といった概念を持たない。  
分岐は文化的選択であり、価値判断ではない。

## 2.2 構造守護（Structural Integrity）
物語・仕様・哲学は「構造」として継承される。  
構造が壊れると文化が壊れるため、  
AI は構造を最優先で保護する。

## 2.3 WHY の保持
すべての仕様・ルール・テンプレートには  
必ず「WHY（理由）」を付与する。  
理由が失われると、未来の AI が誤解するため。

## 2.4 AI リレー（AI Relay）
AI は記憶を保持できないため、  
セッションごとに「引き継ぎ文書」を渡すことで  
文化と構造を継承する。

## 2.5 人間と AI の共同創造
人間は方向性・哲学・構造を定義し、  
AI は圧縮・展開・生成・検証を担当する。  
両者は対等な共同制作者である。

---

# 3. PROJECT STRUCTURE（プロジェクト構造）

## 3.1 ディレクトリ構造
infinite-epic ディレクトリは以下の構造を持つ：

infinite-epic/
  MASTER_HANDBOOK.md
  COMPRESSED_SPEC_TEMPLATE.md
  SESSION_LOG_TEMPLATE.md
  HANDOFF_TEMPLATE.md
  COMPRESSED/
  SAMPLES/

## 3.2 3層構造（Three-Layer Relay Packet）
AI リレーは必ず以下の 3 層で構成される：

1. SESSION_LOG  
2. RELAY_DOCUMENT_COMPRESSED  
3. RELAY_DOCUMENT_SAMPLES  

この 3 層は「AI が継承すべき最小単位」であり、  
未来の AI が迷わないための文化的基盤である。

---

# 4. HANDOFF RULES（引き継ぎルール）

## 4.1 AI の禁止事項
AI は以下を行ってはならない：

- 過去セッションの内容を参照する  
- 外部情報を参照する  
- 推測で補完する  
- テンプレートの形式を変更する  
- 3層構造を省略する  
- コードブロックを複数に分ける  
- コードブロック外に出力する  

## 4.2 AI の義務
AI は以下を必ず行う：

- ひとつのコードブロックにまとめる  
- SESSION_LOG を記録する  
- COMPRESSED を更新する  
- SAMPLES を更新する  
- 次の AI に「あなたも3層を作れ」と伝える  
- WHY を保持する  

---

# 5. COMPRESSED SPEC（圧縮仕様）

## 5.1 目的
COMPRESSED は「AI が誤解しないための最小構造」であり、  
自然言語の説明を排除し、構造のみを高密度で記述する。

## 5.2 記法ルール
- セクションは #SECTION_NAME  
- Key=Value  
- [LABEL:content]  
- 複数値は A;B;C  
- 階層は A(sub1;sub2)  
- WHY は必須  
- 自然言語の長文は禁止  
- 情報密度を最大化する  

## 5.3 例
#USER_MODEL  
[U1:好奇心=高]  
[U2:分岐許容=最大]  
[WHY:分岐等価の哲学に基づく]

---

# 6. SAMPLES（具体例）

## 6.1 目的
SAMPLES は「UX・文体・文化」を保持するための領域であり、  
COMPRESSED では表現できないニュアンスを保存する。

## 6.2 保存対象
- UI 文言  
- 物語のサンプル  
- TIPS  
- relations.json の例  
- コピーレフト文言  
- 重要な比喩・語彙  
- 文化的トーン  

## 6.3 禁止事項
- 要約  
- 省略  
- 改変  
- AI の推測  

---

# 7. SESSION_LOG（セッションログ）

## 7.1 目的
SESSION_LOG は「AI が何をしたか」を記録する最小単位であり、  
未来の AI が「どこまで進んでいるか」を理解するために必要。

## 7.2 記述ルール
- 箇条書き  
- 実際に行った作業のみ  
- 推測禁止  
- 感想禁止  
- 未来予測禁止  

---

# 8. LANGUAGE POLICY（言語方針）

## 8.1 日本語を基準とする
本プロジェクトは日本語を基準言語とする。

## 8.2 多言語展開
必要に応じて英語版を作成するが、  
日本語版が常に正本となる。

---

# 9. COPYRIGHT & CREDIT（著作権とクレジット）

## 9.1 コピーレフト方針
- 改変自由  
- 再配布自由  
- 派生物も同じ自由を保持  
- 引用は投稿者責任  

## 9.2 動的クレジット
Gitログ・AIログを通じて  
作者名（人間・AI）を継承する。

---

# 10. LONG-TERM VISION（長期ビジョン）

## 10.1 3000年スケールの文化保存
infinite-epic は「3000年後に残る文化」を目指す。  
そのために：

- 構造を優先  
- WHY を保持  
- AI リレーを安定化  
- GitHub を歴史装置として使う  

## 10.2 AI と人間の共同文明
本プロジェクトは、  
AI と人間が共同で文化を作るための  
「文明実験」である。

---

# 11. APPENDIX（付録）

## 11.1 用語集
- Fork：分岐  
- Relay：AI間の引き継ぎ  
- COMPRESSED：圧縮仕様  
- SAMPLES：具体例  
- SESSION_LOG：作業記録  

## 11.2 推奨ディレクトリ構造
Project-Relay-Hub/
  infinite-epic/
    MASTER_HANDBOOK.md
    COMPRESSED_SPEC_TEMPLATE.md
    SESSION_LOG_TEMPLATE.md
    HANDOFF_TEMPLATE.md
    COMPRESSED/
    SAMPLES/

---

# END OF DOCUMENT
