---
layout: post
title: 「ドメイン駆動設計 本格入門」に参加してきた感想
tags: 
- study-session-review
---

[[DevLOVE Premium第3回]ドメイン駆動設計 本格入門](https://devlove.doorkeeper.jp/study-session/85247)に参加してきました。

講演形式でも直接お話を聞けると、話し手が強調していることをよりはっきりと受け取ることができて印象的です。このような勉強会には何度か参加していますが、その度に新しい気づきがあります。

<iframe src="//www.slideshare.net/slideshow/embed_code/key/DTt0qFQGcEy3Id" width="595" height="485" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe> <div style="margin-bottom:5px"> <strong> <a href="//www.slideshare.net/masuda220/ss-137608652" title="ドメイン駆動設計本格入門" target="_blank">ドメイン駆動設計本格入門</a> </strong> from <strong><a href="https://www.slideshare.net/masuda220" target="_blank">増田 亨</a></strong> </div>

今回の内容は特に「区分」にフォーカスを当てていたように感じました。まず、**ビジネスルールこそ複雑さの根源であり立ち向かうべきもの**、としたうえで、区分による条件や分岐が特に複雑であると紹介されていました。

業務アプリケーションは、数学的なロジックが求められる難解さよりも、条件や分岐で入り組んだり散らばったりしてしまいがちです。フレームワークを使いこなしてもビジネスルールの複雑さを解消できるわけではないのですが、それについても言及されていました。フレームワークなどのアーキテクチャ論は準備だということです。

> ビジネスルールの記述を独立したモジュールに分離する

アーキテクチャはそのための準備だということですね。同様に、エンティティやリポジトリなどの要素もその前の基本事項であり、エヴァンス本は第3部からが本番だとのこと。読み直してみよう。

ところでエヴァンス本という呼び方には市民権があるのですね。すると実践～はヴァーノン本？？

**エンティティよりも値オブジェクトが主役**、オブジェクト指向とは型指向のプログラミング。というのはこれまでも言われていたことですが、ますます強調してきているなと感じます。ファクト・ルール・ゴール、という整理の仕方もビジネスルールの輪郭を際立たせるものとして理解しておきたいところです。

----

と、私が受けた印象を書き綴ってみました。参加された他の方はまた違った印象を受けたかもしれません。あるいは増田さんの意図とも違っているかもしれません。が、それはそれでよいのです。また見返したりお話を聞いたりしたときにはさらに違っているでしょうから。

オブジェクト指向ってなんだっけ？から始まって、ドメイン駆動設計を知ってそれから追いかけてきていますが、勉強することはまるで尽きないなと感じます。プログラマーは常に勉強し続けないといけない云々なんてことが言われますが、そんなに悲観することではないです。むしろいつだって勉強し始めることができるってことだし、変に焦るよりもこれは楽しいことだって思いたいですね。

<iframe style="width:120px;height:240px;" marginwidth="0" marginheight="0" scrolling="no" frameborder="0" src="//rcm-fe.amazon-adsystem.com/e/cm?lt1=_blank&bc1=000000&IS2=1&bg1=FFFFFF&fc1=000000&lc1=0000FF&t=fukuchiharuki-22&language=ja_JP&o=9&p=8&l=as4&m=amazon&f=ifr&ref=as_ss_li_til&asins=477419087X&linkId=1138f4a407e0e2d334ddfb74be975a0b"></iframe>