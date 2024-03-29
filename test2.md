# goenvを使用したGoのインスールの手順

goenv は Golang のバージョン管理ツールです。  

[Go言語とは](https://hnavi.co.jp/knowledge/blog/go/)  
<br>

### 実行環境
macOS Venture 13.2.1 (22D68)  
ターミナルで使用するシェルはzsh  

### goenvのインストール

1. ターミナルを開く
2. 以下のコマンドを実行する

```
git clone https://github.com/syndbg/goenv.git ~/.goenv
```
```
brew install goenv
```

3. goenvの設定を`.zshrc`ファイルに追加する

```
vi -/ .zshrc
```


4. ファイルが開いたら以下手順を実行する。<br>
Shift+Gを押下する。  
oを押下する。  
Enterを押下する。  
以下の行をコピーして貼り付ける。
```
export GOENV_ROOT="$HOME/.goenv"
export PATH="$GOENV_ROOT/bin:$PATH"
eval "$(goenv init - zsh)"
```

5. 変更を保存する。
```
:wq!
```

7. 変更を反映させるために、以下のコマンドを使用して.zshrcを再読み込みする。
 ```
 source -/.zshrc
 ```
8. 以下コマンドを実行し、インストール可能なバージョンを確認する。

（最新のバージョンが表示されていることを確認）
```
goenv install --list
```

9. 最新バージョンのGoをインストールする。
```
goenv install $(goenv install --list | tail -n 1)
```
10. 最新の1つ前のバージョンのGoをインストールする。
```
goenv install $(goenv install --list | tail -n 2 |head -n 1)
```

11. インストール済みのgoのversionを確認する。
```
goenv versions
```


