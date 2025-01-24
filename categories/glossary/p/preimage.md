---
title: プリイメージ
taxonomy:
    category:
        - glossary
---

## Preimage
2,100 sats

プリイメージとは、[ハッシュ関数](https://lostinbitcoin.jp/glossary/hash_function/)（特定のデータを固定長の値に変換する関数）に入力される元データのことを指します。ハッシュ関数は一方向性で設計されているため、計算結果であるハッシュ値から元のデータ（プリイメージ）を逆算することはできません。

プリイメージにはあらゆるデータを利用できます。例えば、ビットコインの[アドレス](https://lostinbitcoin.jp/glossary/address/)は[公開鍵](https://lostinbitcoin.jp/glossary/public_key/)をハッシュ化して生成されます。同様に、[ブロックヘッダー](https://lostinbitcoin.jp/glossary/block_header/)はブロックの[プルーフオブワーク（PoW）](https://lostinbitcoin.jp/glossary/pow/)のプリイメージとして機能します。

ハッシュは、プリイメージへのコミットメント（特定のデータが存在することの約束）として利用されます。これは、プリイメージを公開せずにコミットメントを示すことが可能であるためです。例えば、ビットコインがP2PKH（公開鍵ハッシュ）アドレスに送金される場合、そのビットコインは特定の公開鍵にコミットされますが、その公開鍵は所有者以外には知られていません。この所有者がビットコインを使用したい場合、公開鍵（プリイメージ）と署名を公開することで、対応する秘密鍵を管理していることを証明します。この情報を基に、[ブロックチェーン](https://lostinbitcoin.jp/glossary/blockchain-2/)を検証する誰もが、ビットコインが実際にその公開鍵に属していたことを確認できます。

[ライトニング・ネットワーク](https://lostinbitcoin.jp/glossary/lightning_network/)でも、プリイメージはライトニング請求書が支払われたことを証明するために使用されます。この場合、[ハッシュタイムロックコントラクト（HTLC）](https://lostinbitcoin.jp/glossary/htlc/)がコミットメントとして機能し、ルーティングノードが支払いのための手数料を受け取ることを約束します。一方、プリイメージ（未ハッシュのタイムロックコントラクト）は、その約束が実行されたことを証明する役割を果たします。HTLCは支払い元のノードからルーティングノード、受取人の[ノード](https://lostinbitcoin.jp/glossary/node-2/)へと送信され、受取人はHTLCのプリイメージを返送することで、ルーティングノードが約束された手数料を受け取れるようにします。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
