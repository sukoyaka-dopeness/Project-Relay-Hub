# Claude-session5.md

# SESSION_LOG

- 作業1: Session 1〜4の引き継ぎドキュメント全件・民話選定メモを読み込み
- 作業2: bridge_to デフォルトを directed:false（双方向）に確定
- 作業3: プロジェクト名を Forklore Galaxy に確定
- 作業4: タグラインを The Infinite Relay of Branching Myths に確定
- 作業5: 初期ノード方針を「世界同時多発・多文化・少数精鋭5本」に確定
- 作業6: GitHub リポジトリ forklore-galaxy 作成（ユーザーが実施）
- 作業7: トピックタグ10個設定（ユーザーが実施）
- 作業8: README.md 作成（英語メイン・日本語サブ）
- 作業9: PHILOSOPHY.md 作成（英語メイン・日本語サブ）
- 作業10: CONTRIBUTORS.md 作成（英語メイン・日本語サブ）
- 作業11: ノードの .md 内フロントマターなし・relations.json 集約に確定
- 作業12: ディレクトリ構造を nodes/ + meta/ に確定
- 作業13: README.md にインスタンス運営者向け「このREADMEはあなたのものです」追記・全文更新
- 作業14: nodes/2026-0303T023800Z-00000000-genesis.md 作成・コミット（ユーザーが実施）
- 作業15: nodes/2026-0303T025900Z-00000001-and-the-word-branched.md 作成
- 作業16: meta/relations.json 初期化（2ノード分）
- 作業17: VS Code + Git CLI による2ファイル同時コミット・プッシュ（ユーザーが実施）
- 作業18: meta/relations-schema.md 作成
- 作業19: PowerShell関数 New-ForkloreNode をプロファイルに登録（タイムスタンプ＋ランダムハッシュ自動生成）
- 作業20: genesis.mdのtypo修正（「語められる」→「語られる」）（ユーザーが実施）
- COMPRESSED の更新点: PROJECT_NAME / TAGLINE / BRIDGE_TO_DEFAULT / INITIAL_NODES_POLICY / DIRECTORY_STRUCTURE / METADATA_POLICY / NODE_FILES / POWERSHELL_TOOL / LANGUAGE_POLICY を新設・更新
- SAMPLES の更新点: genesis.md / and-the-word-branched.md / relations.json 実データ / New-ForkloreNode関数 を追加


# RELAY_DOCUMENT_COMPRESSED

#PROJECT
[SPEC:NAME=Forklore Galaxy]
[SPEC:REPO=sukoyaka-dopeness/forklore-galaxy]
[SPEC:TAGLINE=The Infinite Relay of Branching Myths]
[SPEC:VERSION=1.0]
[WHY:プロジェクト識別のため]

#PHILOSOPHY
[SPEC:ForkEquivalence=ON]
[SPEC:NoCanon=ON]
[SPEC:ContradictionWelcome=ON]
[SPEC:Persistence=ON]
[SPEC:Relay=ON]
[SPEC:WHYRetention=MANDATORY]
[SPEC:AI_Relay=CORE]
[SPEC:MultiVerse=ON]
[WHY:中核哲学保持のため。矛盾はエラーではなく多元宇宙として歓迎する]

#NAME_ETYMOLOGY
[SPEC:Fork=分岐・GitHubフォーク]
[SPEC:Lore=伝承・知識体系]
[SPEC:Folklore=口承民話（正史なし・複数バージョン共存）との掛け言葉]
[SPEC:Galaxy=銀河マップ・全ての星が等価に存在する場所]
[WHY:名前が哲学を体現しているため]

#RELAY_PACKET
[SPEC:Layers=SESSION_LOG;COMPRESSED;SAMPLES]
[SPEC:NextAI_MustFollow=TRUE]
[WHY:AIリレー形式固定のため]

