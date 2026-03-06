# MVP MAP SPEC
## Overview
The MVP map is a small night town designed for quiet walking. The map is not meant to simulate a realistic city. Instead it provides a minimal environment that creates the feeling of walking through a calm nighttime street.
## 概要
MVPマップは静かな夜の散歩のための小さな街です。現実の都市を再現することが目的ではありません。静かな夜道を歩いている感覚を作る最小限の環境を提供します。
## Map Structure
The map is a horizontally scrolling street. The player remains fixed at the center of the screen while the town scrolls left and right.
## マップ構造
マップは横方向にスクロールする街路です。プレイヤーは画面中央に固定され、街が左右にスクロールします。
## Map Length
The MVP map should be long enough to allow several minutes of walking without reaching the edge immediately.
The map may have edges, but reaching them should not happen quickly.
## マップの長さ
MVPマップは数分歩いてもすぐ端に到達しない長さにします。マップに端がある場合でも、すぐ到達する構造にはしません。
## Environment Zones
The MVP town is composed of simple repeating zones.
Example structure:
1. Residential street
2. Small commercial street
3. Park area
4. Residential street
## 環境ゾーン
MVPの街はいくつかのシンプルなゾーンで構成されます。
例：
1. 住宅街
2. 小さな商店街
3. 公園
4. 住宅街
## Residential Area
Residential areas contain apartment buildings and houses. Window lights may appear randomly to create the feeling that some people are awake at night.
## 住宅街
住宅街にはマンションや住宅が配置されます。窓の明かりがランダムに点灯し、夜でも誰かが起きている雰囲気を作ります。
## Commercial Street
The commercial street contains closed shop shutters and signboards. Most shops are closed, reinforcing the late-night atmosphere.
## 商店街
商店街には閉まったシャッターの店と看板があります。多くの店は閉まっており、深夜の雰囲気を作ります。
## Park Area
The park provides a quiet open space.
Elements may include:
- benches
- trees
- streetlights
## 公園
公園は静かな空間です。
配置例：
- ベンチ
- 木
- 街灯
## Street Objects
Street objects appear regularly along the map.
Examples:
- utility poles
- vending machines
- benches
- streetlights
- small signs
## 街オブジェクト
街のオブジェクトは一定間隔で配置されます。
例：
- 電柱
- 自動販売機
- ベンチ
- 街灯
- 小さな看板
## Advertising Locations
Advertising surfaces exist but may initially be placeholders.
Examples:
- bench back panels
- vending machine branding
- shop signboards
- billboard signs
## 広告配置
広告を配置できる場所を用意しますが、初期段階ではプレースホルダーでも構いません。
例：
- ベンチ背もたれ
- 自販機ロゴ
- 商店看板
- ビルボード
## Encounter Density
Players should appear occasionally rather than frequently. The map should feel calm even if the system has multiple users online.
## 出会い密度
プレイヤー同士の出会いは頻繁ではなく、たまに起きる程度にします。ユーザー数が増えても街は静かな密度を保ちます。
## Visual Rhythm
The environment should have a slow visual rhythm.
Objects should not be too dense. Periods of quiet empty street are important.
## 視覚的リズム
街の景観にはゆっくりしたリズムを持たせます。オブジェクトを詰め込みすぎず、何もない静かな道の区間も重要です。
## Future Expansion
Future versions may expand the map with additional districts. Players may eventually walk between different areas such as shopping streets and residential neighborhoods.
## 将来拡張
将来は街を拡張し、異なるエリアを追加できます。商店街から住宅街などへ歩いて移動できる構造も将来実装の候補です。
