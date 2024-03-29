# goenvを使用したGoのインスールのしかた

[Go言語とは](https://hnavi.co.jp/knowledge/blog/go/)



### 実行環境
macOS Venture 13.2.1 (22D68)  
※ターミナルで使用するシェルはzsh  

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


4. ファイルが開いたら以下の行を追加する
```
export GOENV_ROOT="$HOME/.goenv"
export PATH="$GOENV_ROOT/bin:$PATH"
eval "$(goenv init - zsh)"
```

5. 変更を保存する
`:wq!`

6. 




