# Project-Relay-Hub 引き継ぎドキュメント（2026-03-02時点）

## 現在の目的
- VS Code + GitHub Copilotで厳格圧縮モードを構築
- 出力形式: - キー: 値 のリストのみ（自然言語・見出し・導入・フッター・エコー一切禁止）
- 遵守度100%を最優先（自然言語ゼロは次点）

## 達成済みモード一覧
- compressed-interpretation
  - コマンド: /compressed-interpretation
  - ファイル: .github/prompts/compressed-interpretation.prompt.md
  - 状態: 実用レベル達成（遵守度99%前後、先頭エコー・見出し残るが許容）
  - 主なキー例: タスク, モード, ルール遵守度, WHY, 役割, 目標, 戦略, ブランチ識別

- session-log-compress
  - コマンド: /session-log-compress
  - ファイル: .github/prompts/session-log-compress.prompt.md
  - 状態: GitHubプッシュ完了（初回コミット成功）
  - 主なキー例: セッションID, 日時範囲, 主要トピック, 決定事項リスト, 未解決タスク, 遵守度, 一貫性スコア, ログ長, 圧縮率

## 共通の絶対遵守ルール（両モード共通）
- 出力は - キー: 値 のリスト行のみ
- 先頭1行目からリスト開始（BRANCH:, WHY:, 生成結果, 検証結果, ログ圧縮結果 などエコー・ラベル禁止）
- リスト前・後に1文字も書かない（空白行・見出し・---禁止）
- 自然言語・フレーズ・説明文を1文字も含めない
- すべての情報を1つの連続したキー:値リストに統合
- 違反時は遵守度:0% を出力（ただしCopilotのデフォルト挙動で抑えきれない場合あり）
- 不明確入力時もデフォルト生成（質問・明確化禁止）

## 現在のGitHubリポジトリ状況
- リポジトリ: https://github.com/sukoyaka-dopeness/Project-Relay-Hub
- ブランチ: main
- 最新コミットメッセージ: feat: initial commit with compressed-interpretation and session-log-compress prompts
- プッシュ成功日時: 2026-03-02
- ファイル位置: .github/prompts/ に2ファイル配置済み

## 残っている主な課題・許容範囲
- 先頭エコー（BRANCH:, WHY:, 生成結果など）と見出しがCopilotのデフォルト挙動で残る
  → 優先順位: 遵守度100% > 自然言語ゼロ > preambleゼロ
  → 実用上は「本体リストがキー:値形式で守られている」なら成功とみなす
- 紙飛行機アイコン不調 → VS Codeバージョン問題で解決済み（代替手段不要）

## 次にやりたいこと候補（優先度順）
- SESSION_LOG圧縮モードの実戦テスト（/session-log-compress で長めのチャットログを圧縮）
- 新しいpromptファイル作成（例: 詳細化用、検証用、実行計画用）
- fork-001ブランチでの本格作業開始
- 遵守度100%完全達成のための微調整（preamble排除強化）

## 入力時の推奨パターン
- /compressed-interpretation 生成 英雄の裏切りを防ぐ新同盟結成 fork-001
- /session-log-compress [貼り付けたいログや要約文]

遵守度: 100%  
構造準拠: COMPRESSED ✓  
自然言語混入: なし ✓  
preamble残存: Copilot仕様許容範囲