# MVP SPECIFICATION

## Overview
The MVP provides a minimal shared night walking experience.
Players walk through a small quiet town at night. They may occasionally encounter another player. Interaction is intentionally limited.
The goal of the MVP is to validate whether a quiet shared night space can work with a very small number of concurrent users.

## 概要
MVPは「最小構成の夜の共在散歩体験」を提供します。
プレイヤーは静かな夜の街を歩きます。ときどき別のプレイヤーとすれ違います。インタラクションは意図的に最小限にします。
目的は、少人数同時接続でも成立する夜の共在空間が成立するかを検証することです。

## Core Experience
The core experience consists of three simple actions:
- Walk through the town
- Occasionally encounter another player
- Send a small stamp
There is no chat, no profiles, and no performance pressure.

## コア体験
コア体験は次の3つのみです。
- 街を歩く
- ときどき他のプレイヤーと出会う
- 小さなスタンプを送る
チャット、プロフィール、自己表現の圧力はありません。

## Player Perspective
The player character remains fixed at the center of the screen.
The environment scrolls as the player walks.
If the map has edges, the player can walk to the edge.

## プレイヤー視点
プレイヤーは常に画面中央に固定されます。
プレイヤーが歩くと街の背景がスクロールします。
マップに端がある場合、プレイヤーはその端まで歩くことができます。

## Visual Perspective
The visual style is a side-view street perspective.
The player appears as if viewed from the side while walking through the street.
This allows environmental elements such as:
- utility poles
- vending machines
- benches
- shop fronts
- advertising signs
to appear naturally along the street.

## 視覚的視点
ビジュアルは横から見た街の視点（サイドビュー）です。
プレイヤーは街を横から見た形で歩きます。
この視点により、次のような要素を自然に配置できます。
- 電柱
- 自動販売機
- ベンチ
- 商店のシャッター
- 看板や広告

## Encounters
Players occasionally encounter others while walking.
Encounters should feel natural and infrequent, similar to passing someone during a real night walk.
Player density should remain visually sparse even if the total user count increases.

## 出会い
プレイヤーは歩いているとときどき他のプレイヤーに出会います。
これは現実の夜の散歩のように自然でまれに起きるものとします。
ユーザー数が増えても画面上の密度は低く保たれます。

## Interaction
Interaction is intentionally minimal.
The MVP includes a small set of stamps such as:
- hello
- nod
- moon
- good night
No chat is included in the MVP.

## インタラクション
インタラクションは意図的に最小限にします。
MVPでは次のような少数のスタンプのみを使用します。
- hello
- nod
- moon
- good night
チャット機能はMVPには含めません。

## Environment Elements
The environment creates the atmosphere of the night walk.
MVP elements include:
- streetlights
- utility poles
- benches
- vending machines
- closed shop shutters
- apartment buildings

## 環境要素
環境は夜の散歩の雰囲気を作る重要な要素です。
MVPに含まれる要素：
- 街灯
- 電柱
- ベンチ
- 自動販売機
- 閉まった商店のシャッター
- マンション

## Advertising Placeholder
The MVP includes visible locations where sponsorship or advertising can appear.
Examples:
- bench back panels
- vending machine branding
- shop signs
- billboards
These may initially appear as placeholder signs.

## 広告プレースホルダー
MVPではスポンサーや広告が入る場所だけを先に用意します。
例：
- ベンチ背もたれ広告
- 自販機ロゴ
- 商店街看板
- ビルボード
初期段階ではプレースホルダー表示でも構いません。

## Atmosphere
The service prioritizes a calm nighttime atmosphere.
Design choices should avoid overstimulation.
Silence, darkness, and small lights are important.

## 雰囲気
このサービスは静かな夜の空気感を重視します。
刺激が強すぎる演出は避けます。
静けさ、暗さ、小さな灯りが重要な要素です。

## MVP Technical Scope
The MVP focuses on validating the experience rather than scale.
Target characteristics:
- small town map
- low concurrent user count
- minimal interaction system
- lightweight environment assets

## MVP技術範囲
MVPではスケールよりも体験の検証を優先します。
想定：
- 小さな街マップ
- 少人数同時接続
- 最小限のインタラクション
- 軽量な環境アセット

## Out of Scope (Future Features)
The following are intentionally excluded from the MVP:
- character customization
- special avatars (ghost, cat, etc.)
- large maps
- advanced environment simulation

## MVP対象外（将来実装）
次の機能はMVPには含めません。
- キャラクターカスタマイズ
- 特殊アバター（オバケ、猫など）
- 大規模マップ
- 高度な環境シミュレーション
