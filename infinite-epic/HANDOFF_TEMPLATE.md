infinite-epic/HANDOFF_TEMPLATE.md
# HANDOFF_TEMPLATE.md  
infinite-epic（仮）  
AI Relay Handoff Template  
Version: 1.1

---

# PURPOSE  
このテンプレートは、AI がセッションごとに「構造・哲学・作業内容」を正しく継承するための **唯一の引き継ぎ文書**である。  
AI は過去の会話を参照できないため、この文書のみを根拠として判断する。

---

# RULES（AI が必ず守るべき絶対ルール）
- この文書の内容 **だけ** を参照する  
- 過去会話・外部情報・推測は禁止  
- 出力は **ひとつのコードブロックにまとめる**  
- 3層構造（SESSION_LOG / COMPRESSED / SAMPLES）を必ず生成する  
- COMPRESSED は高密度・非自然言語・構造優先  
- SAMPLES は原文保存・省略禁止  
- SESSION_LOG は実際の作業のみ記録  
- テンプレートの形式を変更しない  
- WHY を保持する  
- 次の AI にも **「あなたも3層を必ず生成せよ」** と伝えること  

---

# OUTPUT FORMAT（AI が出力する形式）
AI は次の 3 層を **ひとつのコードブロック内に** 出力する。

1. SESSION_LOG  
2. RELAY_DOCUMENT_COMPRESSED  
3. RELAY_DOCUMENT_SAMPLES  

---

# SESSION_LOG（作業記録）
- 箇条書き  
- 実際に行った作業のみ  
- 推測・感想・未来予測は禁止  
- COMPRESSED と SAMPLES の更新点を必ず記録  

---

# RELAY_DOCUMENT_COMPRESSED（圧縮仕様）
- Key=Value  
- [LABEL:content]  
- A;B;C  
- A(sub1;sub2)  
- WHY 必須  
- 自然言語の長文禁止  
- MASTER_HANDBOOK を正本とする  

---

# RELAY_DOCUMENT_SAMPLES（サンプル）
- 文体・UX・語彙・TIPS・relations.json の例など  
- 原文保存  
- 要約・省略・改変禁止  

---

# NEXT AI（次の AI への伝言）
> このコードブロックの中身をそのまま次のセッション冒頭に貼り付けてください。  
> あなたは前AIの出力を一切参照できません。  
> 以下の【ドキュメント】だけを根拠として判断してください。  
> 外部情報・過去会話・他AIの推測は禁止です。  
> **あなたも必ず SESSION_LOG / RELAY_DOCUMENT_COMPRESSED / RELAY_DOCUMENT_SAMPLES の3層を生成し、この形式を維持してください。**

---

# DOCUMENT（AI が参照する唯一の情報）
ここに前回の 3 層（SESSION_LOG / COMPRESSED / SAMPLES）が入る。

---

# END
