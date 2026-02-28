# COMPRESSED_SPEC_TEMPLATE.md  
infinite-epic（仮）  
Compressed Specification Template  
Version: 1.0

---

# PURPOSE  
このテンプレートは、AI が誤解せずに構造を継承できるよう、  
infinite-epic の仕様を **高密度・低トークン・非自然言語的** に記述するための骨格である。  
すべてのセクションは SPEC と WHY のペアで構成する。

---

# RULES  
[FORMAT:セクションは #SECTION_NAME で開始]  
[FORMAT:Key=Value を基本とする]  
[FORMAT:[LABEL:content] 形式を使用]  
[FORMAT:複数値は A;B;C]  
[FORMAT:階層は A(sub1;sub2)]  
[FORMAT:自然言語の長文は禁止]  
[FORMAT:SPEC と WHY は必ずペア]  
[FORMAT:情報密度を最大化]  
[FORMAT:推測禁止]  
[FORMAT:未定義の語彙を勝手に追加しない]  
[FORMAT:MASTER_HANDBOOK を正本とする]

---

# PROJECT  
[SPEC:NAME=infinite-epic]  
[SPEC:VERSION=1.0]  
[WHY:プロジェクト識別のため]

---

# PHILOSOPHY  
[SPEC:ForkEquivalence=ON]  
[SPEC:StructuralIntegrity=MAX]  
[SPEC:WHYRetention=MANDATORY]  
[SPEC:AI_Relay=CORE]  
[WHY:プロジェクトの中核哲学を保持するため]

---

# USER_MODEL  
#（例：ユーザーの性質・行動原理を圧縮記述する領域）  
[SPEC:U1=好奇心(高)]  
[SPEC:U2=分岐許容(最大)]  
[SPEC:U3=構造優先(強)]  
[WHY:AI がユーザーの行動原理を誤解しないため]

---

# RELAY_PACKET  
[SPEC:Layers=SESSION_LOG;COMPRESSED;SAMPLES]  
[SPEC:SingleCodeblock=TRUE]  
[SPEC:NoExternalContext=TRUE]  
[SPEC:NextAI_MustFollow=TRUE]  
[WHY:AI リレーの形式を固定し、構造崩壊を防ぐため]

---

# SESSION_LOG  
[SPEC:Format=Bullet]  
[SPEC:Content=実際の作業のみ]  
[SPEC:NoGuess=TRUE]  
[WHY:最小限の歴史記録として必要]

---

# SAMPLES  
[SPEC:Preserve=原文]  
[SPEC:NoSummary=TRUE]  
[SPEC:NoOmission=TRUE]  
[SPEC:Types=UI;TIPS;relations.json;文体;語彙]  
[WHY:UX・文化・トーンを保持するため]

---

# COMPRESSED_SECTIONS  
#（プロジェクト固有の構造を追加する領域。必要に応じて拡張する）

#WORLD  
[SPEC:WorldModel=未定義]  
[WHY:後続セッションで定義するための空枠]

#CHARACTERS  
[SPEC:CharacterModel=未定義]  
[WHY:後続セッションで定義するための空枠]

#MECHANICS  
[SPEC:Mechanics=未定義]  
[WHY:後続セッションで定義するための空枠]

---

# COPYRIGHT  
[SPEC:License=Copyleft(CC-BY-SA-like)]  
[SPEC:DynamicCredit=ON]  
[WHY:文化継承と作者名の保持のため]

---

# END  
