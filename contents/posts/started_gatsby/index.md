---
title: "GatsbyJSを利用してポートフォリオサイトを構築"
description: "メンターさんに教えてもらいながらポートフォリオサイトを作ってみた"
date: "2019-04-30"
hero: ../../images/started-gatsby-hero-image.png
tags: ["初心者", "Gatsby"]
---

## はじめに
こんにちは、Yumihikiです。

私は現在、エンジニア転職を目指して活動しています。その中で自分がポートフォリオサイトを作りたかったのでメンターのなかむさん（[@nakanakamu0828](https://twitter.com/nakanakamu0828)）に教わりながらGatsbyJSで構築してみました。と言っても正直なところ、おんぶに抱っこ状態であまり理解出来ていません。そのため、一つ一つ自分なりに調べて・解説をしていきたいと思います。

せっかくの休日ということもあり、出来るだけこの機会にたくさん復習を進めていきたいと思います。まずはこの記事ではGatsbyJSについて説明・紹介していきたいと思います。

## GatsbyJSって何？
GatsbyJSとはReactJS製の静的サイトジェネレーターのことです。（静的サイトジェネレータについて:WordPressなど、サーバーサイドのスクリプトによって訪問者のリクエストに応じてページを生成するサイトを動的サイトと呼びます。静的は対義語になりHTMLで構成されたサイトのことです）GatsbyJSについては日本語の情報がまだ少ないですが、私が参考にしたサイトをいくつか列挙します。
- [GatsbyJS公式Webサイト](https://www.gatsbyjs.org/) :公式Webサイトです。チュートリアルを一通り行いました。Google翻訳で日本語に翻訳してもらいながらでしたが、それなりにわかりやすかったです。
- [メンターのなかむさんの公開したページ](https://gatsby-starter-portfolio.nakamu.life/post/started_gatsby/):こちらのサイトを写経させてもらいました。こういうのを作れるんだ… と初めてみた瞬間、完成度の高さになぜか笑ってしまいました。自分も１からこのレベルのサイトを立ち上げられるようになりたいです。
- [MOTTO × MOTTO](https://mottox2.com/):フリーランスエンジニア・デザイナーとして活動されているもっとさん([@mottox2）](https://twitter.com/mottox2))のブログです。こちら以外にも、もっとさんが書かれた本([GatsbyJS Guidebook](https://booth.pm/ja/items/1312387))があるのでGatsbyJSを日本語で学ぶ場合、参考になるかと思います。
- [RU-Blog](https://ru-blog.com):RUさん([@ru88s](https://twitter.com/ru88s))が作られたブログです。作られた際のメモを残されており、こういう風に作っていけば良いんだな〜と参考にさせてもらいました。
- [bagelee GatsbyJSとNetlifyCMSでWebサイトを作ろう！](GatsbyJSとNetlifyCMSでWebサイトを作ろう！):最初にGatsbyJSについて調べた時にヒットして読んでいた記事です。この記事もわかりやすく、最初にNetlify CMSで公開するまでを取り組んでみました。（ただその公開できるサイトのメンテナンスが難しく、最初に取り組むにはあまりオススメできないです。。）
- [Crient GatsbyJSをはじめる](https://crieit.net/posts/GatsbyJS):保活広場というWebサイトを運営されている、コリさん([@1042limit](https://twitter.com/1042limit))が投稿された記事です。Twitter上でGatsbyについて調べたらおすすめと紹介されていたのと、メンターのなかむさんからもおすすめされました。
- [R note](https://rnote.work/):ryoさん([@rriver](https://twitter.com/rriver/)が運営されているブログ。react-helmetでググっていたところヒットして読ませてもらいました。
- [Takumon Blog](https://takumon.com/):takumonさん([@inouetakumon](https://twitter.com/inouetakumon))が運営されているブログ。かなり完成度の高いブログです！　JS周りのこともたくさん書かれておりとても参考になります。

おそらく私が説明するより、上述したサイトを訪問してもらう方がとてもわかりやすいと思います。

## GatsbyJS触ってみてどう？
正直なところ、難しいです。ReactJS製とのことで、Reactも全くわからない状態からのスタートだったので、「やっぱりWordPressの方が良いのでは…」と悩むこともありました。しかしファイルの読み込みが即時反映される、少ない時間で素晴らしいサイトが作れると言ったメリットが素晴らしく、情報を集めるため海外のサイトも積極的に訪問しようと思えました。難しいですけど、普通に楽しいです。Reactについても勉強して、理解を深めたいと思います。

## 終わりに
mdファイルでのブログ構築も初めてなので記事を書くのに非常に時間がかかってしまいました。まずはこのような入門？記事として、他にReactJS、TailwindCSS、Netlifyについても記事を書きたいと思います。その後、実際にポートフォリオサイトを作ってみての解説？をしていけたらなと思います。