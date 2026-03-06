# MOVEMENT SYSTEM

## Purpose
Defines how the player moves through the world, including controls, walking speed, and camera behavior.
## 目的
プレイヤーが世界を移動する方法（操作、歩行速度、カメラ挙動）を定義する。

# Basic Principle
## English
Movement should feel calm and natural, like a slow night walk. It should not resemble a fast-paced game. The goal is quiet wandering.
## 日本語
移動は静かで自然な「夜の散歩」の感覚を目指す。ゲームのような速い移動ではなく、穏やかな歩行体験にする。

# Player Position
## English
The player remains fixed at the center of the screen. The world scrolls around the player as they move.
## 日本語
プレイヤーは常に画面中央に固定される。移動すると世界の方がスクロールする。

# Controls

## PC Controls
### English
Players can move using keyboard input or mouse clicks.
### 日本語
PC版ではキーボード操作またはクリックで移動できる。

### Example
#### English
- Arrow keys: move direction
- WASD: move direction
- Mouse click: walk toward clicked direction
#### 日本語
- 矢印キー：移動
- WASDキー：移動
- マウスクリック：クリック方向へ移動

## Mobile Controls
### English
Players move by tapping the screen.
### 日本語
スマートフォン版では画面タップで移動する。

### Example
#### English
- Tap direction to walk
- Hold to continue moving
#### 日本語
- タップ方向へ歩く
- 長押しで歩き続ける

# Walking Speed

## English
Walking speed should feel relaxed and slightly slow to match the atmosphere of a night walk.
Final tuning will be performed during beta testing.
## 日本語
歩行速度は夜の散歩に合う、少しゆっくりした速度にする。最終的な調整はβテストで行う。

# Map Boundaries

## English
Maps may have boundaries. If a player reaches the edge of the map, they stop moving in that direction.
## 日本語
マップには端が存在する場合がある。プレイヤーが端に到達した場合、その方向には進めない。

# Obstacles

## English
Buildings and certain structures block movement.
Players cannot walk through them.
## 日本語
建物や一部の構造物は通行できない障害物として扱う。

# Camera Behavior

## English
The camera follows the player smoothly with no abrupt movement.
## 日本語
カメラはプレイヤーに追従し、急激な動きは行わない。

# Future Movement Ideas

## English
Future versions may include additional movement features.
## 日本語
将来バージョンでは移動システムが拡張される可能性がある。

### Examples
#### English
- Cat character walking on fences
- Different movement styles for different characters
#### 日本語
- 猫キャラクターが塀の上を歩く
- キャラクターごとの移動スタイル
