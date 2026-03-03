# SESSION_LOG

- 作業1: Session 1〜3の引き継ぎドキュメントを全件読み込み・内容確認
- 作業2: bridge_to の方向性仕様を確定（directed=false/true の選択式）
- 作業3: ノード文字数制限をSession3からの漏れとして復元・記録
- 作業4: 孤立ノードの扱いを「浮遊する星＝外部参照と同一仕様」として確定
- 作業5: genesis.mdの複数起源・矛盾を多元宇宙として歓迎する方針を確定
- 作業6: インスタンスポリシー方針を確定（整合性・雰囲気はインスタンスごとに自由）
- 作業7: 翻訳UIの初期仕様を確定（外部リンクボタン）・将来像を記録
- 作業8: 銀河マップの多言語方針を確定（原文言語不問で並列表示）
- 作業9: オンボーディングでの言語選択UIを記録
- 作業10: 初期フェイズのGitHub運用構造を確定（個人リポジトリハブ＋fork）
- 作業11: 参入障壁の段階的解消ロードマップを記録
- 作業12: インスタンス運営者の日常業務と軽減策を整理
- 作業13: relations.jsonの管理者問題を解決（各fork所有者が自分のものを管理）
- 作業14: 著作権方針を整理（PD原文そのまま＋翻訳リンク）
- 作業15: 民話選定用軽量メモを別途出力（別チャットタスク）
- COMPRESSED の更新点: #BRIDGE_TO / #NODE_SPEC / #ISOLATED_NODE / #GENESIS / #INSTANCE_POLICY / #TRANSLATION_UI / #GITHUB_STRUCTURE / #ONBOARDING / #INITIAL_LIMITATIONS を新設
- SAMPLES の更新点: 翻訳UIサンプル / relations.jsonサンプル（孤立・外部参照）/ オンボーディング文言 を追加


# RELAY_DOCUMENT_COMPRESSED

#PROJECT
[SPEC:NAME=infinite-epic(仮)]
[SPEC:VERSION=1.0]
[WHY:プロジェクト識別のため]

#PHILOSOPHY
[SPEC:ForkEquivalence=ON]
[SPEC:StructuralIntegrity=MAX]
[SPEC:WHYRetention=MANDATORY]
[SPEC:AI_Relay=CORE]
[SPEC:ContradictionWelcome=ON]
[SPEC:MultiVerse=ON]
[WHY:中核哲学保持のため。矛盾はエラーではなく多元宇宙として歓迎する]

#RELAY_PACKET
[SPEC:Layers=SESSION_LOG;COMPRESSED;SAMPLES]
[SPEC:SingleCodeblock=TRUE]
[SPEC:NoExternalContext=TRUE]
[SPEC:NextAI_MustFollow=TRUE]
[WHY:AIリレー形式固定のため]

#TECHNICAL_ARCHITECTURE
[SPEC:PHYSICAL_FILES=TIMESTAMP-SHA-title.md]
[SPEC:LOGICAL_LINKS=meta/relations.json]
[SPEC:NodeID=TIMESTAMP-contenthash8-12chars-title.md]
[WHY:2層管理による物理・論理分離のため]

#NODE_SPEC
[SPEC:CharLimit_ja=1200文字]
[SPEC:CharLimit_other=日本語1200字換算(ローカライズ担当者またはAI自動算出)]
[SPEC:SizeMin=制限なし(haiku断片も可)]
[SPEC:SizeMax=制限なし(長編も可)]
[SPEC:Direction=前方向・後方向ともに許容]
[WHY:Session3漏れを復元。粒度自由がフォーク多様性を生む]

#RELATIONS_JSON
[SPEC:File=meta/relations.json]
[SPEC:Format=SingleJSON]
[SPEC:AllowedKeys=precedes;follows;characters;location;bridge_to;tags;cycle_annotation;created_by;degree;heat;visibility;status]
[SPEC:SelfLoop=permit(mini-loop-story)]
[SPEC:CycleDetect=annotation("ループを検知しました。この分岐は循環しています。")]
[SPEC:OrphanCheck=ON]
[SPEC:Degree=構造的接続数(別管理)]
[SPEC:Heat=読者活動指標(別管理)]
[SPEC:NodePersistent=ON(削除禁止・視認性制御のみ)]
[SPEC:Visibility=adjustable(author_request)]
[WHY:構造守護と分岐等価を両立するため]

