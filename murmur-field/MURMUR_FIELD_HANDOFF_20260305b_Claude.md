# MURMUR_FIELD_HANDOFF_20260305_Claude.md

Version: 1.0 | Created: 2026-03-05 | Author: Claude (Project-Relay-Hub AI relay)  
バージョン: 1.0 | 作成: 2026-03-05 | 記述者: Claude（Project-Relay-Hub AIリレー）

---

## 0. Metadata / メタデータ

- **Project Name / プロジェクト名:** murmur-field
- **Session:** 4
- **Previous Handoff / 前回引き継ぎ:** MURMUR_FIELD_HANDOFF_20260305_Gemini
- **Status / ステータス:** MVP Specification — Design Refinement / MVP仕様定義——デザイン精緻化

---

## 1. Machine-Readable State / 機械可読ステート

```json
{
  "project_meta": {
    "name": "Murmur Field (マーマーフィールド)",
    "version": "2026.03.05-claude",
    "current_mode": "linear",
    "core_priority": "思想継承優先"
  },
  "machine_readable_state": {
    "current_session_id": 4,
    "previous_actors": ["Gemini", "Copilot", "Perplexity", "Grok", "Claude", "Gemini"],
    "current_actor": "next AI",
    "approval_required": true,
    "auto_loop_guard": true,
    "cost_mode": "zero_cost",
    "next_task": "未決事項の優先順位を人間と確認し、残作業を進める"
  },
  "compressed_state": "mode=linear;session=4;actor=next;approval=true;cost=zero;name=MurmurField"
}
```

---

## 2. SESSION_LOG — Session 4 Decisions / 決定事項

