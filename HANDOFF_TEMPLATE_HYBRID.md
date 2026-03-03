# HANDOFF_TEMPLATE_HYBRID.md
# 汎用 AI リレー引き継ぎドキュメント（ハイブリッド版）
Version: 1.0 | 作成: 2026-03-04 | 提案: Claude (AI2)

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

```json
{
  "project_meta": {
    "name": "プロジェクト名をここに",
    "version": "YYYY.MM.DD",
    "initiator_type": "Human (Origin / First Runner)",
    "current_mode": "linear | parallel_synthesis",
    "core_priority": "思想継承優先"
  },
  "machine_readable_state": {
    "current_session_id": 1,
    "mode": "linear",
    "previous_actors": null,
    "contributors": [],
    "synthesizer": null,
    "current_actor": "AI1",
    "approval_required": true,
    "decision_log_count": 0,
    "auto_loop_guard": true,
    "cost_mode": "zero_cost",
    "next_task": "ここに次のタスクを記載"
  },
  "compressed_state": "mode=linear;session=1;actor=AI1;approval=true;cost=zero",
  "session_history": [
    {
      "session_id": 1,
      "mode": "linear",
      "origin": "human",
      "previous_actors": null,
      "contributors": ["AI1"],
      "synthesizer": null,
      "status": "in_progress",
      "date_started": "YYYY-MM-DD",
      "date_completed": null
    }
  ],
  "ongoing_tasks": {
    "priority_1": "タスク1",
    "priority_2": "タスク2"
  },
  "ai_role_rules": {
    "ai1": "役割の説明",
    "synthesizer": "並列セッション時：複数AIのアイデアを統合する。少数意見・矛盾も保存すること。",
    "human_manager": "最終承認者。Core Philosophy・Decision Logの変更権限を持つ唯一の存在。"
  },
  "decision_log": [
    {"date": "YYYY-MM-DD", "actor": "Human", "decision": "最初の決定をここに記録"}
  ]
}
```

---

# SESSION_LOG（作業記録）
- 箇条書き・実際に行った作業のみ
- 推測・感想・未来予測は禁止
- JSONブロックの更新点を必ず記録

```
SESSION_LOG:
- （作業内容をここに記載）
- JSONブロック更新点: なし
```

---

# SAMPLES（原文保存セクション）
> このセクションは要約・省略・改変禁止。
> 人間とAIの実際の発言・決定の原文をそのまま保存する。
> 「なぜその結論になったか」の生の文脈を守るために存在する。

```
[YYYY-MM-DD | Human]:
"ここに実際の発言を原文のまま貼り付ける"

[YYYY-MM-DD | AI (モデル名)]:
"ここに実際の発言を原文のまま貼り付ける"
```

---

# PHILOSOPHICAL_CORE（変更禁止）
> Human が承認した哲学・方針のみここに記載する。
> AI はここを読み取るが、書き換えることはできない。

- 例：「最初の走者は常にHumanであり、AIは補助である」
- 例：「思想の継承を短期最適化より優先する」

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
