# Firebase データ構造（Realtime DB）

- active_users: { [pushID]: { joined_at, night_start, icon_type, last_stamp, sheep_count: 0, ... } }
- stamps_log: { [pushID]: { user_id, type, content, timestamp } }  // 最近のログ（制限数で古い削除）
- ai_patterns: { ai1: { last_action, next_delay } }
- config: { stamp_list: [...], text_presets: [...] }
