---
title: マリアビリティ
taxonomy:
    category:
        - glossary
---

## Malleability
2,100 sats

トランザクション展性（マリアビリティ）とは、1つの[トランザクション](http://lostinbitcoin.jp.testrs.jp/staging/glossary/transaction/)が複数の有効な[トランザクションID（txid）](http://lostinbitcoin.jp.testrs.jp/staging/glossary/txid/)を持つ可能性を指します。マリアビリティは、トランザクションが[署名](http://lostinbitcoin.jp.testrs.jp/staging/glossary/signature/)された後でも、その署名を無効化せずにトランザクションの一部を変更できる場合に発生します。txidはトランザクション全体のハッシュ値であるため、トランザクションが変更されるとtxidも変わります。ただし、変更によって署名が無効になる場合は問題ではありません。問題となるのは、署名が有効なままでtxidだけが変更されるケースです。

マリアビリティは、[ブロックチェーン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/blockchain/)上で確認される前の以前のトランザクションを参照して支払いトランザクションを作成したい開発者やユーザーにとって問題となります。この問題は、以前のトランザクションによって作成されたアウトプットを使用するためには、支払いトランザクションが以前のトランザクションのtxidを参照する必要があるためです。もしこのtxidが変更可能であれば、参照は失敗し、支払いトランザクションは無効となります。

マリアビリティが発生する理由は２つあります。一つ目は、署名後のScriptSig（トランザクションの署名スクリプト）への追加データの挿入です。二つ目は、ScriptSig内の署名自体の変更です。これらは、署名が自身を保護する仕組みを持たないために発生します。

しかし、[SegWit](http://lostinbitcoin.jp.testrs.jp/staging/glossary/segwit/)アップグレードにより、トランザクションのマリアビリティは解消されました。SegWitでは、トランザクションのマリアビリティに関する部分であるScriptSigをトランザクション本体から分離し、新たに設けられたWitnessセクションに移動しました。これにより、[ライトニング・ネットワーク](http://lostinbitcoin.jp.testrs.jp/staging/glossary/lightning_network/)や[タップルート](http://lostinbitcoin.jp.testrs.jp/staging/glossary/taproot/)といった、Bitcoin上でのさらなる技術革新が可能となりました。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
