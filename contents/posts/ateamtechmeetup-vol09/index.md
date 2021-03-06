---
title: "ATEAM TECH MeetUp_Vol.09 エイチームフィナジーのバックエンド開発"
description: "エイチーム社主催ミートアップ"
date: "2019-09-12"
tags: "勉強会"
---

## ATEAM TECH MeetUp_Vol.09 エイチームフィナジーのバックエンド開発

株式会社エイチーム様主催のイベントに参加してきたのでそのイベント内容と感想です。

## 取り組み

インターネットを軸に事業を行う総合IT企業。幅広く活動されており大きく3つの事業領域で構成されている。

3つの事業領域とは

- エンターテイメント事業
- ライフスタイルサポート事業
- EC事業

で、例えばライフスタイルサポート事業ではエンジニアがみんなお世話になっているであろうQiitaも運営されている（最近まで知らなかった）

## 企業理念

- みんなで幸せになれる会社にすること
- 今から100年続く会社にすること

## エイチームのビジネス

インターネットやスマートデバイスを通じて利用者の皆様に様々なサービスを提供

## ライフスタイルサポート事業

- 引っ越し侍
- ナビクル
- Hanayume
- ナビナビキャッシング
- Lalune
- Qiita

## 中長期的な展望

IT　× 〇〇　で色々と取り組まれていく

以下、セッションについて

## 段階的なシステムリプレースを実現するデータ同期技術

発表者：鈴木さん

## サービスの内容について

- 金融メディア事業の中の一Webメディア
- 2013年12月ローンチ
- グループ最大規模の売上に成長

## 問題

運用を続けるうちに、システムが肥大化・複雑化
Webサイト上のコンテンツの正確な管理・更新が問題となっていった

複雑化した旧システムを刷新し新しいシステムへ段階的なリプレースを実現したい

Ruby on Railsの知見が社内に多いから移行することに

新システムを大きく

- ユーザ向けページ
- 社員向け管理画面
- MySQLデータベース

旧システムでは社員向け管理画面を開かない

## 新システムへのリプレース後の各データの扱い

- マスタデータ
- トランザクションデータ

これらを新旧システムでReadのみ、Read/Write両方など分けた。

## データを同期させる必要

マスタデータのみを新システムへ持っていくと決めたが
依然として新システムを旧システムとを同時に稼働させ動かしていく必要がある
そのために行ったこと

1. MySQLを初期移行
1. 新システムで更新し、旧システムへ継続的な変更反映
1. 変換

旧システムのデータをSQLで取得しデータを移行

MySQL Replication　を使って新システムから旧システムへデータを複製

当初はバッチ処理を定期的に動かそうとしたが、
運用コストの高さ（整合性の保証やリトライ）を考えて

MySQL Viewを使い、旧システムのデータを旧システムのスキーマへ沿うように変換した

Replicationで作られたテーブルを参照するViewを作りRENAMEする

Amazon Aurora MySQL(AWSで提供されているMySQ:Lと互換性のあるマネージドのRDBMS)を利用

レプリケーションとは非同期の仕組み

AuroraReplicaLagというメトリクス

## まとめ

初期以降スクリプトとMySQLのReplication / viewを使い新システムのマスタデータを
旧システムでも利用できるようになった

このデータ同期により同一のマスタデータを取り扱う新システムへの段階的な移行が実現した。

## Rails APIの新規開発を担保するテストについて

@yothio317 さん

フロントはNEXT バックエンドはRAILSで構成されているシステムに携わっている
両方のソースがわからないといけないため両方関われた

社内プロジェクト
Ruby on Railsで動いている

RSpecを用いてテストを記述

Model/Serializer/Decorator => RSpec
View/ControllerはE2E

Rails API Mode?

rswag

RailsAPIのSqaggerツール
SwaggerベースのDSLを提供

rswagはAPIとUIの2つを提供してくれる

API側に変更を加える

新しいエンドポイント・リクエストのパラメータが変わる場合はテストを書く

## SSRの必要性について

アカザキヒロキさん
@mushokusai5

アニメ勢

カードローン事業部

SPAでサービスを作る！チャレンジング精神とサービス的にSPAが好ましかった

課題
SEOを考慮しないといけない

Next.jsとは？Reactを使えるJSフレームワーク。SSR機能が標準で搭載

CSRとSSR

SEO的観点
SSR必要なし

パフォーマンス的観点では
SSR　必要あり

Next.jsは多機能で便利

## GraphQLについて

ogomさん

Osaka Rubykaigiオーガナイザー

[OSS Gate](https://oss-gate.github.io/)にも携わっている

GraphQLの勉強は得意な言語からまたはGraphQLStudy、HowToGraphQLで学ぶ

## シャッフルランチの組み合わせロジックを実装してみた

アダチタクヤさん

エイチームフィナジー様で取り組まれているシャッフルランチ（各部署の人同士でランチを行う）の組み合わせについてこう言う仕組みはどうか？と言う提案を行なった

用いたものは遺伝的アルゴリズム

自分で調べた参考URL
<https://qiita.com/Azunyan1111/items/975c67129d99de33dc21>

一つの個体内で複数のグループを表現

参加者一人一人を遺伝子として表現してコーディング
改修がとても容易とのこと

笑顔で終始楽しそうに発表されていた

## 感想

単語だけのメモになっている箇所もありますが、以上が参加しての記事になります。
Webサービスを運営される中でどうしてもシステムが肥大化したり、古くなったりは避けられないのでどのように改修されるかと言う点に興味を持って参加したので実際のお話を伺えて楽しかったです。

また、テストに関しても興味はあるがなかなかできていない状態だったので個人開発においても取り組んでいかねばと思いました。

LTにも色々と刺激をもらえ、OSSに貢献できるようにしないとなーとか、Next.jsに興味を持てたり、アルゴリズムの学習ってすげーと思いました。

Next.jsから若干派生して、VueとReactではどちらを触ろうかなと悩むこともあったのですが、エイチームの社員の方とお話ししてReactに対して気持ちが傾いています。

理由の一つで知らなかったのはReactの機能を参考にしてVueが機能を取り入れていると言うことで技術的にも先を行っているのがReactなのかなぁなんて思います。

何はともあれ？この刺激を個人開発に活かしていきます。また機会があれば参加させていただきたいなと思います。ありがとうございました。
