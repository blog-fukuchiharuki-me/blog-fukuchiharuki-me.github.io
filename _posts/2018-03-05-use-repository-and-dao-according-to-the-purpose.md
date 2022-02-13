---
layout: post
title: リポジトリとDAOの違い
tags: 
- software-design
---

リポジトリとDAOは似ています。どちらもデータストアとアプリケーションコードの間に位置します。しかしリポジトリとDAOにはやはりどこか違いがありそうです。

リポジトリとDAOの違いはどこにあるのか、参考文献からそれぞれの目的を調べてみます。また具体的にリポジトリとDAOをどう使い分けられそうかを考えてみます。

# リポジトリはドメインオブジェクトのコレクション

> A Repository mediates between the domain and data mapping layers, acting like an in-memory domain object collection.   
-- [P of EAA: Repository](https://martinfowler.com/eaaCatalog/repository.html)

リポジトリはエンタープライズアプリケーションアーキテクチャパターンにおいて次のように説明されています。リポジトリはドメインとデータマッピングレイヤをとりなして、**インメモリなドメインオブジェクトのコレクション**のように振る舞います。

> Conceptually, a Repository encapsulates the set of objects persisted in a data store and the operations performed over them, [...]  
-- [P of EAA: Repository](https://martinfowler.com/eaaCatalog/repository.html)

リポジトリはドメインオブジェクトの永続化に関わる操作を隠蔽しているとも言えます。

> [...]それ自体はドメインに由来しないが、ドメイン設計においては意味のある役割を持っている。これらの構成概念は、モデルオブジェクトを操作できるようにすることで、[...]  
-- エリック・エヴァンスのドメイン駆動設計

また、エリック・エヴァンスのドメイン駆動設計において次のように説明されています。リポジトリの目的はドメインオブジェクトを操作できるようにすることです。リポジトリそのものはモデルとは呼ばないようです。

# DAOはデータアクセスのメカニズムを隠蔽する

> separates a data resource&#39;s client interface from its data access mechanisms  
-- [Design Patterns: Data Access Object](https://www.oracle.com/java/technologies/data-access-object.html)

DAOはデザインパターンのひとつです。DAOはデータリソースのクライアントインタフェースをデータアクセスのメカニズムから分離します。**データアクセスのメカニズムを隠蔽**する点はリポジトリと一致しています。

> The DAO pattern allows data access mechanisms to change independently of the code that uses the data.  
-- [Design Patterns: Data Access Object](https://www.oracle.com/java/technologies/data-access-object.html)

DAOの目的はデータを利用するコードから独立してデータアクスのメカニズムを変更できるようにすることです。

# 一致する点と相違する点

リポジトリとDAOはデータアクセスに関わるメカニズムを隠蔽する点で一致しています。

リポジトリとDAOの違いはその目的にあります。リポジトリの目的はアプリケーションコードがドメインオブジェクトを操作できるようにすることです。一方で、DAOの目的はアプリケーションコードから独立してデータアクセスのメカニズムを変更できるようにすることです。

つまり、リポジトリとDAOはデータストアとアプリケーションコードの間に位置する点で一致していますが、関心の向きに違いがあると言えそうです。リポジトリの関心はドメインオブジェクトにあり、DAOの関心はデータアクセスのメカニズムにあります。

# リポジトリとDAOの使い分け方

さて、リポジトリとDAOをどう使い分けられるかを考えてみます。

まず、JPAやMyBatisを利用することがDAOの実装に相当すると考えます。DAOはデータアクセスのメカニズムを隠蔽するものです。JPAやMyBatisを利用すれば、インタフェースを用意するだけでまさにデータアクセスすることができます。JAPやMyBatisがその実装を引き受けて、これを隠蔽してくれます。

次に、リポジトリの実装はドメインオブジェクトを構築するものにします。リポジトリにはドメインオブジェクトのコレクションとしての振る舞いをもたせます。ここで、ドメインオブジェクトの構造はデータベースのテーブル構造と同じでないことに気がつきます。従って、（データベースのコンテキストで言うところの）エンティティからドメインオブジェクトを構築する必要があります。リポジトリがその役割を担うわけです。

上記を次の図に整理します。

![リポジトリとDAOの関係](../images/use-repository-and-dao-according-to-the-purpose/class-diagram.png)

# まとめ

リポジトリとDAOの違いはその目的にあります。目的の違いは説明されるコンテキストの違いに依ります。リポジトリはドメイン駆動設計における、DAOはデザインパターンにおける用語です。一方で、リポジトリとDAOは別々のコンテキストで説明されるので、これらには一致した側面があります。いずれもデータアクセスのメカニズムを隠蔽します。

リポジトリの目的はアプリケーションコードがドメインオブジェクトを操作できるようにすることです。リポジトリはエンティティからドメインオブジェクトを構築することで、ドメインオブジェクトのコレクションのように振る舞います。

DAOはの目的はアプリケーションコードから独立してデータアクセスのメカニズムを変更できるようにすることです。DAOはクライアントインタフェースを設けることで、データアクセスのメカニズムを隠蔽します。


リポジトリとDAOの使い分け方はメカニズムの隠蔽とアプリケーションコードに対する役割で整理できます。

メカニズムの隠蔽でDAOとリポジトリの使い分け方を整理できます。DAOはデータアクセスのメカニズムを隠蔽してエンティティの操作をクライアントに提供します。リポジトリはエンティティから構築してドメインオブジェクトの操作をクライアントに提供します。

アプリケーションコードに対する役割でリポジトリとDAOの使い分け方を整理できます。アプリケーションコードがリポジトリを利用し、リポジトリがDAOを利用します。リポジトリとDAOは併せて、次の役割と目的をもちます。ドメインオブジェクトの永続化に関わる物理的な操作を隠蔽し、アプリケーションコードがドメインオブジェクトを概念的に操作できるようにします。

----

# 参考

- [P of EAA: Repository](https://martinfowler.com/eaaCatalog/repository.html)
- [Design Patterns: Data Access Object](http://www.oracle.com/technetwork/java/dao-138818.html)
- [c# - What is the difference between the Data Mapper, Table Data Gateway (Gateway), Data Access Object (DAO) and Repository patterns? - Stack Overflow](https://stackoverflow.com/questions/804751/what-is-the-difference-between-the-data-mapper-table-data-gateway-gateway-da)
