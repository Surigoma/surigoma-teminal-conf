# surigoma-terminal-conf
ただただターミナル操作でカラフルにするだけの設定群  
各鯖で表示を同期するためのやつだから勝手にforkして編集してもOK  
いんたーねっつからコピペしまくってるのでどっから持ってきたかもわからないぬるい仕様  

#Apps
- zsh
- vim
- byobu(Backend is tmux)

# Vimが文字化ける
power-line導入してるからググッてteratermとかputtyに適応してください。
(フォントファイルを上げると著作権違反になる)

# byobuのロゴ消し
勝手にスクロールしちゃったりなんだかんだめんどくさい  
### とりあえずロゴいらん  
  [.byobu/status @32行目](https://github.com/Surigoma/surigoma-teminal-conf/blob/master/.byobu/status#L32)  
  tmux_left="logo → tmux_left="#logo  
### ロゴ表示したいけどどうにかしたい
  環境によるかもだけど  
  [/usr/lib/byobu/logo @40行目](https://github.com/dustinkirkland/byobu/blob/master/usr/lib/byobu/logo#L40)  
  printf " u□ "; → printf " U ";
### コンフィグ以外のところを弄りたくない
  ただし、色はつかない  
  (エスケープシーケンスとか頑張ったけどつけられなかった)  
  [.byobu/statusrc @32行目](https://github.com/Surigoma/surigoma-teminal-conf/blob/master/.byobu/statusrc#L32)  
  #LOGO="\o/" → LOGO=" U "  

#多分参照元(Thanks)
- http://d.hatena.ne.jp/oovu70/20120405/p1
- http://vimvim-beginner.tumblr.com/post/95719664644/vimneobundle%E3%81%A7%E3%83%97%E3%83%A9%E3%82%B0%E3%82%A4%E3%83%B3%E7%AE%A1%E7%90%86%E3%82%92%E7%B0%A1%E5%8D%98%E3%81%AB%E3%81%99%E3%82%8B%E6%96%B9%E6%B3%95