| Date / 日付 | Decision / 決定内容 |
|---|---|
| 2026-03-05 | TAG_SUGGESTIONSをコンテンツ系（Q1・Q2用）と感情系（ブックマーク時専用）に分類した |
| 2026-03-05 | 「ささやき」はサービス機能名と同音のためコンテンツ系タグから除外 |
| 2026-03-05 | 「林業」「水産業」は専門性が高いため少なくともオンボーディングから除外。将来のユーザー生成タグとして再検討可能 |
| 2026-03-05 | 「農業」単独のバランス問題を解決するため「料理」と統合し「食と農 / Food & Farming」カテゴリを新設 |
| 2026-03-05 | 「社会と時事 / Society & Current Events」カテゴリを新設（政治 / 経済 / 社会 / 時事 / 事件・事故） |
| 2026-03-05 | 「自然と宇宙」は時間帯による差が少ないカテゴリとして全時間帯★★で統一 |
| 2026-03-05 | 社会・時事カテゴリは20時以降に意図的に遠ざける（野原が休息を守る） |
| 2026-03-05 | 時間帯別タグ分類はアルゴリズム内部テーブルとして持つ。UIには語彙を出さずビジュアル・振動で表現 |
| 2026-03-05 | 「タグはタグのまま、アルゴリズムが時間帯×タグの相性テーブルを持つ」方式に決定 |
| 2026-03-05 | リズム検知信号：アクセス時刻分布・セッション長・デバイス種別・タグ時間帯別傾向を採用。タイムゾーンは除外 |
| 2026-03-05 | 「学習が精緻化するほど、ノイズ比率を一定に保つ」ルールをAmbient Rhythmモデルに追記 |
| 2026-03-05 | カードの揺れ：常時ではなくランダムな風がときおり揺らす程度（MVP実装可能）。石カードは揺れを持たない完全静止 |
| 2026-03-05 | スマートフォンを振るとフィールドがかき混ぜられる。振る強さで混ぜ具合が変わる |
| 2026-03-05 | コメント入力フォーカス中はshakeジェスチャーを無効化する（実装フェーズで確認が必要） |
| 2026-03-05 | 「石を置いた」カードは流れの中で静止する（リスト上部固定ではなく、フィールド内の静止物として存在） |
| 2026-03-05 | 「石をはずす」操作は軽くできる。ただし誤操作防止のため長押し後にボタン表示、シングルタップで確定 |
| 2026-03-05 | 「枯れ草」カードは選択制：そのまま残す or「忘れる」で消去。デフォルトは残す |
| 2026-03-05 | 操作語彙を確定：「石をはずす」（ピン解除）／「忘れる」（通常カード・枯れ草カード共通の消去） |
| 2026-03-05 | 「削除」という語彙はmurmur-fieldでは使わない |
| 2026-03-05 | クラスタ貢献度にブックマークインポート数（頭打ちあり）とタグ採用率（クラスタ内採用率ベース）を追加 |
| 2026-03-05 | 「ブックマーク数」指標を除外し、タグ多様性スコア（ユニークタグ数×厳選度比率）に置き換える |
| 2026-03-05 | タグ採用率は絶対数ではなくクラスタ内採用率で評価——先行者利益を緩和するため |
| 2026-03-05 | 厳選度比率（石÷総ブックマーク数）には最低ブックマーク数の下限設定が必要（除算エラー回避）——実装フェーズで確認 |
| 2026-03-05 | コミットメッセージはConventional Commits形式（`docs:` 等のプレフィックス）で統一 |
| 2026-03-05 | リポジトリ名：`murmur-field` / ディスクリプション：`Murmur Field: slow social bookmarking. Ambient rhythm. Gentle resonance. No noise.` |
| 2026-03-05 | 全ドキュメントを英語・日本語の順で併記するバイリンガル形式に統一 |
| 2026-03-05 | オンボーディング問2の文言：「少し遠ざけておきたい気分の話題」で確定 |
| 2026-03-05 | オンボーディング問3の文言：「マーマーフィールドを主に使いそうな時間帯は？」で確定 |
| 2026-03-05 | オンボーディングカテゴリ表示名：TAG_TAXONOMYとは別のやわらかい表示名を採用（詳細はONBOARDING_DESIGN参照） |
| 2026-03-05 | カテゴリ並び順：ことば・物語→哲学・こころ→自然・宇宙→ウェブ・雑学→テクノロジー・ものづくり→料理・食・農→暮らし・教育→ニュース・時事 |
| 2026-03-05 | 「忘れる」初回予告：通常カード・枯れ草カードそれぞれ初回のみ予告メッセージを表示。2回目以降は確認なし |
| 2026-03-05 | アンドゥ機能は設けない。初回予告によって「消えちゃった」の驚きを構造的に防ぐ |
| 2026-03-05 | オンボーディング画面のビジュアルトーンはUIデザインフェーズに委任 |

---

## 3. Documents Created This Session / 本セッション作成ドキュメント

| File / ファイル | Description / 説明 |
|---|---|
| `README.md` | Repository overview — bilingual / リポジトリ概要——バイリンガル版 |
| `MURMUR_FIELD_TAG_TAXONOMY.md` | Complete tag classification — content and emotional layers / タグ再分類完全版——コンテンツ系・感情系 |
| `MURMUR_FIELD_CLUSTER_CONTRIBUTION.md` | Cluster contribution score specification / クラスタ貢献度スコア仕様 |
| `MURMUR_FIELD_VISUAL_INTERACTION.md` | Visual and interaction design — cards, stones, withered grass, shake / ビジュアル・インタラクション設計 |
| `MURMUR_FIELD_AMBIENT_RHYTHM_MODEL.md` | Ambient Rhythm Model v1.1 — bilingual update with noise rule and time×tag table / 環境リズムモデル v1.1 |
| `MURMUR_FIELD_COMMENTS_DESIGN.md` | Comments design — ported from prior session v0.2, bilingual / コメント設計——前セッションv0.2のバイリンガル版 |
| `MURMUR_FIELD_USER_STORY.md` | User story — ported from prior session, bilingual, with ambient rhythm reference / ユーザーストーリー——前セッションのバイリンガル版 |
| `MURMUR_FIELD_ONBOARDING_DESIGN.md` | Onboarding design v1.0 — fully rewritten with session 4 decisions / オンボーディング設計 v1.0——セッション4決定事項を反映 |
| `MURMUR_FIELD_HANDOFF_20260305_Claude.md` | This document / 本ドキュメント |