#BRIDGE_TO
[SPEC:Type=bridge_to]
[SPEC:Directed_false=A↔B(双方向ワームホール)]
[SPEC:Directed_true=A→B(一方通行ワームホール)]
[SPEC:Default=未定(後続セッションで決定)]
[WHY:異なる世界線の接続に方向性の選択肢を持たせるため]

#ISOLATED_NODE
[SPEC:Definition=どのノードからもリンクされていないノード]
[SPEC:Treatment=外部参照と同一仕様(status="floating")]
[SPEC:VisibleOnMap=TRUE]
[SPEC:ConnectionForced=FALSE]
[SPEC:Unification=孤立ノード・外部プロジェクトノード・未接続ノードを同一概念で扱う]
[WHY:「まだ知られていない外部宇宙への入口」として意味を持たせるため]

#CROSS_REPO
[SPEC:ExternalNodeFormat=repo_url::node_id]
[SPEC:CrossProjectLink=permit]
[SPEC:FormatStandard=ONF(Open Narrative Format)候補]
[WHY:Session3確定。類似プロジェクトとの接続を歓迎するため]

#GENESIS
[SPEC:MultipleGenesis=ON]
[SPEC:PerInstance=TRUE]
[SPEC:Contradiction=welcome(多元宇宙)]
[SPEC:SingleOrigin=FALSE]
[WHY:全分岐等価の哲学をgenesisレベルまで拡張。矛盾は多元宇宙として歓迎]

#INSTANCE_POLICY
[SPEC:NarrativeConsistency=インスタンス運営者が自由に決定]
[SPEC:CommunityAtmosphere=インスタンスごとに自由]
[SPEC:ConsistencyExample="このインスタンスでは整合性を重視します／しません"]
[SPEC:CentralControl=OFF]
[SPEC:NoPermissionNeeded=ON(READMEに明記)]
[WHY:中央集権的管理はプロジェクト思想と矛盾するため。インスタンス多様性を保持]

#TRANSLATION_UI
[SPEC:InitialPhase=外部リンクボタン(DeepL;Google翻訳;Microsoft Translator)]
[SPEC:Method=DeepLやGoogle翻訳のURLに原文を渡す]
[SPEC:FuturePhase=ページ内翻訳API(未来実装リスト)]
[SPEC:Copyright=PD原文そのまま配置・翻訳行為はユーザー側]
[WHY:翻訳者の権利を侵害しない最もクリーンな方式。初期コストほぼゼロ]

#GALAXY_MAP_LANGUAGE
[SPEC:DisplayPolicy=原文言語不問で並列表示]
[SPEC:LanguageFilter=インスタンスポリシーで変更可]
[SPEC:Condition=技術が許せば]
[WHY:言語の壁を意識させない多元宇宙的体験のため]

#ONBOARDING
[SPEC:LanguageSelection=初回アクセス時に言語を選択]
[SPEC:Options=ja;en;zh;es等]
[SPEC:Persistence=選択言語を記憶]
[SPEC:Changeable=TRUE]
[WHY:読者体験の言語最適化のため]

#GITHUB_STRUCTURE
[SPEC:InitialHub=sukoyaka-dopenessの個人リポジトリ]
[SPEC:ParticipantAction=forkして自リポジトリで執筆]
[SPEC:RelationsJson_Owner=各fork所有者が自分のものを管理]
[SPEC:NoConflict=各forkは独立して完結するため競合なし]
[WHY:初期フェイズの最もシンプルな構造]

#INITIAL_LIMITATIONS
[SPEC:GitHubAccount=参加に必要(初期フェイズの限界として明記)]
[SPEC:SharedAccount=GitHubTOS違反のため不可]
[SPEC:Mitigation=将来のWebUI+GitHub API対応で解消予定]
[WHY:参入障壁として認識・記録。段階的解消ロードマップへ接続]

#GROWTH_ROADMAP
[SPEC:Phase1=個人リポジトリA(今すぐ開始可能)]
[SPEC:Phase2=Organization+簡易WebUI(障壁を下げる)]
[SPEC:Phase3=OSSインスタンス化(誰でも立てられる)]
[SPEC:Phase4=DAO(後期フェイズ保留)]
[WHY:段階的な中央集権からの脱却。思想とインフラの整合性を保つ]

