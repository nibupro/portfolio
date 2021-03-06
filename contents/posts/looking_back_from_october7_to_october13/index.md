---
title: "10月7日から10月13日までの振り返り"
description: "お客先様訪問とポートフォリオ作り"
date: "2019-10-13"
tags: "振り返り"
---

## はじめに

こんにちは、Yumihikiです。今週は業務でお客様先へ訪問を行い、プライベートではポートフォリオ作成を進めていました。

## お客様先訪問

自社のECサイトの勉強会（使い方の説明）と、お客様から自社へCSVデータでの発注を行う仕組み(EDIと読んでいますが世間一般の正確な言葉とあっているのかは不明です・・・)の打ち合わせを行なっていました。
ECサイトの勉強会では、お客様がログインするまでの手順と使用方法(発注方法)、便利機能の説明などを行いました。今回は15人程度のお客様へ一気に説明することになりましたがみなさまリアクションがよく、しっかりと説明できたかと思います。多数の方へ向けての説明だと反応が少ない場合もあり多少不安になりながら解説することになることが多いのですが、お客様に恵まれたと思います。

また、CSVデータでの発注を行う仕組みの打ち合わせですが、その前に説明を挟むと現職ではお客様からの発注方法として電話・FAX・インターネット発注の3つを用意し、受注しています。その中でインターネット発注にはDVD-ROMからインストールするものとECサイト、そしてCSVデータ間でのやり取りを行うものを用意しています。上述していますが、自社ではEDIと呼んでいるのですがこの呼び名も正確なようなそうでないような気がするので何て言えば良いかご存知の方がいらっしゃったら教えていただきたいです。

若干話がそれましたが、私はCSVで受発注を行うために発注を識別するユニークな値が欲しい、コードが欲しいといった希望レイアウトの話やそもそも機能としてありそうか、といったヒアリングやご提案を行なっています。今回伺ったお客様は前回一度システム担当者様とお話ししており、追加で打ち合わせを行うため訪問しました。事前に準備していたこともありスムーズに話が進みました。
うまく説明・提案が進むお客様ばかりではないのですが、今回は企業様にシステム担当者がいらっしゃることもあり比較的スムーズに話が進んでよかったです。

## ポートフォリオ作成

この土日に大きく進めることができたのですが、出来たことは大きく3つで次の通りでした。

- レイアウト調整(BootStrap3から4の記述へ)
- 削除ボタンの実装
- 編集ボタンの実装

レイアウト調整は、参考にしていた基本のタスクリストがBootStrap3の書き方だったこともあり、現行の4系では存在しない「panel」を「card」へ変更や無くても伝わりそうな箇所の削除など行いました。まだ出来ていない・気になるところもありますが、まずは機能を先に実装していこう！と思いまた後々手を加えていきます。

削除ボタンは、、正直基本のタスクリストをまま実装しただけなのでControllerを利用する等修正します。

編集ボタンには若干手間取りましたが何とか（？）機能として実装できました。とはいえ、こちらも良い書き方ではないため修正予定です。
というのはメンターさんにコードを少し見てもらったところ、[Route Model Binding](https://laravel.com/docs/6.x/routing#route-model-binding)　という機能を教えてもらいました。この機能を使ってもっと簡潔に記述できるはず、とのことなのでこちらを試しつつもっと良いコードにしていきたいと思います。

機能としては、たくさん実装したい内容は他にもありますが、とりあえずはカレンダーを搭載して他の日付の記録を確認できるようにしたいと思っています。やりたいことと期日までに出来るもののバランスなどを考えるのが若干楽しく、最初は全て実装したい！という気持ちが強かったのですが、それではいつまでたっても完成しないため、まずは最低限のものを実装してから順次機能を追加する予定です。

## 最後に

エラーが出てしまうことも多々あったのですが、エラーメッセージを読む・検索する、SlackOverflowを見ることで8割がた解決できた気がします。この辺りも以前の自分と比べるとレベルアップしたなと感じて少し自信になります。この調子で引き続きコーディングしながら、今月中にポートフォリオ作成を終わらせていきたいと思います！

最後まで読んでくださりありがとうございました。