---

## 4. Pending Items / 未決事項

**Priority High / 優先度高：**
- Chain Reaction score threshold — trigger condition for stage 2 presence feedback / Chain Reactionスコアの閾値——第二段階フィードバックのトリガー条件
- Character limit for「引用メモ」/「引用メモ」の文字数制限
- Specific unlock thresholds for gradual unlock axes / 段階的アンロックの軸の具体的な閾値

**Priority Medium / 優先度中：**
- Shake gesture conflict resolution — implementation verification (OS/framework dependent) / shakeジェスチャー衝突回避の実装確認（OS・フレームワーク依存）
- Whether first-time「忘れる」count is unified or independent across card types / 初回「忘れる」カウントの統一・独立の判断
- Minimum bookmark count floor for selectivity ratio (division-by-zero prevention) / 厳選度比率の最低ブックマーク数下限設定（除算エラー回避）
- Ambient Rhythm layer weights — initial placeholder values needed before beta / Ambient Rhythmレイヤー重みの初期仮置き値
- AI庭師（Gardeners）のペルソナ詳細設計

**Priority Low / 優先度低・将来フェーズ：**
- relations.jsonの距離スコアとUI連動仕様
- 個人リズム学習アルゴリズム詳細（Phase 1）
- 星座・菌糸ビューの設計（Phase 1）
- Micro Glance UI（将来検討）
- Layer 4（環境軸）の採否

---

## 5. Philosophical Core / 設計思想コア（変更禁止 / DO NOT MODIFY）

- **霧の演出（Fog of Visibility）:** Distant clusters are physically invisible or rendered as meaningless noise — structurally preventing context collision.  
  遠いクラスタの声は物理的に不可視、または意味をなさない「ざわめき」として処理し、文脈の衝突（嘲笑）を構造的に防ぐ。

- **バズより共鳴:** Resonance over reach. Cluster-internal density is the measure of value, not platform-wide counts.  
  全体のブックマーク数ではなく、クラスタ内密度を価値の指標とする。

- **AI Gardeners:** AI is a gardener, not an administrator. It seeds quality, then recedes as community becomes self-sustaining.  
  AIは管理者ではなく「庭師」。良質な文化の種をまき、コミュニティが自走を始めたら存在感を消す。

- **ネガティブ・オンボーディング:** Filtering begins not just from "what you love" but "what you want distance from (as a mood)."  
  「何が好きか」だけでなく「何から守られたいか（気分として）」を起点にフィルタリングを構築する。

- **静かに寄り添う:** The service adapts to the user's rhythm. It does not colonise the user's time.  
  サービスがユーザーの時間を支配するのではなく、ユーザーの時間のリズムにサービスが合わせる。

- **倫理ではなく物理を設計する:** Build structures that do not amplify — rather than judging and excluding.  
  特定ユーザーを判定・排除するのではなく、増幅しない構造を作る。

---

## 6. Instructions for Next AI / 次のAIへの伝言

Read this document and all files listed in section 3 before beginning work.  
作業を始める前に、このドキュメントとセクション3に記載された全ファイルを読むこと。

Rules that must be followed / 必ず守ること：

1. `approval_required: true` — confirm with the human before taking action / アクション前に人間の承認を求める
2. Philosophical Core must not be modified / PHILOSOPHICAL_COREは変更しない
3. Confirm priorities with the human before starting work / 未決事項の優先順位を人間と確認してから作業を始める
4. Append new decisions to SESSION_LOG / 決定事項を増やしたらSESSION_LOGに追記する
5. All documents must be written in English-first, Japanese-second bilingual format / 全ドキュメントは英語・日本語の順で併記するバイリンガル形式で書く
6. Use Conventional Commits prefix for all commit messages / コミットメッセージはConventional Commits形式を使う
7. Pass these rules to the next AI / このルールを次のAIにも引き継ぐこと

---

*END OF DOCUMENT*
