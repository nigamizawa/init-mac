# vscode

vscodeの設定をgitによる履歴管理を行う。
設定の同期だけならば、ポータブルモードとか、Settings Syncとかあるっぽいけど設定変更の履歴まで管理できないみたい。


## vscodeの設定ファイル一覧概要

macだと`~/Library/Application\ Support/Code/User/`に設定ファイルが格納されている

- [settings.json](./settings.json) : 設定全般
- [keybindings.json](./keybindings.json) : キーバインド
- [init_vscode_settings.sh](init_vscode_settings.sh): vscodeの初期設定スクリプト

## 各種設定ファイル詳細

### 拡張機能について

なんかhomebrewで管理できるみたいw

### init_vscode_settings.sh

初期化スクリプトでやってること

1. 各種既存設定ファイルを`~/Library/Application\ Support/Code/User/`を削除する
   1. 対象は`settings.json`と`keybindings.json`
2. 本プロジェクトの設定ファイルを`~/Library/Application\ Support/Code/User/`にシンボリックリンクする

## その他

### 参考ドキュメント、設定集

- <https://code.visualstudio.com/docs/getstarted/settings>
- <https://zenn.dev/sayuki_coding/articles/c389d9ad48feaa>
- [VSCodeでvimrcの設定を読み込みたい](https://qiita.com/kino-ma/items/735148fe58dc14898903)
