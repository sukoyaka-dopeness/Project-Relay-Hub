# CANVAS STRUCTURE
## Overview
The rendering system uses a side-view scrolling street. The player character stays fixed at the center of the screen while the environment moves horizontally.
## 概要
描画システムは横スクロールの街構造を使用します。プレイヤーは画面中央に固定され、街の環境が左右にスクロールします。
## Camera Model
The camera is centered on the player. The player position on screen does not move. The world scrolls relative to the player movement.
## カメラモデル
カメラはプレイヤーを中心に固定されます。プレイヤーの画面上の位置は動きません。プレイヤーの移動に応じて世界がスクロールします。
## Coordinate System
The world is structured as a horizontal map.
Key properties:
- X axis represents street distance
- Y axis represents vertical layering
- Player position updates the world offset
## 座標システム
世界は横方向のマップとして構成されます。
主な構造：
- X軸：街の距離
- Y軸：高さレイヤー
- プレイヤー移動によりワールドオフセットが更新される
## Layer Structure
The canvas is divided into layered visual elements.
Back to front rendering order:
1. Sky layer
2. Far background (distant buildings)
3. Main buildings
4. Street environment objects
5. Player characters
6. Foreground objects
7. Light effects
## レイヤー構造
キャンバスは複数のレイヤーで構成されます。
描画順（奥→手前）
1. 空レイヤー
2. 遠景建物
3. 建物
4. 街オブジェクト
5. プレイヤー
6. 前景オブジェクト
7. 光エフェクト
## Environment Object Layer
Street objects appear along the walking path.
Examples:
- utility poles
- vending machines
- benches
- streetlights
- shop shutters
- signboards
Objects are anchored to world coordinates.
## 環境オブジェクトレイヤー
街のオブジェクトは歩道に沿って配置されます。
例：
- 電柱
- 自動販売機
- ベンチ
- 街灯
- 商店シャッター
- 看板
オブジェクトはワールド座標に固定されます。
## Advertising Surfaces
Certain objects contain surfaces intended for sponsorship or advertising.
Examples:
- bench back panels
- vending machine logos
- shop signs
- billboard panels
These may initially appear as placeholder textures.
## 広告配置面
いくつかのオブジェクトにはスポンサー・広告用の表示面があります。
例：
- ベンチ背もたれ
- 自販機ロゴ面
- 商店看板
- ビルボード
初期段階ではプレースホルダーテクスチャでも構いません。
## Player Layer
Players appear on the street level. Player avatars may initially be simple silhouettes or minimal characters. Future versions may allow different avatar types.
## プレイヤーレイヤー
プレイヤーは道路レベルに表示されます。初期段階ではシルエットなどの簡易キャラクターを使用します。将来は異なるアバタータイプが追加される可能性があります。
## Visibility Radius
Only nearby players are rendered. Players outside the visibility range are not shown. This maintains a sparse nighttime feeling.
## 可視範囲
近くにいるプレイヤーのみ描画されます。可視範囲外のプレイヤーは表示されません。これにより夜の静かな密度を保ちます。
## Lighting
Streetlights provide local light sources. Light intensity should remain soft to maintain nighttime atmosphere.
## 照明
街灯は局所的な光源として機能します。光は柔らかく、夜の雰囲気を保つようにします。
## Performance Considerations
The canvas system should prioritize simplicity.
Key goals:
- low rendering cost
- minimal animation
- lightweight assets
## パフォーマンス設計
キャンバス構造はシンプルさを優先します。
目標：
- 低レンダリング負荷
- 最小限のアニメーション
- 軽量アセット
