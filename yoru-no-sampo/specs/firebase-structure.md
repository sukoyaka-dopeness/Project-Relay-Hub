# FIREBASE_STRUCTURE.md

## English
This document describes the Firebase data structure for the night walk project.  
It is designed to support MVP functionality while allowing future expansion.

### Collections and Documents

#### Players
- `playerId` (document ID)
  - `position`: {x, y} – current coordinates on the map
  - `characterType`: "shadow" | "human" | future options ("cat", "ghost")
  - `lastMessageId`: reference to Messages collection
  - `lastStampId`: reference to Stamps collection
  - `timestamp`: last update time

#### Map
- `mapId` (document ID)
  - `tiles`: 2D array of tile data
  - `buildings`: array of building objects
    - `id`
    - `position`
    - `type` (residential, commercial, park, etc.)
    - `lightState` (on/off, for future time-based animation)
  - `adSpaces`: array of sponsor/advertisement placeholders

#### Messages
- `messageId` (document ID)
  - `text`
  - `type`: "MVP" | "future"
  - `authorId` (optional, for future user-generated content)

#### Stamps
- `stampId` (document ID)
  - `imageUrl`
  - `type`: "MVP" | "future"

### Real-Time Sync
- Players collection updates trigger WebSocket broadcasts
- Position, lastMessageId, and lastStampId are propagated to nearby players

### Future Considerations
- Additional fields for seasonal events or area-based sponsorship
- Expansion to new streets or residential zones
- Optional sound fields for atmosphere (ambient sounds, wind, subtle city noise)

---

## 日本語
このドキュメントは「夜の散歩」プロジェクトにおけるFirebaseのデータ構造を示します。  
MVP機能をサポートしつつ、将来的な拡張にも対応できる設計です。

### コレクションとドキュメント

#### Players（プレイヤー）
- `playerId`（ドキュメントID）
  - `position`: {x, y} – マップ上の現在位置
  - `characterType`: "影" | "人型" | 将来の選択肢 ("猫", "おばけ")
  - `lastMessageId`: Messagesコレクションへの参照
  - `lastStampId`: Stampsコレクションへの参照
  - `timestamp`: 最終更新時間

#### Map（マップ）
- `mapId`（ドキュメントID）
  - `tiles`: タイルの2次元配列データ
  - `buildings`: 建物オブジェクトの配列
    - `id`
    - `position`
    - `type`（住宅、商業、公園など）
    - `lightState`（点灯/消灯、将来的な時間変化用）
  - `adSpaces`: スポンサー・広告スペースのプレースホルダー配列

#### Messages（メッセージ）
- `messageId`（ドキュメントID）
  - `text`
  - `type`: "MVP" | "将来実装"
  - `authorId`（将来のユーザー生成コンテンツ用、任意）

#### Stamps（スタンプ）
- `stampId`（ドキュメントID）
  - `imageUrl`
  - `type`: "MVP" | "将来実装"

### リアルタイム同期
- Playersコレクションの更新はWebSocketでブロードキャスト
- 位置、lastMessageId、lastStampIdを近くのプレイヤーに伝える

### 将来の拡張
- 季節イベントやエリアごとのスポンサー用フィールド追加
- 新しい通りや住宅地への拡張
- 雰囲気向上のための音声フィールド（環境音、風、街のささやきなど）
