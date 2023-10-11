# Keybindings

## Setting Note


### ショートカットの置き換え

以下の設定追記が必要
- 既存ショートカットの無効化
- 新規ショートカットの追加

コマンド名の前に`-`を記述することで既存ショートカットを無効にできる。
以下は`ctrl+a`を`ctrl+s`に入れ替えるサンプル

```json
[
  {
    "key": "ctrl+s",
    "command": "editor.action.selectAll"
  },
  {
    "key": "ctrl+a",
    "command": "-editor.action.selectAll"
  }
]
```
