# zsh

プラグインの管理とかだるいのでいい感じのフレームワーク([prezto](https://github.com/sorin-ionescu/prezto))を利用する。

## prezto

- https://github.com/sorin-ionescu/prezto

### install and setup

preztoをインストールする
```
git clone --recursive https://github.com/sorin-ionescu/prezto.git "${ZDOTDIR:-$HOME}/.zprezto"
```

設定ファイルの配置（このディレクトリで操作）
```
setopt EXTENDED_GLOB
for rcfile in "$PWD"/^README.md(.N); do
  ln -s "$rcfile" "${ZDOTDIR:-$HOME}/.${rcfile:t}"
done
```

### update

```
cd $ZPREZTODIR
git pull
git submodule sync --recursive
git submodule update --init --recursive
```