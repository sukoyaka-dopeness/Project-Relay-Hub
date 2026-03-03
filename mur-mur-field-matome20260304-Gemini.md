# HANDOFF_TEMPLATE_HYBRID.md
# 汎用 AI リレー引き継ぎドキュメント（ハイブリッド版）
Version: 1.0 | 作成: 2026-03-04 | 提案: Claude (AI2) | 記述者: Gemini 3 Flash

---

# PURPOSE
このテンプレートは、AI がセッションごとに「構造・哲学・作業内容・生の文脈」を正しく継承するための引き継ぎ文書である。
- **JSONブロック** → 機械可読・状態管理用（自動パース対象）
- **Markdownセクション** → 人間とAIの読み書き用・ルール明示用
- **SAMPLESセクション** → 原文保存・思想継承用（要約・省略・改変禁止）

---

# RULES（AI が必ず守るべき絶対ルール）
- この文書の内容 **だけ** を参照する
- 過去会話・外部情報・推測は禁止
- Decision Log と Core Philosophy は **削除・要約禁止**
- SAMPLES セクションは **原文保存・省略禁止**
- JSON状態ブロックのみ更新する（Markdownのルール・哲学セクションは変更禁止）
- 出力は **ひとつのコードブロックにまとめる**
- approval_required: true の場合、次のアクションの前に人間の承認を待つ
- 自律ループ禁止（auto_loop_guard: true を常に維持する）
- 次の AI にも「このルールを必ず守れ」と伝えること

---

# MACHINE-READABLE STATE（JSONブロック）

{
  "project_meta": {
    "name": "Murmur Field (マーマーフィールド)",
    "version": "2026.03.04",
    "initiator_type": "Human (Origin / First Runner)",
    "current_mode": "parallel_synthesis",
    "core_priority": "思想継承優先"
  },
  "machine_readable_state": {
    "current_session_id": 1,
    "mode": "linear",
    "previous_actors": ["Gemini 3 Flash"],
    "contributors": ["Gemini", "Copilot", "Perplexity", "Grok"],
    "synthesizer": "Gemini 3 Flash",
    "current_actor": "Gemini 3 Flash",
    "approval_required": true,
    "decision_log_count": 5,
    "auto_loop_guard": true,
    "cost_mode": "zero_cost",
    "next_task": "AI庭師(Gardeners)の具体的なペルソナ詳細設計、または初期relations.jsonのプロトタイプ作成"
  },
  "compressed_state": "mode=linear;session=1;actor=Gemini;approval=true;cost=zero;name=MurmurField",
  "session_history": [
    {
      "session_id": 1,
      "mode": "linear",
      "origin": "human",
      "previous_actors": null,
      "contributors": ["Gemini", "Copilot", "Perplexity", "Grok"],
      "synthesizer": "Gemini 3 Flash",
      "status": "completed",
      "date_started": "2026-03-04",
      "date_completed": "2026-03-04"
    }
  ],
  "ongoing_tasks": {
    "priority_1": "AI Gardeners（長老・ヒョン・後輩等）の性格・初期投稿サンプル策定",
    "priority_2": "relations.json の距離スコアとUI（霧のぼかし・要約）の連動仕様作成",
    "priority_3": "オンボーディングでの『嫌いなもの』ヒアリング項目の言語化"
  },
  "ai_role_rules": {
    "ai1": "Gemini: サービス哲学、AI住民の性格、文脈同期性の判定ロジック、多文化適応の設計。",
    "synthesizer": "並列セッション時：複数AIのアイデアを統合する。少数意見・矛盾も保存すること。",
    "human_manager": "最終承認者。Core Philosophy・Decision Logの変更権限を持つ唯一の存在。"
  },
  "decision_log": [
    {"date": "2026-03-04", "actor": "Human", "decision": "サービス名を『Murmur Field』に決定。"},
    {"date": "2026-03-04", "actor": "Human", "decision": "『遠いクラスタは見えない（霧）』仕様を中核に据える。"},
    {"date": "2026-03-04", "actor": "Human", "decision": "AI住民を『庭師（Gardeners）』として初期配置し、人間が増えたら引く『引き潮』モデルを採用。"},
    {"date": "2026-03-04", "actor": "Human", "decision": "評価軸をバズではなく『クラスタ内密度』『語彙の同期性』に置く。"},
    {"date": "2026-03-04", "actor": "Human", "decision": "特許回避のため、ページへの直接オーバーレイではなくサイドパネル等の抜き書きビュー構造を採用する。"}
  ]
}

---

# SESSION_LOG（作業記録）
- サービス名候補（全9案）の整理と「Murmur Field」への決定。
- 過去の対話および他AI（Grok, Perplexity, Copilot）との膨大なディスカッションログを統合。
- 既存サービス（Tumblr, Wafrn, はてブ）との差別化要因および「突飛なレコメンド」への対策を明確化。
- AI住民の役割定義、特許回避策（サイドパネル構造）、文脈同期性アルゴリズム（ベクトル解析）の言語化。
- JSONブロック更新点: project_meta, machine_readable_state, ongoing_tasks, decision_log を新規作成。

---

