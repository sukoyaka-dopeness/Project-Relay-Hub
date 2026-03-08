# おやじストッパー 仕様書

## 📋 機能仕様表

| 機能名 | トリガー | 応答例 | 技術要件 | 優先度 |
|--------|----------|--------|----------|--------|
| **リアルタイムおやじ検知** | ダジャレ3連続 | `「はい1回目～！」` | Whisper Tiny + regex | ★★★★★ |
| **昭和トークループ** | 同一話5回以上 | `「その話今週5回目です」` | SQLite履歴DB + keyword | ★★★★☆ |
| **絵文字洪水** | 1発言5個以上 | `「絵文字祭りですね！」` | emoji-regex | ★★★☆☆ |
| **昭和度メーター** | キーワード密度75%↑ | `「昭和度危険水域！」` | TF-IDF簡易版 | ★★★★☆ |
| **自動ギャグストック** | ネタ切れ検知 | `「次はこのダジャレどう？」` | Llama3.2 1.5B生成 | ★★★☆☆ |
| **P2Pギャグ交換** | 友達リクエスト | AirDrop/Quick Share | WebRTC + Simple-Peer | ★★☆☆☆ |
| **落ち込み寄り添い** | 声トーン-20%低下 | `「昭和話なら聞きますよ」` | Pitch分析 + 簡易感情 | ★★★☆☆ |

## 🔋 バッテリー最適化仕様

### 消費予測（iPhone15 Pro基準）
| 運用モード | 1時間消費 | 1日持続時間 |
|------------|-----------|-------------|
| 常時録音 | 12-15% | 8時間 |
| **キーワード起動** | **3-5%** | **24時間OK** |
| 通知のみ | 1-2% | 48時間 |

### 最適化手法
キーワードトリガー: 「おやじ」「昭和」「ダジャレ」で録音開始

AI量子化: Llama3.2 INT8（メモリ4GB→1.5GB）

OS連携: iOS最適化充電 / Android適応バッテリー

スリープモード: 無音30秒で休止

## 📱 対応デバイス・最小スペック

| カテゴリ | モデル | 必要スペック | 備考 |
|----------|--------|--------------|------|
| **スマホ** | iPhone15+ | A17 Pro / 8GB | Neural Engine必須 |
| | Pixel8+ | Tensor G3 / 8GB | 最適 |
| | Galaxy S23+ | Exynos/Snapdragon 8Gen3 | Quick Share |
| **ウォッチ** | Apple Watch9+ | watchOS10+ | 振動通知 |
| | Galaxy Watch6+ | WearOS4+ | 通知 |
| **イヤホン** | AirPods Pro2 | iOS17+ | ささやき |
| | Galaxy Buds2 Pro | Android11+ | 通知 |

## 🛠️ 技術スタック詳細

┌── Frontend
│ ├── React Native + Expo (クロスプラットフォーム)
│ ├── Tamagui (UIライブラリ)
│ ├── Lottie (アバターアニメ)
│ └── 創英角ポップ体 (フォント)
│
├── AI Core
│ ├── Llama3.2 1.5B (MLC-LLM on-device)
│ ├── Whisper Tiny (音声認識)
│ └── Web Speech API (TTS)
│
├── 通信
│ ├── WebRTC + Simple-Peer (P2P)
│ ├── Nearby Share API (Android)
│ └── AirDrop (iOSネイティブ)
│
└── Storage
└── SQLite + AsyncStorage (ローカルログ)


## 🎮 アバター仕様（6種）

| アバター | 性格 | ツッコミ強度 | 代表フレーズ | 音声 |
|----------|------|-------------|-------------|------|
| 冷徹秘書 | 事務的 | 低 | `「3回目です」` | ロボ音 |
| 若者後輩 | 友達 | 中 | `「またそれ～！」` | 軽快 |
| **昭和司会者** | 実況 | **高** | `「はい1回目～！」` | **デフォルト** |
| 孫キャラ | 甘え | 低 | `「おじいちゃん～お口くさい～」` | 幼児 |
| おかん | 心配 | 中 | `「元気ないね…」` | 母親 |
| ギャル後輩 | 毒舌 | 高 | `「それ古すぎ！」` | ギャル |
| 飲み屋の友達 | 毒舌 | 高 | `「まったく〇〇さんはしょうがねえなあ！！」` | おやじ |

## 📊 メトリクス計算式

昭和度 = (昭和キーワード出現数 / 総単語数) × 100
おやじ指数 = (ギャグ回数×3) + (繰り返し×2) + 絵文字数
ギャグ連発 = 過去180分間のダジャレ検出数


**安全圏**: 昭和度<70%, おやじ指数<100, ギャグ<5回/1日

## 🔌 P2P実装詳細
iOS ↔ iOS: AirDrop (ネイティブ)
Android ↔ Android: Quick Share (標準)
クロスプラットフォーム: WebRTC (アプリ内)
フォールバック: Bluetooth Classic 5.0
転送データ: ギャグストックJSON (最大10KB)


## 🎨 デザイン仕様
カラー:
├── メイン: ピンク #FF69B4 (ホットピンク)
├── アクセント: ラメシルバー #C0C0C0
├── 背景: 薄ピンク #FFE4E1
└── 文字: ダークネイビー #1C2526

フォント: 創英角ポップ体 (1位) → Rounded M+ (2位)
角丸: 12px (全ボタン・カード)
影: ピンクグラデーション (hover時)


## 🚀 デプロイ手順

```bash
# 開発環境構築
npx create-expo-app oyaji-stopper --template
cd oyaji-stopper

# 依存関係
expo install expo-av expo-haptics expo-speech
npm i @tamagui/core llama-node react-native-lottie

# 初回ビルド
npx expo run:ios    # or :android
npx expo start      # Expo GoでQRスキャン

# ストア公開
eas build --platform ios
eas build --platform android

📈 開発スケジュール（MVP）
フェーズ	作業内容	所要日数
Week1	音声認識 + 基本ツッコミ	5日
Week2	アバターUI + 昭和度	4日
Week3	P2P + バッテリー最適化	5日
Week4	テスト + ストア申請	4日
総工数: 18日 → 4週間でAppStore公開可能

Phase 5: Perplexity - 仕様書完成
実装可能な哲学の具現化
2026.03.09