#COPYRIGHT
[SPEC:PDSeed=アリス;シェイクスピア;グリム等のPD原文]
[SPEC:NodeType_A=PD原文そのまま]
[SPEC:NodeType_B=PD素材をもとにAIが新規執筆]
[SPEC:NodeType_C=PD素材のエッセンスをAIが翻案(結末違い・視点違い等)]
[SPEC:InitialNodeGoal=フォークの多様性を例示するセットを初期フェイズに用意]
[WHY:著作権リスクを回避しつつフォーク例示の多様性を確保するため]

#UI_NAVIGATION
[SPEC:5Buttons=⬅️前の章/➡️後の章/🌿この章からフォーク/⏪この章の前を書く/⏭️この章の後を書く]
[SPEC:ForkPrompt="このノードのフォークを作る？"]
[SPEC:Wormhole=bridge_toによる世界線ジャンプ]
[WHY:読者と執筆者の両方の行動を1画面でサポートするため]

#DAILY_OPS
[SPEC:AutoDetect=fork検知はGitHub APIで可能]
[SPEC:ManualJudge=繋げる判断はAI委譲可能(将来)]
[SPEC:NoPermissionCulture=「許可不要・forkして自由に書く」をREADMEに明記]
[SPEC:CopyrightScope=参加者の自リポジトリの問題・あなたのリポジトリには入ってこない]
[WHY:運営負荷を最小化するための設計方針]


# RELAY_DOCUMENT_SAMPLES

## 翻訳UIボタン例（ノード閲覧画面）
🌐 この章を翻訳して読む
[DeepL] [Google翻訳] [Microsoft Translator]

## オンボーディング文言例
「どの言語で読みますか？」
[日本語] [English] [中文] [Español] ...
※いつでも変更できます

## relations.json：孤立ノード（浮遊する星）例
{
  "node_id": "2026-0303T120000Z-a1b2c3d4-lonely",
  "precedes": [],
  "follows": [],
  "bridge_to": [],
  "tags": [],
  "status": "floating",
  "visible_on_map": true,
  "cycle_annotation": null,
  "created_by": "human"
}

## relations.json：外部プロジェクトへのクロスリンク例
{
  "from": "2026-0303T120000Z-a1b2c3d4-node",
  "to": "https://github.com/other/project::node-88",
  "type": "external_reference",
  "directed": false
}

## relations.json：bridge_to 方向性例
{
  "node_id": "2026-0303T120000Z-b2c3d4e5-wormhole",
  "bridge_to": [
    {
      "target": "2026-0303T130000Z-c3d4e5f6-other",
      "directed": false
    },
    {
      "target": "2026-0303T140000Z-d4e5f6g7-oneway",
      "directed": true
    }
  ]
}

## genesis.md 複数起源の思想メモ
インスタンスAのgenesis：「世界は海から生まれた」
インスタンスBのgenesis：「世界は火から生まれた」
→ 両者のノードがbridge_toで繋がっても矛盾ではなく多元宇宙。歓迎。

## インスタンスポリシー宣言文例
「このインスタンスでは整合性を重視します」
「このインスタンスでは物語の矛盾・逸脱を歓迎します」

## README冒頭：「許可不要」文化の明示例
このリポジトリをフォークするのに許可は不要です。
あなたが刻んだ一行は、どこに置いても等価です。
「正しい続き」は存在しません。フォークして歴史を紡げ。

## 初期ノード構成案（著作権フリー素材使用）
genesis.md    → PD原文そのまま（例：グリム童話の冒頭断片）
fork-A.md     → 結末が違う版（AIがPD素材をもとに翻案）
fork-B.md     → 視点・語り手が違う版（狼側から語られる赤ずきん等）
fork-C.md     → 時代・舞台が違う版（現代都市への翻案等）

## 未来実装リスト（将来フェイズで実装）
- ページ内翻訳API（ノード本文がその場で書き換わる）
- GitHub APIを叩くWebUI（GitHubアカウント不要で参加可能）
- relations.jsonの自動バリデーション（GitHub Actions）
- 銀河マップ上での言語フィルタリング（インスタンスポリシー）
- 繋げる判断のAI自動化
