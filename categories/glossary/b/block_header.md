---
title: ブロックヘッダー
taxonomy:
    category:
        - glossary
---

## Block Header
2,100 sats

[ブロック](http://lostinbitcoin.jp.testrs.jp/staging/glossary/block/)とは、[トランザクション](http://lostinbitcoin.jp.testrs.jp/staging/glossary/transaction/)の集合体を指します。また、各ブロックにはブロックの概要を提供するいくつかのメタデータが含まれており、このメタデータがブロックヘッダーと呼ばれます。ブロックヘッダーには以下のデータが含まれます：

	・[ブロック高](http://lostinbitcoin.jp.testrs.jp/staging/glossary/block_height/)：このブロックの前に存在するブロックの数を示します。
	・ブロックハッシュ：このブロックの[プルーフオブワーク](http://lostinbitcoin.jp.testrs.jp/staging/glossary/pow/)を表します。
	・前のブロックのハッシュ：過去のブロックが改ざんされないよう保証します。
	・タイムスタンプ：ブロックが公開された日時を示します。
	・マークルルート：このブロックに含まれるすべてのトランザクションをハッシュ化した値です。
	・[難易度](http://lostinbitcoin.jp.testrs.jp/staging/glossary/difficulty/)（Difficulty）：難易度がエンコードされており、「bits」と呼ばれます。
	・ナンス：プルーフオブワークを達成するためにマイナーが使用するランダムな数値です。

ブロックヘッダーはブロックの効率的な要約として機能するため、ブロック全体よりも早く、ネットワーク上に迅速に送信され処理することができます。マイナーが有効なハッシュを探すためにブロックを継続的にプルーフオブワークする際、実際にハッシュ化しているのはブロック全体ではなくブロックヘッダーです。

この方法は効率性を考慮したものであり、ブロックに含まれる何千ものトランザクション全体をハッシュ化するよりも時間がかかりません。もしマイナーがブロック全体をハッシュ化しなければならない場合、より効率的にハッシュ化するために、空のブロックを採掘することにインセンティブが働きます。これは、マイナーがトランザクションを処理する動機を失い、結果[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)の処理能力や実用性を低下させることにつながります。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
