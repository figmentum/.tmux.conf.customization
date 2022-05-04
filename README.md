# .tmux.conf.customization

## これは何？
 * [gpakosz/.tmux](https://github.com/gpakosz/.tmux)をベースにbyobu風のキーバインドを設定するなどカスタマイズしたもの
 * 随時アップデート予定
 * あくまで自分用

## 使い方
[gpakosz/.tmux](https://github.com/gpakosz/.tmux)をgit cloneしたうえで、このレポジトリの[.tmux.conf.local](https://github.com/figmentum/.tmux.conf.customization/blob/master/.tmux.conf.local)でカスタマイズ部分を適用する。


```
$ cd ~
$ git clone https://github.com/gpakosz/.tmux.git
$ ln -s -f .tmux/.tmux.conf
$ git clone https://github.com/figmentum/.tmux.conf.customization.git
$ ln -s ~/.tmux.conf.customization/.tmux.conf.local ~/
```

このレポジトリの[.tmux.conf.local](https://github.com/figmentum/.tmux.conf.customization/blob/master/.tmux.conf.local)と元の[.tmux.conf.local](https://github.com/gpakosz/.tmux/blob/master/.tmux.conf.local)とを比較すれば変更点が確認出来る。
[scripts](https://github.com/figmentum/.tmux.conf.customization/tree/master/scripts)以下にtmuxのステータスバー表示用のスクリプト群が入っている。

## 制限事項
* 基本的にzshとの組み合わせでの動作を想定
* byobuのキーバインドを真似ているが、再現度は高くない
* tmux初心者（ペイン分割は滅多にせず、タブとセッション保持程度にしか使っていない）の設定のため、間違いや不適切な設定がいくつも含まれている可能性あり
* 自分以外が使うことを想定していないため、手元で動いているように見えること以上の検証はしていない
