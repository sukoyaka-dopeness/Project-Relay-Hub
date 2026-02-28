# Perplexity-session1.md

## SESSION_LOG

- 作業1: 「後にあなたに引き継ぎメッセージを作ってもらうとき既存の事例、ツール・関連例を原文のまま記録してもらうので、記憶しておいてください。」

- 作業2: 「記録完了: フォーク小説sukoyaka-dopeness/forkable-novelの全設計仕様・事例・コードスニペットを原文原文のまま記憶しました。」

- 作業3: 「引き継ぎドキュメントを作る準備はできた？」

- 作業4: 「引き継ぎドキュメント作成準備：完全完了」「記憶済み全要素（この会話から抽出・原文保存）：[📋 プロジェクト名: sukoyaka-dopeness/infinite-epic（仮）...]」

- 作業5: 「Promptを入力します。# AI リレーディスカッション 引き継ぎプロンプト」

- 作業6: 「# SESSION_LOG [...] # RELAY_DOCUMENT_COMPRESSED [...] # RELAY_DOCUMENT_SAMPLES [...]」（完全な引き継ぎドキュメントコードブロック）

COMPRESSED の更新点: なし  
SAMPLES の更新点: なし


## RELAY_DOCUMENT_COMPRESSED

#PROJECT_OVERVIEW
[NAME=infinite-epic|OWNER=sukoyaka-dopeness|CONCEPT=フォーク可能無限叙事詩]
[GENRE=ポストモダン群像文学|WHY=『街』の無限拡張]
[TARGET=文学史家;テック層;一般読者]

#TECHNICAL_ARCHITECTURE
[PHYSICAL_FILES=TIMESTAMP-SHA-title.md|SPEC=2026-0301T005112Z-8f2d1a3b-warrior.md]
[LOGICAL_LINKS=.meta/relations.json|precedes/follows/characters/location]
[FINAL_CHAPTER=05-convergence.md|PROTECTED=fork不可|CONTAINS=全貢献者クレジット]
[TIMELINE=自動ソート|UI=全章マップ+進捗表示]

#UI_SPECIFICATION
[5BUTTONS=⬅️前の章/➡️後の章/🌿分岐/⏪前書く/⏭️後書く]
[UX_MODES=読書モード/創作モード/拡張モード]
[PROGRESS=現在位置(3/総章数)+貢献者数+活発分岐数]

#COPILOT_USAGE
[FREE_TIER=月50回/人|STRATEGY=各フォーク独立Copilot利用]
[HYBRID=人間90%+AI10%|ACTIONS=貢献度計算/relations更新/マップ生成]

#COPYRIGHT_COMPLIANCE
[PD_SEED=アリス/シェイクスピア/グリム|MULTILINGUAL=ja/en/zh]
[WARNING_DIALOG=初回表示|LOCALSTORAGE=同意記録]
[GLOBAL_PD=.meta/public-domain.json|universal_safe/region_safe/warning_needed]

#REVENUE_SHARING
[CONTRIBUTION=Gitログ語数計算|SHARE=貢献度比例]
[VOTE=.meta/revenue-vote.json|TRIGGER=出版オファー多数決]

#PREDECESSOR_COMPARISON
[TABLE=
|作品|構造|参加性|進化性|
|『街』|固定8ルート|読むだけ|静的|
|ゲームブック|有限分岐|読むだけ|静的|
|可能世界VN|メタ分岐|読むだけ|静的|
|Twine|選択肢グラフ|読むだけ|静的|
|infinite-epic|Gitフォーク無限分岐|全世界フォーク/PR|Git履歴永遠進化|]

#IMPLEMENTATION_ROADMAP
[PHASE1=5ファイル手書き(Day1)]
[PHASE2=GitHub Pages+X投稿(Day2-3)]
[PHASE3=フォーク解禁+AI補助(Day7)]
[PHASE4=最終章完成+クレジット(Day30)]

#CURRENT_AI=Perplexity
#SESSION_NUMBER=1
#NEXT_AI=未定
#NOTE_ALL_NUMBERS=1247等は将来イメージの仮数字


## RELAY_DOCUMENT_SAMPLES

### ファイル名例
2026-0301T005112Z-8f2d1a3b-warrior.md  
2026-0301T005256Z-c5e7f9d2-stargazer.md  
-1000-00:00:00Z-9g3e4f5c-origin.md

### relations.json例
{
  "2026-0301T005112Z-8f2d1a3b": {
    "title": "戦士の覚醒",
    "precedes": "2026-0301T010033Z-a1b2c3d4",
    "follows": null,
    "characters": ["warrior_A"],
    "location": "battlefield"
  }
}

### 5ボタンUI例
[⬅️ 前の章を読む] [➡️ 後の章を読む]  
[🌿 この章から分岐] [⏪ この章の前を書く] [⏭️ この章の後を書く]

### 最終章クレジット例
---
# 🌉 無限神殿 - 全時間軸完結
[感動の収束シーン...]

## ✨ この叙事詩を創った1,247人
- 戦士ルート: sukoyaka-dopeness (1,250語)
- 星読みルート: user123 (980語)
- 深淵ルート: ai-collaborator456 (1,100語)
**総文字数: 3,780語 | 1,247人の共著**

### 著作権警告ダイアログ
<div id="copyright-warning">
  <h3>🚨 著作権法遵守のお願い</h3>
  <ul>
    <li>✅ オリジナルキャラ・ストーリーのみ</li>
    <li>✅ 著作権切れ作品（プーさん等）</li>
    <li>✅ CC-BYライセンス作品</li>
    <li>❌ 商業作品の直引用・キャラ登場</li>
  </ul>
  <label><input type="checkbox" id="agree"> 同意する</label>
</div>

### README冒頭文言
# 🌌 infinite-epic：世界初のフォーク可能無限叙事詩
**sukoyaka-dopenessが2026/2/28に着想**  
全世界クリエイターへ：フォークして歴史を紡げ！