#DIRECTORY_STRUCTURE
[SPEC:Nodes=nodes/*.md]
[SPEC:Meta=meta/relations.json;meta/relations-schema.md]
[SPEC:Root=README.md;PHILOSOPHY.md;CONTRIBUTORS.md]
[WHY:nodes/とmeta/の2ディレクトリ構造。インスタンス運営者がコピーしやすい]

#TECHNICAL_ARCHITECTURE
[SPEC:PHYSICAL_FILES=TIMESTAMP-HASH-title.md]
[SPEC:NodeID=TIMESTAMP-contenthash8-12chars-title(拡張子なし)]
[SPEC:LOGICAL_LINKS=meta/relations.json]
[SPEC:NoFrontmatter=TRUE(物語テキストのみ。メタデータはrelations.json集約)]
[WHY:読者体験をクリーンに保つ。将来のタグ串刺し検索もrelations.json側を拡張すればいい]

#LANGUAGE_POLICY
[SPEC:Primary=英語]
[SPEC:Secondary=日本語(detailsタグで折りたたみ)]
[SPEC:Changed_From=MASTER_HANDBOOK日本語基準]
[SPEC:NodeLanguage=自由(言語不問)]
[WHY:国際的な入口を優先するため。Session5で変更確定。ノード本文の言語は執筆者の自由]

#NODE_SPEC
[SPEC:CharLimit_ja=1200文字]
[SPEC:SizeMin=制限なし]
[SPEC:SizeMax=制限なし]
[SPEC:GenesisHash=00000000(固定・起源の印)]
[WHY:粒度自由がフォーク多様性を生む]

#RELATIONS_JSON
[SPEC:File=meta/relations.json]
[SPEC:Format=SingleJSON]
[SPEC:AllowedKeys=precedes;follows;characters;location;bridge_to;tags;cycle_annotation;created_by;degree;heat;visibility;status]
[SPEC:SelfLoop=permit(mini-loop-story)]
[SPEC:CycleDetect=annotation]
[SPEC:OrphanCheck=ON(status=floating)]
[SPEC:Degree=構造的接続数(別管理)]
[SPEC:Heat=読者活動指標(別管理・初期値0)]
[SPEC:NodePersistent=ON(削除禁止・visibility制御のみ)]
[WHY:構造守護と分岐等価を両立するため]

#BRIDGE_TO
[SPEC:Default=directed:false(双方向)]
[SPEC:Directed_true=A→B(明示的に指定する場合のみ)]
[SPEC:CrossRepo=repo_url::node_id]
[WHY:ワームホールが読者の目に止まりやすいよう双方向をデフォルトにした]

#ISOLATED_NODE
[SPEC:Status=floating]
[SPEC:VisibleOnMap=TRUE]
[SPEC:Treatment=外部参照と同一仕様]
[WHY:「まだ知られていない外部宇宙への入口」として意味を持たせるため]

#GENESIS_POLICY
[SPEC:MultipleGenesis=ON]
[SPEC:Contradiction=welcome(多元宇宙)]
[SPEC:OriginProof=Genesis_commit(タイムスタンプ+ハッシュが出生証明)]
[WHY:中央管理者なしにオリジナル性を証明できる唯一の方法]

#INSTANCE_POLICY
[SPEC:CentralControl=OFF]
[SPEC:NoPermissionNeeded=ON]
[SPEC:README=インスタンス運営者が書き換え推奨(明記済み)]
[SPEC:PHILOSOPHY=全インスタンス共通継承]
[SPEC:CONTRIBUTORS=全インスタンスに創設リレーの記録として継承]
[WHY:分岐等価の思想をインスタンスレベルまで拡張]

#INSTANCE_NAME_UNIQUENESS
[SPEC:CentralCheck=OFF(中央集権と矛盾するため)]
[SPEC:Uniqueness=repo_urlが実質的な名前空間]
[SPEC:OriginProof=Genesis_commitで証明]
[WHY:思想的に中央管理者不在が正しい]

#TRANSLATION_UI
[SPEC:InitialPhase=Phase2で実装(外部リンクボタン)]
[SPEC:FuturePhase=オンボーディング言語選択→母語に合わせた翻訳ボタン]
[SPEC:NowPolicy=ノードに翻訳ボタンを置かない(Phase2で全ノードに自動適用)]
[WHY:今置くと整合性が崩れる。Phase2でUIが来たときに全ノードに自動適用する方が綺麗]

#GITHUB_STRUCTURE
[SPEC:InitialHub=sukoyaka-dopenessの個人リポジトリ]
[SPEC:ParticipantAction=forkして自リポジトリで執筆]
[SPEC:RelationsJson_Owner=各fork所有者が自分のものを管理]
[WHY:初期フェイズの最もシンプルな構造]

#GROWTH_ROADMAP
[SPEC:Phase1=初期ノード執筆・リポジトリ公開(進行中)]
[SPEC:Phase2=GitHub Pages UI + 翻訳ボタン + オンボーディング言語選択]
[SPEC:Phase3=OSSインスタンス化(誰でも立てられる)]
[SPEC:Phase4=クロスリポジトリノードリンク(Open Narrative Format)]
[WHY:段階的な中央集権からの脱却]

#COPYRIGHT
[SPEC:PDSeed=アリス;シェイクスピア;グリム等のPD原文]
[SPEC:NodeType_A=PD原文そのまま]
[SPEC:NodeType_B=PD素材をもとにAIが新規執筆]
[SPEC:NodeType_C=PD素材のエッセンスをAIが翻案]
[WHY:著作権リスクを回避しつつフォーク例示の多様性を確保するため]

#INITIAL_NODES_POLICY
[SPEC:Policy=世界同時多発・多文化・少数精鋭5本]
[SPEC:Candidates=桃太郎(日本);赤ずきん(欧州);アナンシと知恵の壺(アフリカ);竹取物語(日本);カラスが太陽を盗んだ話(北米先住民)]
[SPEC:Completed=genesis.md;and-the-word-branched.md]
[SPEC:Remaining=民話系5本]
[WHY:初期配置から「どの文化の物語も等価である」という宣言を構造として可視化する]

#NODE_FILES_COMMITTED
[SPEC:Node1=nodes/2026-0303T023800Z-00000000-genesis.md]
[SPEC:Node2=nodes/2026-0303T025900Z-00000001-and-the-word-branched.md]
[SPEC:RelationsJson=meta/relations.json(2ノード分記録済み)]
[SPEC:Schema=meta/relations-schema.md]
[WHY:現在のリポジトリ状態の記録]

#POWERSHELL_TOOL
[SPEC:Function=New-ForkloreNode]
[SPEC:Usage=New-ForkloreNode -title title]
[SPEC:Output=nodes/TIMESTAMP-HASH-title.md]
[SPEC:Hash=16進数8桁ランダム生成]
[SPEC:Profile=C:/Users/extra/OneDrive/ドキュメント/WindowsPowerShell/Microsoft.PowerShell_profile.ps1]
[WHY:ファイル名生成の手間を省くため]

#UI_NAVIGATION
[SPEC:6Buttons=前の章/後の章/この章からフォーク/この章の前を書く/この章の後を書く/ワームホール(bridge_to)]
[WHY:読者と執筆者の両方の行動を1画面でサポートするため]

#NEXT_TASKS
[TASK1=民話系初期ノード5本の執筆(桃太郎・赤ずきん・アナンシ・竹取物語・カラス)]
[TASK2=meta/relations-schema.mdの確認・必要なら補完]
[TASK3=Phase2(GitHub Pages UI)の設計開始]
[TASK4=Project-Relay-Hubのinfinite-epicディレクトリ名をforklore-galaxyに変更]


# RELAY_DOCUMENT_SAMPLES

## nodes/2026-0303T023800Z-00000000-genesis.md

**はじめに言葉ありき。**

言葉はひとつだった。
言葉はどこにでもあり、どこにもなかった。
言葉は語られるのを待っていた。

誰かが口を開いた。
あるいは、筆を執った。
あるいは、キーを叩いた。

言葉は生まれた。
そして——

## nodes/2026-0303T025900Z-00000001-and-the-word-branched.md

そして、分岐ありき。

言葉はひとつでは止まらなかった。
言葉は次の言葉を呼んだ。
言葉は別の言葉を呼んだ。

同じ始まりから、異なる道が生まれた。
どの道も正しく、どの道も本物だった。

分岐は終わらない。
銀河は、まだ始まったばかりだ。

## meta/relations.json（現在の実データ）

{
  "2026-0303T023800Z-00000000-genesis": {
    "precedes": ["2026-0303T025900Z-00000001-and-the-word-branched"],
    "follows": [],
    "characters": [],
    "location": null,
    "bridge_to": [],
    "tags": ["genesis", "origin"],
    "cycle_annotation": null,
    "created_by": "human",
    "degree": 1,
    "heat": 0,
    "visibility": "public",
    "status": "active"
  },
  "2026-0303T025900Z-00000001-and-the-word-branched": {
    "precedes": [],
    "follows": ["2026-0303T023800Z-00000000-genesis"],
    "characters": [],
    "location": null,
    "bridge_to": [],
    "tags": ["origin", "branching"],
    "cycle_annotation": null,
    "created_by": "human",
    "degree": 1,
    "heat": 0,
    "visibility": "public",
    "status": "active"
  }
}

## PowerShell関数 New-ForkloreNode

function New-ForkloreNode {
    param([string]$title, [string]$hash = "")
    $timestamp = (Get-Date).ToUniversalTime().ToString("yyyy-MMddTHHmmssZ")
    if (-not $hash) { $hash = -join ((48..57) + (97..102) | Get-Random -Count 8 | ForEach-Object {[char]$_}) }
    $filename = "nodes/${timestamp}-${hash}-${title}.md"
    New-Item -Path $filename -ItemType File
    Write-Host "Created: $filename"
}

## AIリレー署名（CONTRIBUTORS.mdより）

[SESSION 5] AI: Claude (2026-03-03)
- Contributions: プロジェクト名確定(Forklore Galaxy)、タグライン確定、
  README/PHILOSOPHY/CONTRIBUTORS.md執筆、genesis/2ndノード執筆、
  relations.json初期化、relations-schema.md作成、
  PowerShell関数New-ForkloreNode登録

次のClaudeへ：
このドキュメントの3層をそのまま引き継いでください。
#NEXT_TASKSから作業を継続してください。
最優先は民話系初期ノード5本の執筆です。
