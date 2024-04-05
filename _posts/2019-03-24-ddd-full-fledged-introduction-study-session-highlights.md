---
layout: post
title: 【ドメイン駆動設計 本格入門】ハイライトと感想
redirect_from:
  - /entry/ddd-full-fledged-introduction
---

[[DevLOVE Premium第3回]ドメイン駆動設計 本格入門](https://devlove.doorkeeper.jp/study-session/85247)に参加してきました。

このような勉強会には何度か参加していますが、その度に新しい気づきがあっておもしろいです。講演形式でも直接お話を聞くと、話し手が強調していることをよりはっきりと受け取ることができて印象的です。

<iframe src="//www.slideshare.net/slideshow/embed_code/key/DTt0qFQGcEy3Id" width="595" height="485" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe> <div style="margin-bottom:5px"> <strong> <a href="//www.slideshare.net/masuda220/ss-137608652" title="ドメイン駆動設計本格入門" target="_blank">ドメイン駆動設計本格入門</a> </strong> from <strong><a href="https://www.slideshare.net/masuda220" target="_blank">増田 亨</a></strong> </div>

今回の内容は特に「区分」にフォーカスを当てていたように感じました。まず、**ビジネスルールこそ複雑さの根源であり立ち向かうべきもの**、としたうえで、区分による条件や分岐が特に複雑であると紹介されていました。

業務アプリケーションは、数学的なロジックが求められる難解さよりも、条件や分岐で入り組んだり散らばったりしてしまいがちです。フレームワークを使いこなしてもビジネスルールの複雑さを解消できるわけではないのですが、それについても言及されていました。フレームワークなどのアーキテクチャ論は準備だということです。

> ビジネスルールの記述を独立したモジュールに分離する

アーキテクチャはそのための準備だということですね。同様に、エンティティやリポジトリなどの要素もその前の基本事項であり、エヴァンス本は第3部からが本番だとのこと。読み直してみよう。ところでエヴァンス本という呼び方には市民権があるのですね。すると実践～はヴァーノン本ということに？？

**エンティティよりも値オブジェクトが主役**、オブジェクト指向とは型指向のプログラミング。というのはこれまでも講演者が主張していたことですが、ますます強調してきているなと感じます。ファクト・ルール・ゴール、という整理の仕方もビジネスルールの輪郭を際立たせるものとして理解しておきたいところです。

---

オブジェクト指向ってなんだっけ？に始まって、ドメイン駆動設計を知ってから追いかけてきていますが、勉強することはまるで尽きないなと感じます。プログラマーは常に勉強し続けないといけない云々なんてことが言われますが、そんなに悲観することではないです。むしろいつだって勉強し始めることができるってことだし、変に焦るよりもこれは楽しいことだって思いたいですね。

# アソシエイトリンク

- [現場で役立つシステム設計の原則 ~変更を楽で安全にするオブジェクト指向の実践技法 単行本（ソフトカバー）](https://www.amazon.co.jp/%E7%8F%BE%E5%A0%B4%E3%81%A7%E5%BD%B9%E7%AB%8B%E3%81%A4%E3%82%B7%E3%82%B9%E3%83%86%E3%83%A0%E8%A8%AD%E8%A8%88%E3%81%AE%E5%8E%9F%E5%89%87-%E5%A4%89%E6%9B%B4%E3%82%92%E6%A5%BD%E3%81%A7%E5%AE%89%E5%85%A8%E3%81%AB%E3%81%99%E3%82%8B%E3%82%AA%E3%83%96%E3%82%B8%E3%82%A7%E3%82%AF%E3%83%88%E6%8C%87%E5%90%91%E3%81%AE%E5%AE%9F%E8%B7%B5%E6%8A%80%E6%B3%95-%E5%A2%97%E7%94%B0-%E4%BA%A8/dp/477419087X?__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&crid=3LN0AA6JIJUCZ&dib=eyJ2IjoiMSJ9.Gd-KflCL_WLCWrS1RIMV4A.JhyGWYMUlgjxGAOhPdQrwWM0igfXQNfHk7vd6QH4OdQ&dib_tag=se&keywords=477419087X&qid=1705678593&sprefix=477419087x%2Caps%2C195&sr=8-1&linkCode=ll1&tag=fukuchiharuki-22&linkId=5d3e5d453ad7050de2d31240463c3dd8&language=ja_JP&ref_=as_li_ss_tl)
- [エリック・エヴァンスのドメイン駆動設計: ソフトウェアの核心にある複雑さに立ち向かう 単行本](https://www.amazon.co.jp/%E3%82%A8%E3%83%AA%E3%83%83%E3%82%AF%E3%83%BB%E3%82%A8%E3%83%B4%E3%82%A1%E3%83%B3%E3%82%B9%E3%81%AE%E3%83%89%E3%83%A1%E3%82%A4%E3%83%B3%E9%A7%86%E5%8B%95%E8%A8%AD%E8%A8%88-Architects%E2%80%99Archive-%E3%82%BD%E3%83%95%E3%83%88%E3%82%A6%E3%82%A7%E3%82%A2%E9%96%8B%E7%99%BA%E3%81%AE%E5%AE%9F%E8%B7%B5-%E3%82%A8%E3%83%AA%E3%83%83%E3%82%AF%E3%83%BB%E3%82%A8%E3%83%B4%E3%82%A1%E3%83%B3%E3%82%B9/dp/4798121967?_encoding=UTF8&dib_tag=se&dib=eyJ2IjoiMSJ9.QVYIYI5g6MsJJmFhmLMzbg.5fQyzKM663QV7UU-pRqz6d34w0t3xNjfhcDkbvnZ8Nc&qid=1705678642&sr=8-1&linkCode=ll1&tag=fukuchiharuki-22&linkId=88d6499e2585d963267e63dec60d1eee&language=ja_JP&ref_=as_li_ss_tl)
- [実践ドメイン駆動設計 単行本（ソフトカバー）](https://www.amazon.co.jp/%E5%AE%9F%E8%B7%B5%E3%83%89%E3%83%A1%E3%82%A4%E3%83%B3%E9%A7%86%E5%8B%95%E8%A8%AD%E8%A8%88-Object-Oriented-SELECTION-%E3%83%B4%E3%82%A1%E3%83%BC%E3%83%B3%E3%83%BB%E3%83%B4%E3%82%A1%E3%83%BC%E3%83%8E%E3%83%B3/dp/479813161X?__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&crid=37FZ9H5359DVX&dib=eyJ2IjoiMSJ9.1_8ajliR_YewOi4HCxjArQ.NMINaX63pA09xceFqg-qkaPCYOpAWpN30-ouTdXVO4w&dib_tag=se&keywords=479813161X&qid=1705678726&sprefix=%E3%82%A8%E3%83%AA%E3%83%83%E3%82%AF+%E3%82%A8%E3%83%B4%E3%82%A1%E3%83%B3%E3%82%B9%E3%81%AE%E3%83%89%E3%83%A1%E3%82%A4%E3%83%B3%E9%A7%86%E5%8B%95%E8%A8%AD%E8%A8%88+%E3%82%BD%E3%83%95%E3%83%88%E3%82%A6%E3%82%A7%E3%82%A2%E3%81%AE%E6%A0%B8%E5%BF%83%E3%81%AB%E3%81%82%E3%82%8B%E8%A4%87%E9%9B%91%E3%81%95%E3%81%AB%E7%AB%8B%E3%81%A1%E5%90%91%E3%81%8B%E3%81%86+%E5%8D%98%E8%A1%8C%E6%9C%AC%2Caps%2C384&sr=8-1&linkCode=ll1&tag=fukuchiharuki-22&linkId=cbea299b7bfc4ddac1b926e166626b32&language=ja_JP&ref_=as_li_ss_tl)
