# Fishのインストールメモ

## 再セットアップ時
- fishインストール
- フォントインストール
- fisherインストール
- コンフィグファイル設置(シンボリックリンク)

## コンフィグファイルの位置
`~/.config/fish/conf.d`

## Fishインストール
brewがインストールされている前提
```
brew install fish
```

`/usr/local/bin/fish`を追加
```
sudo vi /etc/shells
```

デフォルトシェルを変更
```
chsh -s /usr/local/bin/fish
```

## Fisherをインストール
https://github.com/jorgebucaran/fisher  
`curl -sL https://git.io/fisher | source && fisher install jorgebucaran/fisher`

## Fisherの基本
### インストール
`fisher install {GitUser名}/{リポジトリ名}`
### アンインストール
`fisher rm {GitUser名}/{リポジトリ名}`

## Themeの変更
Themeの一覧は[ここ](https://github.com/oh-my-fish/oh-my-fish/blob/master/docs/Themes.md)

Powerlineの導入
```
fisher install oh-my-fish/theme-bobthefish
```

## Powerline用のフォント
[ここ]()のリポジトリをクローンして`install.sh`を実行

## コンフィグファイル群をgit管理下にする
configフォルダの実体をgit管理下に置き、fishのコンフィグフォルダをシンボリックリンクで配置する

移動
```
mv ~/.config/fish/{configfile}
```

シンボリックリンク(.config/fishディレクトリです)
```
ln -s fish/config/{configfile}
```
