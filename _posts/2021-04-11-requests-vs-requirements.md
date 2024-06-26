---
layout: post
title: 要望と要求と要件の違い
redirect_from:
  - /entry/form-of-request-and-requirement
---

要望と要求と要件の違いは何でしょうか。

要望と要求と要件、その関係を調べるとベン図を用いた説明を目にすることがあります。この図では要望が最も広く、その中に要求があり、さらにその中に要件があります。要件は要求の、要求は要望のサブセットというわけです。

![ベン図で表される関係](../images/2021-04-11/figure-1.png)

このベン図は要望と要求と要件の関係をよく表しているでしょうか？……要望と要求と要件とは何か、それらの違いはどこにあるのかを改めて考えてみましょう。

# 機能一覧は要件定義か

「こんな機能がほしい」、利用者の声を集めた機能一覧を一度は見たことがあるのではないでしょうか。あるシステムをリニューアルすべく打合せをしているとします。現行システムにはもちろん利用者がいます。そこで利用者から声が集められます。システムは自動化が行き届いていないために運用の手間がかかるとのこと。

この機能一覧を元に要件が定められていきます。機能一覧には優先度を示す列が設けられており、どの機能が特に求められているかランクで分かるようになっています。さて、それでは優先度の高い機能から実装していくことにしましょう。そんなふうに打合せは進められていきます。

この議論の進め方には違和感があります。ユーザーの声を集めた機能一覧からピックアップして実装していくだけのやり方では、「それで何がどうなるのか」が見えてきません。それぞれの機能をとりあげればなるほど便利そうです。機能ひとつひとつはおかしなことを言っているわけではないのです。しかし、それらの機能を実現したときの、システムの姿が見えてきません。

**そのシステムを含めた利用者を取り巻く環境がどうなるか**を想像したでしょうか。それらの機能を実装していくことはきっとできます。実装するとどうなるのか。そのシステムをリリースすることはできるかもしれません。リリースするとどうなるのか。それでシステムをリニューアルしたことになるのでしょうか。

システムをリリースした先に何を見るのか、その姿を描くものが必要です。リリースをゴールにすれば、やってやれないことはないでしょう。しかし、やったところで何をしたことになるかを明言できるでしょうか。明言できない、というよりは、存在していないのかもしれません。

# システムの姿を定義する

システムの姿を描いていなければ、優先度の高い機能を実装していったとしてもリニューアルを完成させられたとは言えないでしょう。具体的な姿を想像することなしに目標を設定できるとは思えません。目標を定めるからプロジェクトです。要件は達成すべき目標です。機能一覧を"舐めていく"やり方では要件を導くことはできないでしょう。

ベン図が表す要望と要求と要件の関係は間違いで、別の形で表現されるべき関係があるのかもしれません。"要件は要求の、要求は要望のサブセット"、これは思い込みなだけで実はまったく現実に即していません。優先度の高い機能を挙げていってもシステムの姿を定義できないことは容易に想像できます。利用者の声をそのまま要件にするのは安易というものです。

![課題と解決](../images/2021-04-11/figure-2.png)

システムの姿を描くことは目標の設定につながります。要件の定義とはシステムの姿の定義だと言えそうです。利用者の声を集めることが間違いだと言いたいわけではありません。要望や要求の整理は課題を理解するために必要な過程です。その解決の形である要件は要望や要求から飛躍するのかもしれません。

# 要件は要望や要求から飛躍する

システムには利用者がいて、システムと利用者との間には関係が存在します。
解決策としてシステムが存在するとき、課題をもった利用者が対で存在します。要件がシステムの姿で、利用者の声と切り離された定義なら、システムの姿と切り離された、利用者の声としての定義があってもよさそうです。そこで、要望と要求と要件の関係を次の絵に当てはめてみます。

![利用者の声とシステムの姿](../images/2021-04-11/figure-3.png)

たとえば、利用者の作業において工数を削減したいとする利用者の望み、これを要望とします。利用者が「受注作業の工数を削減したい」と考えているとします。工数削減したい対象の受注作業がシステムを用いるなら、暗黙にシステムに期待していることがあるかもしれません。しかし、工数削減そのものはシステムに向けた声ではありません。

利用者がシステム（の開発者）にこうあってほしいと求める声、これを要求とします。利用者は受注作業に目視を伴う転記や手計算が含まれていることに気がつきます。そしてこれらが受注作業の工数を引き上げていると考えたとします。利用者は「受注作業の一部を自動化したい」と言うでしょう。「工数削減」に対して「自動化」はシステムに向けられています。

システムおよび、そのシステムを含めた利用者を取り巻く環境をこのようにしようとする定義、これを要件とします。開発者は利用者の声をそのまま実現するとは限りません。開発者は「作業工数を削減するために一部作業を自動化したい」とする声を受けて考えます。システムがどうあるべきか。システムとの作用の中にある利用者を想像します。システムの次の姿を描くと、最後に開発者は「承認プロセスを省いた作業フロー」を提案します（！？）。

---

要件とはシステムの姿を描いた定義であると考えると、要件の定義はもっと能動的な活動であるべきだと分かります。優先度の高い機能をただ実装していくような受け身の活動ではありません。要件は要望や要求からある意味で切り離されていると考えられます。開発者は利用者の声に従うのではなく、自発的にシステムの姿を描くべきでしょう。ただし、開発者が自発的にシステムの姿を描くには利用者の声・課題を理解する必要があります。利用者が何を望みシステムに何を求めているか。これを理解してはじめてシステムの姿を思い描くことができます。

![要望と要求と要件の新しいかたち](../images/2021-04-11/figure-4.png)

ベン図で表す要望と要求と要件の関係を考え直してみました。利用者の望みとしての要望、システムに向けられた要求、システムの姿としての要件がある。そんな関係を考えてみました。要望と要求の発信元は利用者ですが、要件の発信元は開発者です。要望と要求は分析で、要件は設計であるとも捉えられそうです。なので、要件は要望と要求から飛躍し得ると考えられます。そして、要件を定める活動は自発的で能動的です。要件としてシステムの姿を描く。それがシステムをデザインする活動なのだと思います。
