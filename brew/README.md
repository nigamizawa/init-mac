# brew

Brewfileを正とし、Brewfileに記載されていないものは定期的に削除する。  
必要なものはちゃんとBrewfileに記載しよう！

## commands

Write all installed casks/formulae/images/taps into a Brewfile in the current directory.
```
brew bundle dump
brew bundle dump --file ${file}
brew bundle dump --cask #casks only
```

Install packages from the Brewfile.
```
brew bundle 
```


Check if all dependencies are installed from the Brewfile.
```
brew bundle check
```


Uninstall all dependencies not listed from the Brewfile.
```
brew bundle cleanup
```

## パッケージについて
よく使い方忘れるやつとか以下にメモを記載していく

- [パッケージ一覧](./doc/packages.md)


## initelプロセッサでしか動作しないAppについて

brewで諸々を管理する際、initelプロセッサでしか動作しないアプリケーションのことを考慮する必要がある。  
[Rosetta](https://support.apple.com/ja-jp/HT211861)を利用することでApple Siliconでもintel用のAppを動作させることができる。  
しかし、brewでこれらのAppを管理する場合、公式での手順通りに管理すると混在し扱いが煩雑になってしまうので、
アーキテクチャごとに別々のbrewを管理する手法を取るとする。  

### 各種パス
- arm64e(AppleSilicon) -> /opt/homebrew/bin/brew
- x86_64(intel)        -> /usr/local/bin/brew


### 設定サンプル

```zsh:~/.zprofile
ARCH=$(uname -m)
if [[ $ARCH == arm64 ]]; then
    echo "Current Architecture: $ARCH"
	eval $(/opt/homebrew/bin/brew shellenv)
elif [[ $ARCH == x86_64 ]]; then
    echo "Current Architecture: $ARCH"
	eval $(/usr/local/bin/brew shellenv)
fi
```

### ref
https://zenn.dev/junjunjunk/articles/4b230519d87de4

