# TECH_STACK.md

## Philosophy
「夜の散歩 (yoru-no-sampo)」の技術選定は、  
**シンプルさ・軽さ・長期維持のしやすさ**を重視します。

MVP段階では、次の原則を採用します。

- 小規模チームでも維持できること
- 実装の複雑さを最小限にすること
- 将来の拡張が可能であること

最初からスケールを想定した巨大な構成にはしません。

---

## Frontend

### Core
- HTML5
- CSS
- JavaScript

### Rendering
- Canvas API

理由：
- 軽量
- ブラウザ互換性が高い
- 2Dゲームとの相性が良い

ゲームエンジンはMVPでは使用しません。

---

## Backend

### Runtime
- Node.js

### Framework
- Express

理由：
- シンプル
- MVPに十分
- リアルタイム通信との相性が良い

---

## Real-Time Communication

### Protocol
- WebSocket

### Library
- Socket.IO（候補）

用途：
- プレイヤー位置共有
- すれ違いイベント検出
- メッセージ表示

---

## Database

### MVP
- SQLite

理由：
- セットアップが簡単
- 小規模サービスに適している
- 運用コストが低い

### 将来候補
- PostgreSQL

---

## Hosting

### MVP候補
- Vercel
- Fly.io
- Render

要件：
- Node.js対応
- WebSocket対応
- 小規模運用可能

---

## Map Data

### MVP
手作りのタイルマップを使用します。

形式：
- JSON
- またはシンプルな配列データ

マップは小さな街1つから開始します。

---

## Client Platforms

### Desktop
- ブラウザ

### Mobile
- ブラウザ

ネイティブアプリはMVPでは作りません。

---

## Asset Style

画像は以下を想定します。

- ピクセルアート
- 軽量PNG
- 低解像度

理由：
- 夜の雰囲気と相性が良い
- 軽量
- 制作コストが低い

---

## Scaling Strategy

MVPではスケールを優先しません。

最初の目標は：

- 小さく動くこと
- 安定して動くこと

プレイヤーが増えた場合にのみ、次の対応を検討します。

- データベース移行
- サーバー分散
- マップ拡張

---

## Guiding Principle

技術は目的ではありません。

このプロジェクトの目的は  
**静かな体験を作ること**です。

技術はその体験を支えるためだけに存在します。
