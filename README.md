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
# Repositoryの.tmux.conf.localをそのまま利用する or 直接書き換える場合
$ ln -s ~/.tmux.conf.customization/.tmux.conf.local ~/
# .tmux.conf.localをコピーして編集する場合
$ cp ~/.tmux.conf.customization/.tmux.conf.local ~/
# scriptsをPATHに追加（bashの場合）
$ echo '
if [[ -d $HOME/.tmux.conf.customization/scripts ]]; then
    export PATH="$PATH":"$HOME/.tmux.conf.customization/scripts"
fi
' >> ~/.bashrc
# scriptsをPATHに追加（zshの場合）
$ echo '
if [[ -d $HOME/.tmux.conf.customization/scripts ]]; then
    export PATH="$PATH":"$HOME/.tmux.conf.customization/scripts"
fi
' >> ~/.zshrc
```

このレポジトリの[.tmux.conf.local](https://github.com/figmentum/.tmux.conf.customization/blob/master/.tmux.conf.local)と元の[.tmux.conf.local](https://github.com/gpakosz/.tmux/blob/master/.tmux.conf.local)とを比較すれば変更点が確認出来る。
[scripts](https://github.com/figmentum/.tmux.conf.customization/tree/master/scripts)以下にtmuxのステータスバー表示用のスクリプト群が入っている。

## 制限事項
* 基本的にzshとの組み合わせでの動作を想定
* byobuのキーバインドを真似ているが、再現度は高くない
* tmux初心者（ペイン分割は滅多にせず、タブとセッション保持程度にしか使っていない）の設定のため、間違いや不適切な設定がいくつも含まれている可能性あり
* 自分以外が使うことを想定していないため、手元で動いているように見えること以上の検証はしていない

## License
* .tmux.conf.customization/.tmux.conf.local
  * Original author: Gregory Pakosz (@gpakosz). Dual licensed under the WTFPL v2 license and the MIT license.
  * Author of modification: figmentum (https://siesta.pm). Licensed under MIT license.
* Files in sciprt/ directory
  * Author: figmentum (https://siesta.pm). Licensed under MIT license.
