---
title: "11月18日から11月24日までの振り返り"
description: "Wantedlyのプロフィール充実とIISでPHPを利用できる様にしました"
date: "2019-11-24"
tags: "振り返り"
---

## はじめに

こんにちは、Yumihikiです。今週はプログラミングで手を動かす度合いが少なめでした。

## Wantedlyのプロフィール充実？

転職活動で利用しているビジネスSNSのWantedlyに自己紹介文をしっかり書く様にしてみました。少し前までは少ない文章でこのポートフォリオサイトを見てね！という状態だったのですが余り企業様からの反応を得られなかったため、Wantedlyにしっかり文章を書く様にしてみました。
自分についての自己紹介、Web系のエンジニアを目指す理由、どんなエンジニアを目指すのか、働きたい企業についてといった項目を追加しました。

あしあとという項目があり、それを見ると色々と見て頂けている様なのですが、スカウトをなかなか頂けていないのが現状なので今後も少しずつ更新していきたいなと思います。

## IISでPHPを利用できる様に？

自社のポータルサイトを運用しているのですが、現在使用中のサーバーが廃止されるということで引越しの作業を行っていました。当初はPHPのインストールまで行っていただけると思っていたのですが、システム部門の方からIISのインストールはしたのであとは自分でやる様に、と言われたため「良い経験になるかな」と思って作業しました。
最初はPHPを単にインストールするだけでしょ！　と思っていたのですが、案の定途中で詰まるなどありました。

うまいことまとめきれていないのですが、私が触った環境の場合は次のことができていないため、PHPが動いていませんでした。（参考：[なにか作る-Windows 7のIIS上でPHPを動かす](http://create-something.hatenadiary.jp/entry/2014/06/11/194808))

> IISのインストール
> [インターネット インフォメーション サービス] > [World Wide Web サービス] > [アプリケーション開発機能] > [CGI] にチェックを入れる。
> Download Visual Studio 2012 更新プログラム 4 の Visual C++ 再頒布可能パッケージ from Official Microsoft Download Centerからランタイムをダウンロードしてインストールする。

(実際には2015をインストールしました)

> アクセス権限の設定

設定全般

> IISへのPHPランタイムの登録

設定全般

といった具合でした。良い経験になりました。

自社はIISを基本的に利用しているみたいなのでLinuxではありませんでしたが、今後はLinuxなどサーバー周りも色々と触ってみたいなと思いました。

## どんなエンジニアになりたいか？

前回の最後に、
> そのため少し自分なりにどういうエンジニアになりたいか・どう人生を過ごしていきたいか考え直しています。また来週にでも、自分の気持ちを改めて整理した上でブログに投稿致します。

なんて投稿していました。
自分なりに考えていたのですが、一言でいうとゼネラリスト系のエンジニアになりたいと思っています。バックエンド・フロントエンド・インフラ関係を理解し、設計・要件定義から開発運用まで担えるエンジニアを目指しています。その理由は、一つの分野に特化すると汎用性が失われ活躍の場が減ってしまうことを懸念していること、また複数の強みを掛け合わせた上でオンリーワンの強みを持ちたいと思っていることが挙げられます。

前者の理由としては、尊敬するエンジニアの方から聞いた話がきっかけです。その方曰く、リーマンショックの時に派遣切りが多く行われたことがあり、それまでは特化型でも問題なかったそうなのですが派遣切り以降は汎用性の高いエンジニア、複数の領域も担当できるエンジニアが求められる様になったとのことでした。その話を聞いて、一つの領域だけ行えるというのはその様な弱みにも繋がるのだなと思い、ゼネラリスト寄りが良いと判断する様になりました。

また後者の理由は、自身がこれから活躍していくことを考えた場合に「何でもできる！」だと抽象度が高くあまり必要とされにくいのでは、と先日購入した「キャリアスキルズ」という本を読んで感じたことに加え、以前に（1月になりますが）[そうだんドットミー](https://www.so-dan.me/)　というサービスを利用した際にアドバイザーの方から強みを掛け合わせてオンリーワンのエンジニアになろうと言われたことがきっかけです。単純にPHPだけできる！というだけでなく、PHPとデザインができる！という状態からさらにPHPとデザインとインフラ構築ができる！というのでは希少性・価値が高まると思うため、複数領域の強みを掛け合わせたいなと思います。

あとは単純に、色々と勉強することが楽しいなと思うので色々とやってみたいなという気持ちもあります（笑）

若干まとまりがないですが、こういうエンジニアを目指しています。

## 最後に

転職活動が少しずつ進み始め、プログラミングに割ける時間が少なくなりつつありますが合間を見てHiitaの改善に努めていきたいなと思います。
楽なことばかりではないですが、満足いく様に転職活動を行なっていきたいと思います。

最後まで読んでくださりありがとうございました。
