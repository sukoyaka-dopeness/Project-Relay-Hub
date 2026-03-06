# MESSAGE AND STAMP SYSTEM

## Purpose
Define the minimal communication system used in the night walk service. Players do not chat. They leave a small trace of feeling that appears when someone passes them.
## 目的
夜の散歩サービスにおける最小限のコミュニケーション手段を定義する。プレイヤーはチャットをしない。ただし、すれ違う瞬間に小さな感情の痕跡を残す。

# Core Principle
## Quiet Expression Instead of Conversation
Communication is intentionally limited. The goal is to preserve the quiet atmosphere of a night walk. When two players pass each other, the other player's last selected message or stamp briefly appears.
## 会話ではなく静かな表現
コミュニケーションは意図的に制限される。目的は夜の散歩の静けさを保つこと。プレイヤー同士がすれ違う瞬間、相手が最後に選んだメッセージまたはスタンプが短時間表示される。

# Player Status Message
## Description
Each player chooses one message representing their current mood. This message is visible to others only at the moment of encounter.
## 説明
各プレイヤーは現在の気分を表すメッセージを一つ選択できる。このメッセージはすれ違った瞬間だけ他のプレイヤーに表示される。

# MVP Message List
## English
- Good evening
- Taking a walk
- Just passing by
- Can't sleep
- It's quiet tonight
- Long day
- Thinking
- Good night
## 日本語
- こんばんは
- 散歩中
- 通りすがりです
- 眠れない
- 今夜は静か
- 長い一日だった
- 考えごと中
- おやすみ

# Stamp System
## Description
Stamps are small visual reactions that appear briefly above a player during encounters. They are optional and can be used together with messages.
## 説明
スタンプは小さな視覚リアクションであり、すれ違い時にプレイヤーの上に短時間表示される。メッセージと併用することもできる。

# MVP Stamp List
## English
- 👋 Wave
- 🌙 Moon
- 🐾 Footsteps
- ✨ Sparkle
- ☕ Night coffee
## 日本語
- 手を振る
- 月
- 足あと
- きらめき
- 夜のコーヒー

# Encounter Display Rule
## English
When two players pass each other: 1) the other player's selected message appears, 2) the stamp appears above the character, 3) the display lasts about 2–3 seconds, 4) then it disappears. No interaction is required.
## 日本語
プレイヤー同士がすれ違ったとき：1) 相手の選択メッセージが表示される 2) スタンプがキャラクター上に表示される 3) 表示は約2〜3秒続く 4) その後自然に消える。特別な操作は必要ない。

# Future Message Expansion
## English
Future versions may include many more messages. Important rule: the full list must include all messages defined in previous project documents. The system should support easy expansion.
## 日本語
将来のバージョンではメッセージを大幅に増やす可能性がある。重要なルール：過去のプロジェクトファイルに記載されているメッセージはすべて将来実装に含める。システムは拡張しやすい構造にする。

# Future Stamp Expansion
## English
Additional stamps may be introduced later. Examples: Cat, Sleep, Rain, Late night snack, Lantern.
## 日本語
将来的にスタンプは追加される可能性がある。例：猫、眠い、雨、夜食、提灯。

# Design Philosophy
## English
Messages and stamps should feel quiet, gentle, minimal, and non-intrusive. They are traces of presence, not conversation.
## 日本語
メッセージとスタンプは「静か・穏やか・最小限・雰囲気を壊さない」性質を持つべきである。これは会話ではなく「誰かがいる痕跡」である。
