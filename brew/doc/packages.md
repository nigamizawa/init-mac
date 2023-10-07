# パッケージ一覧

## rtx

公式曰く、「多言語対応ランタイムマネージャー（asdf rust クローン）」  
`asdf`の上位互換、より早いw
asdfと互換性があるので、設定とかはasdf公式が参考になるかも

- [rtx](https://github.com/jdx/rtx)
- [asdf configuration](https://asdf-vm.com/manage/configuration.html)

## git
brew導入した際にgitも一緒に入ってくるが、それとは別にbrew管理下にあるgitを基本的に使用する

## docker
brewコマンドでDocker Desktop for Macを入れるには `--cask`オプションが必要  
入れないとcliしか入ってこない

```
brew install --cask docker
```

## direnv
- [direnv](https://github.com/direnv/direnv)