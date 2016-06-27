---
title: 自称Javaristaの僕がいかにしてHaskellに触れて純粋になったか
tags: ポエム, Haskell
---
2014-12-24

# 自称Javaristaの僕がいかにしてHaskellに触れて純粋になったか

　話をしよう、あれは今から…36万…あー…いつだったか。  
最初にHaskellに触れた時は…確かー…1万…まぁいい。  
君たちは純粋関数に…まぁいいや。  
…  
…  
　そうそう、思い出した。  
僕が初めてHaskellに触れたのは、今から約1年前くらいのことだった。  
今日はその話をしようと思う。  


- - -

## 第一章「お前にHello,world!! お前にHello,world!!」

　まず最初にHaskellに触れた時、果敢にも…いえ、無謀にも僕は書籍を持たずに入門しようとしました。  
そしてもっとも最初に目に触れたコードがこれ。

    main = putStrLn "Hello, World!"

「普通の出力だ、簡単だ」  
そう思ったのは間違いでした。


- - -

## 第二章「ようこそ我が胎内へ」

```haskell
Prelude> let fac n = if n == 0 then 1 else n * fac (n-1)
```

「！？？ ！？！？」

```haskell
Prelude> fac 42
1405006117752879898543142606244511569936384000000000
```

「！？！？！？ 長…数字が長…too long suuji!!!？？？！？」

```haskell
fac 0 = 1
fac n = n * fac (n-1)
main = print (fac 42)
```

ここで僕はHaskellをやめました。  
バイバイHaskellまた次の時空で。  


しかし僕は決してHaskellを手放さなかったのでした…。  


- - -

## 第三章「もう何も怖くない」

「お前にHello,world!! お前にHello,world!!」  

　そんな言葉が脳内に響き渡る。  
そう、これは今思えば。  
これこそが、僕の中に覚醒したHaskell Curryの紋章の声だったんだっ！！  


　僕が「すごいHaskellたのしく学ぼう！」を手に入れたのはそんな時でした。  
「すごいHaskellたのしく学ぼう！」、通称「すごいH本」。  
英語で言うと「Great-H-Book」。  
[すごいH本](http://www.amazon.co.jp/%E3%81%99%E3%81%94%E3%81%84Haskell%E3%81%9F%E3%81%AE%E3%81%97%E3%81%8F%E5%AD%A6%E3%81%BC%E3%81%86-Miran-Lipova%C4%8Da/dp/4274068854)

　これにはprintという名の鈍器はありませんでした。  
もちろん「名状し難いprintのようなもの」も登場しません。 ( 最初の方は )  

　僕はこの魔本を手にし、Haskellの地を歩いていくことにしました。  


- - -

## 第四章「お待ちなさい、モナドが曲がっていてよ」

　その後僕は魔法にかけられたかのようにHaskellを楽しんでいた。  
カリー様がみてる。  

　まず最初に苦しんだのが再帰。  
元々命令型言語でも再帰はよくわからなかったし、そもそもあんまり使わなかった。  
でもHaskellでは必須！ なぜならカリー様がみてるからっ！！  

　その後、型についてはとりあえずある程度の理解を得たと思うの。  
しかしファンクタ、アプリカティブ、…Monad。
僕はここでまたしも倒れたのだった。   
( 満身創痍になってすごいH本を読みきりました。 最終理解レベルは多分高くはなかった。 )  

\*\*__おおモノイドインスタンスよ、しんでしまうとはなさけない__\*\*  


- - -

## 第五章「そして全てがモノイドになった」

　次に今から4ヶ月前くらいとかからは型について日常的に考えるようになりました。  
ついったーでは、某氏に__圏論カウンセラー__などをしてもらったりしましたっ！  
そこらへんはちょっととげったーにまとめたりもしました。  

うん、おそらくそこからでしょう。  
型を日常的に考察するようになったのは。  

__型々カタカタ__  
__ラムダケイサンはとくにないけれど、オオゲサなタイプ片手にここでイッタン停止☆__


- - -

## 第六章「 僕『お前にHello,world!! お前にHello,world!!』 」

　周りの人にHaskellを布教しないと気が済まない不治の病にかかりました。  
僕の取扱いには気をつけましょう。  


- - -

## 第七章「俺、カリーハスケルになります。」

　とりあえず~~ハスケルギアを手にしたのでモナドを侵略したいとおもいま~~気のせいでした。  

　Haskellに関して ( とりわけモナドやファンクタ(関手)に対しては特に ) SlideShareなどで  
おもしろおかしく情報を取り入れ始めたのはこの頃からです。  
とりあえず今から1ヶ月前くらいからかな。 もっと前？  


- - -

## 第八章「台無しだと言っているのよ…」

　今は[Haskellの薄い本](http://www.amazon.co.jp/%E3%83%97%E3%83%AD%E3%82%B0%E3%83%A9%E3%83%9F%E3%83%B3%E3%82%B0Haskell-Graham-Hutton/dp/4274067815)を読んでいます。  
今になってやっとわかる内容なので、

* Haskellを独学で始めようとする                      ->
* すごいH本を読む                                    ->
* すごいH本を満身創痍でなんとか頭に入れて読み終わる  ->
* 型に興味があります！！                             ->
* モナドは単なる自己関手の圏におけるモノイド対象だよ ->
* Haskellの薄い本読む

というプロセスを踏んで本当によかったと思いますっ！  
[こんなの](http://www.slideshare.net/YoichiroIshikawa/haskelljavavim-script)も書きました、発表しました。  
2時間以上ぶっ続けで話すのは初めてだったと思います。  


- - -
## 最終章「だけどね、だれが、どこで死ぬかなんて、私にはわからなかったのよ。」
　この記事は誰に対してのなにだよこのっ！！！！  
もう寝る。
  
  
  
__終わり__
  
  
  