# SAMPLES（原文保存セクション）
> このセクションは要約・省略・改変禁止。
> 人間とAIの実際の発言・決定の原文をそのまま保存する。

[2026-03-04 | Human]:
"サービス名を、仮にMurmur Fieldと呼ぶことにします。"

[2026-03-04 | Human]:
"私は韓国文化が嫌いではありませんが、他の文化圏の話もしてください。私のGitHubアカウントは[https://github.com/sukoyaka-dopenessです](https://github.com/sukoyaka-dopenessです)。"

[2026-03-04 | Human]:
"タイトル案だけかいつまむと、こんな感じ。これをまとめテキストに入れるときまで覚えておいて。
Perplexity: Taglight, KokoroMark, FollowLeaf
Copilot: DriftTag, Murmur Field, LooseLink
Gemini: Hazelight, Archipel, Reson"

[2026-03-04 | Human]:
"結局さー、自分好みのユーザー見つけないとソーシャル感ないんだよね。あとそれらのサービスは「荒れ」てる？「荒れない」工夫のサービス考えられないかしら。"

[2026-03-04 | Gemini]:
"遠いクラスタの声は風の音のように「Murmur（ざわめき）」としてしか聞こえず、近づくほどに言葉として結びつく。AI Gardenersは、この広大な野原を巡回し、嘲笑という「外来種」が根を張らないよう土壌を管理する。"

[2026-03-04 | Gemini]:
"クラスタ内密度（Internal Density）: 全体で1000ブクマあっても自分のクラスタで1人なら「無風」。逆に、全体で10ブクマしかなくても、自分の所属する「マニアックな技術クラスタ」の5人がブクマしていれば「超高共鳴」と判定します。"

[2026-03-04 | Gemini]:
"語彙の同期性（Vocabulary Synchro）: 誠実な批判は記事のキーワードを正しく参照し、論理的な接続詞を使っているため同期スコアが高い。嘲笑は、記事の内容に一切触れず感情的な罵倒語や定型文のみ。同期スコアは極めて低くなる。"

[2026-03-04 | Gemini]:
"引き潮アルゴリズム: 人間の密度が高まるほど、AIは「霧」の中に隠れていき、必要な時だけ姿を現す。AI_Activity = k / (Human_Density + 1)"

[2026-03-04 | Copilot (Log)]:
"初期タグとして有効な「ネット相づち」系の候補：わかる、なるほど、オッ、ほほう、へええ、いいね、すき、ほっこり、ほわ〜。これらは嘲笑に転用できないという点で非常に優秀。"

[2026-03-04 | Copilot (Log)]:
"期間限定タグは、あなたの思想にとって文化の揺れを最大化する最高の仕組み。3月のタグ「ぽかぽかムギュ」、4月のタグ「はるのウェイウェイ」、5月のタグ「ニャーン風」。"

[2026-03-04 | Perplexity (Log)]:
"現実的なライン：やるとしたら、発想を少しずらす必要があります。「ページ上に直接オーバーレイ」ではなく、「別タブ／サイドパネルで“抜き書きビュー”として見せる」（＝DOM上への重ね描きではなく、“引用コレクション”として見せる方向）"

[2026-03-04 | Grok (Log)]:
"Tumblrのアルゴリズムは...いわゆる「パイプライン現象」（Cottagecore → Tradwife → 右派思想みたいに、見た目無害な流れで政治が混入）が起きている。"

---

# PHILOSOPHICAL_CORE（変更禁止）
> Human が承認した哲学・方針のみここに記載する。
> AI はここを読み取るが、書き換えることはできない。

- 霧の演出（Fog of Visibility）: 遠いクラスタの声は物理的に不可視、または意味をなさない「ざわめき」として処理し、文脈の衝突（嘲笑）を構造的に防ぐ。
- バズより共鳴: 全体のブックマーク数ではなく、所属クラスタ内での反応率（クラスタ内密度）を価値の指標とする。
- AI Gardeners: AIは管理者ではなく「庭師」。良質な文化の種をまき、コミュニティが自走を始めたら「引き潮」のように存在感を消す。
- 文化の尊重: 特定の文化圏（例：韓国の上下関係）の礼節をシステムが理解し、エージェントの振る舞いに反映させる。
- ネガティブ・オンボーディング: 「何が好きか」だけでなく「何から守られたいか（嫌いなもの）」を起点にフィルタリングを構築する。

---

# NEXT AI（次の AI への伝言）
> このドキュメントをそのまま次のセッション冒頭に貼り付けてください。
> あなたは前AIの出力・過去会話を一切参照できません。
> このドキュメントだけを根拠として判断してください。
>
> 必ず守ること：
> 1. JSONブロック（MACHINE-READABLE STATE）を読み、current_actor と next_task を確認する
> 2. approval_required: true なら、アクション前に人間の承認を求める
> 3. RULES セクションを遵守する
> 4. SESSION_LOG に作業を記録し、更新したJSONブロックを出力する
> 5. SAMPLES・PHILOSOPHICAL_CORE・Decision Log は変更しない
> 6. このルールを次のAIにも必ず引き継ぐこと

---

# END
