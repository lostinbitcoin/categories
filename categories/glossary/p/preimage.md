---
title: プリイメージ
taxonomy:
    category:
        - glossary
---

## Preimage
2,100 sats

プリイメージとは、[ハッシュ関数](http://lostinbitcoin.jp.testrs.jp/staging/glossary/hash_function/)（特定のデータを固定長の値に変換する関数）に入力される元データのことを指します。ハッシュ関数は一方向性で設計されているため、計算結果であるハッシュ値から元のデータ（プリイメージ）を導き出すことはできません。

プリイメージにはあらゆるデータを利用できます。例えば、[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)の[アドレス](http://lostinbitcoin.jp.testrs.jp/staging/glossary/address/)は[公開鍵](http://lostinbitcoin.jp.testrs.jp/staging/glossary/public_key/)をハッシュ化して生成されます。同様に、[ブロックヘッダー](http://lostinbitcoin.jp.testrs.jp/staging/glossary/block_header/)は[ブロック]((http://lostinbitcoin.jp.testrs.jp/staging/glossary/block/))の[プルーフオブワーク（PoW）](http://lostinbitcoin.jp.testrs.jp/staging/glossary/pow/)のプリイメージとして機能します。

ハッシュは、プリイメージへのコミットメント（特定のデータが存在することの約束）として利用されます。これは、プリイメージを公開せずにコミットメントを示すことが可能であるためです。例えば、ビットコインがP2PKH（公開鍵ハッシュ）アドレスに送金される場合、そのビットコインは特定の公開鍵にコミットされますが、その公開鍵は所有者以外には知られていません。この所有者（ここではアリスと呼びます）がビットコインを使用したい場合、公開鍵（プリイメージ）と署名を公開することで、対応する[秘密鍵](http://lostinbitcoin.jp.testrs.jp/staging/glossary/private_key/)を管理していることを証明します。この情報を基に、[ブロックチェーン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/blockchain-2/)を検証する誰もが、ビットコインが実際にその公開鍵に関連付けられており、アリスがその公開鍵の所有者であることを確認できます。

[ライトニング・ネットワーク](http://lostinbitcoin.jp.testrs.jp/staging/glossary/lightning_network/)でも、プリイメージは[ライトニング・インボイス](http://lostinbitcoin.jp.testrs.jp/staging/glossary/lightning_invoice/)が支払われたことを証明するために使用されます。この場合、[ハッシュタイムロックコントラクト（HTLC）](http://lostinbitcoin.jp.testrs.jp/staging/glossary/htlc/)がコミットメントとして機能し、ルーティングノードが支払いのための手数料を受け取ることを約束します。一方、プリイメージ（すなわち、ハッシュ化されていないタイムロックコントラクト）は、その約束が実行されたことを証明する役割を果たします。HTLCは支払い元のノードからルーティングノード、受取人の[ノード](http://lostinbitcoin.jp.testrs.jp/staging/glossary/node-2/)へと送信され、受取人はHTLCのプリイメージを返送することで、ルーティングノードが約束された手数料を受け取れるようにします。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
