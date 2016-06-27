---
title: すんませんVrapperなめてました
tags: プログラミング, Vim
---
# すんませんVrapperなめてましたの話

* * *

## Vrapperとは
Java, C/C++, Python, etc用統合開発環境(IDE)であるEclipseの中の
組み込みエディタで**Vimと同じ操作を可能とするものである。**


* Vrapperを使う理由
    - EclipseでVimを使えるのなら、**もう何も怖くない**



### Vrapperをなめていた理由
+ 「Vrapper使ってみたけど、あくまでVim風の操作を提供するだけでvimrc読み込めないじゃーん。 自分好みの操作を定義できないじゃーん」


### 悔い改め
+ 「Vrapperって、Vrapper用の設定ファイルをvimrcと同じように書けたのですねっ！？！？ すみませんでしたっ！！」


# 使う手順

## まずVrapper入れる

Eclipse開く ---> Help > Install New Software >  

それっぽいところに入力してAdd  
Work with: [http://vrapper.sourceforge.net/update-site/stable](http://vrapper.sourceforge.net/update-site/stable)  

これ入れる。  
流れに乗る。(インストールしていく)  


## EclipseのVimっぽい操作に競合するキーバインドを破壊する

Window > Preferences > General > Keys  
だいたいCtrl+(hoge)系が競合するので削除削除サクジョォォォォ！！！

* 削除したのはだいたいこんなん
    - Ctrl+F
    - Ctrl+B
    - Ctrl+N
    - Ctrl+P
    - Ctrl+I
    - Ctrl+J
    - Ctrl+W
    - Ctrl+V
    - Ctrl+C ( 僕の場合後で<Esc>にマップしたいからっ )
    - Ctrl+A
    - Ctrl+X

これらを画面下部にある[Unbind Command]でアンバインド。


## 悔い改める ( Vrapperの設定ファイルを書く )

ホームディレクトリに.vrapperrcというファイルを書けば
勝手にEclipse起動時に読み込んでくれます。
すごい、benri-。

* * *

こんなん

```vim
nnoremap <Up>    <NOP>
nnoremap <Down>  <NOP>
nnoremap <Left>  <NOP>
nnoremap <Right> <NOP>
inoremap <Up>    <NOP>
inoremap <Down>  <NOP>
inoremap <Left>  <NOP>
inoremap <Right> <NOP>
cnoremap <Left>  <NOP>
cnoremap <Right> <NOP>

nmap     <C-j> <CR>
imap     <C-j> <CR>

cnoremap <C-b> <Left>
cnoremap <C-f> <Right>
cnoremap <C-a> <Home>
cnoremap <C-h> <Backspace>
cnoremap <C-d> <Del>
cnoremap <C-e> <End>

inoremap <C-l> <Esc>
vnoremap <C-l> <Esc>
cnoremap <C-l> <Esc>

inoremap <C-k><C-l> <Esc>
```

***Eclipseが来た***  