# project-20260303-SESSION3.md

# 🧠 PROJECT RELAY HUB — SESSION HANDOFF DOCUMENT

---

# 1️⃣ SESSION_LOG

## SESSION_ID
20260303-Session3-ChatGPT

## PARTICIPANTS
- User
- ChatGPT

## SUMMARY_OF_THIS_SESSION

本セッションで実際に行った作業のみを記録する。

1. 自己ループ正式ポリシー化の合意  
   - 自己ループ（node → same node）は許容する方針を確定  
   - 「mini-loop story」として意味を持つ構造であれば有効  
   - 禁止しないことを正式仕様に含めることを決定  

2. degree と heat の分離確定  
   - degree = 構造的接続数  
   - heat = 読者活動指標  
   - 別メタデータとして管理する方針を確定  

3. ノード永続方針の整理  
   - ノードは原則削除しない  
   - 執筆者が望めば「表示されにくくする」扱いにできる  
   - Git履歴削除は行わない  
   - 「見えにくくなる」ことを事実上の撤回とする設計思想を確認  

4. クロスプロジェクト接続思想の合意  
   - 類似プロジェクトの出現を歓迎  
   - 同フォーマット採用であればクロスリポジトリ接続可能  
   - 物語規格としての拡張性を持たせる方針を確認  

5. 名称候補の整理  
   - StoryGraph  
   - Narrative Multiverse  
   - Living Narrative  
   - Story Genome  
   - Forkverse（追加）  
   - NGP / ONF は副題・規格名候補とする  

6. DAOは後期フェイズ構想として明記する方針決定  

7. 将来設計思想の確認  
   - Webアプリ化を否定しない  
   - スマートフォンアプリ化を否定しない  
   - P2P化可能性を排除しない  
   - 独立ドメインの存在と思想的中央性は別概念であることを確認  

---

# 2️⃣ RELAY_DOCUMENT_COMPRESSED

## PROJECT_CORE

GRAPH_BASED_NARRATIVE_SYSTEM  
NODE_PERSISTENT  
DELETE=discourage  
VISIBILITY=adjustable  

SELF_LOOP=permit  
SELF_LOOP_TYPE=mini_loop_story  

DEGREE=structural_metric  
HEAT=reader_activity_metric  
METADATA_SPLIT=degree_heat  

CROSS_REPO_LINK=permit  
EXTERNAL_NODE_FORMAT=repo_url::node_id  

FORMAT_OPEN_STANDARD=aspired  
MULTI_PROJECT_COMPATIBLE=true  

DAO_PHASE=future  
P2P_POSSIBLE=true  
CENTRAL_SERVER≠CENTRAL_STRUCTURE  

NAME_CANDIDATES=
- StoryGraph
- Narrative Multiverse
- Living Narrative
- Story Genome
- Forkverse

PROTOCOL_CANDIDATES=
- Narrative Graph Protocol (NGP)
- Open Narrative Format (ONF)

---

## DESIGN_PRINCIPLES

- ノードは永遠に残る  
- 表示調整は可能  
- 削除よりも視認性制御  
- 構造と人気は分離  
- 物語規格を目指す  
- 類似プロジェクト歓迎  
- 絶滅耐性設計  

---

## UI_POLICY_INITIAL

- 初期段階では気順UIなし  
- 将来的に heat 優先表示可能  
- 高次数ノードと高heatノードは一致するとは限らない  

---

# 3️⃣ RELAY_DOCUMENT_SAMPLES

## SAMPLE: relations.json (self-loop)

```json
{
  "from": "node-001",
  "to": "node-001",
  "type": "self_loop",
  "label": "internal_reflection"
}

SAMPLE: cross-repo link
{
  "from": "node-010",
  "to": "https://github.com/other/project::node-88",
  "type": "external_reference"
}

SAMPLE: visibility control metadata
{
  "node_id": "node-042",
  "visibility": "low",
  "reason": "author_request"
}

SAMPLE: degree & heat separation
{
  "node_id": "node-015",
  "degree": 12,
  "heat": 87
}

END OF SESSION 3 DOCUMENT
