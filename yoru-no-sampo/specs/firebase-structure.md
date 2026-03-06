# firebase-structure.md

## 🌙 Firebase Structure — 夜の散歩（MVP）

本書は「夜の散歩」MVPにおける  
**Firebase Realtime Database / Anonymous Auth の使用方針とデータ構造**  
をまとめたものです。

Firebase は以下の目的に限定して使用する：

- 他ユーザーの「気配」（presence）の同期  
- スタンプ送信ログ  
- 定型文送信ログ  
- 広告クリックログ  
- 気分アイコンの入室ログ  
- 匿名ユーザー識別（Anonymous Auth）

---

# 1. Authentication（匿名認証）

### ✔ Anonymous Auth を使用
- ユーザー名は不要  
- 個人情報は扱わない  
- UID のみを presence やログに使用

```
auth/
  uid: string
```

---

# 2. Presence（他ユーザーの気配）

他ユーザーの位置を「点」で表現するためのデータ。

### ✔ 更新頻度  
- 1〜2秒ごとに現在位置を送信  
- 切断時は自動で削除（onDisconnect）

### ✔ データ構造

```
presence/
  {uid}/
    x: number        // 現在の横位置（スクロール位置）
    mood: string     // 気分アイコン（入室時に選択）
    updatedAt: number // タイムスタンプ
```

### ✔ 表示仕様  
- 名前は表示しない  
- 点の揺れや淡い動きはクライアント側で処理  
- mood は UI には出さず、内部的な分類に使用

---

# 3. 入室ログ（気分アイコン）

ユーザーが入室時に選んだ気分を記録する。

### ✔ 用途  
- 深夜の利用傾向の分析  
- 気分ごとの滞在時間の把握（将来）

### ✔ データ構造

```
enterLogs/
  {logId}/
    uid: string
    mood: string
    timestamp: number
```

---

# 4. スタンプログ

ユーザーがスタンプを送信したときに記録する。

### ✔ 用途  
- スタンプの人気分析  
- 不正利用の検知（連打など）

### ✔ データ構造

```
stampLogs/
  {logId}/
    uid: string
    stampId: string   // どのスタンプか
    x: number         // 送信時の位置
    timestamp: number
```

---

# 5. 定型文ログ

ユーザーが定型文を送信したときに記録する。

### ✔ 用途  
- どの言葉がよく使われるかの分析  
- 時間帯ごとの傾向

### ✔ データ構造

```
textLogs/
  {logId}/
    uid: string
    textId: string    // 定型文のID
    x: number
    timestamp: number
```

---

# 6. 広告クリックログ

広告（自販機・コンビニ・看板）がタップされたときに記録する。

### ✔ 用途  
- 広告効果の測定  
- どの広告が自然に見えるかの分析  
- 将来の広告最適化

### ✔ データ構造

```
adClickLogs/
  {logId}/
    uid: string
    adType: string     // vending, convenience, signboard
    adId: string       // 個別広告のID
    x: number          // クリック時の位置
    timestamp: number
```

---

# 7. データの保持方針

### ✔ presence  
- 常に最新のみ  
- 切断時に自動削除

### ✔ 各種ログ（enterLogs / stampLogs / textLogs / adClickLogs）  
- MVPでは削除しない  
- 将来、一定期間でアーカイブする可能性あり

---

# 8. セキュリティルール（概要）

### ✔ 読み取り  
- presence は全員が読み取り可能  
- ログは読み取り不可（管理者のみ）

### ✔ 書き込み  
- presence は本人のみ  
- ログは誰でも書き込み可能（匿名）

※ 詳細な security rules は MVP-spec.md に統合予定

---

# 9. 今後の拡張（将来実装）

- 天気依存のデータ（晴れ／雨／霧）  
- 季節依存のデータ（夏の虫など）  
- 道の種類の切り替えログ  
- AIキャラの発話ログ  
- 朝の演出のトリガー記録

---

# 10. このファイルの目的

- Firebase の役割を明確にする  
- データ構造を統一し、後続の開発者やAIが迷わないようにする  
- MVP の範囲を明確にし、将来実装との境界を保つ

---
