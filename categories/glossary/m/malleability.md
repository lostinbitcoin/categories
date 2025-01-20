---
title: マリアビリティ
taxonomy:
    category:
        - glossary
---

## Malleability
2,100 sats

マリアビリティとは、1つの[トランザクション](https://lostinbitcoin.jp/glossary/transaction/)が複数の有効な[トランザクションID（txid）](https://lostinbitcoin.jp/glossary/txid/)を持つ可能性を指します。この問題は、[署名](https://lostinbitcoin.jp/glossary/signature/)後に署名を無効とせず、トランザクションの一部が変更可能な場合に発生します。txidはトランザクション全体のハッシュ値であるため、トランザクションが変更されるとtxidも変わります。ただし、署名が無効化される変更は問題ではなく、txidが変更されても署名が有効である場合に問題が生じます。

マリアビリティは、以前のトランザクションを参照して新しいトランザクションを作成する際に問題を引き起こします。特に、未確認トランザクションを参照して新しいトランザクションを作成する際、txidが変更されるとその参照が無効となり、新しいトランザクションが失敗します。

マリアビリティが発生する理由は２つあります。一つ目は、署名後にScriptSig（トランザクションの署名スクリプト）への追加データの挿入です。二つ目は、ScriptSig内の署名自体の変更です。これらは、署名が自身を保護する仕組みを持たないために発生します。

しかし、[SegWit](https://lostinbitcoin.jp/glossary/segwit/)アップグレードにより、トランザクションのマリアビリティは解消されました。SegWitでは、トランザクションのマリアビリティに関する部分であるScriptSigをトランザクション本体から分離し、新たに設けられたWitnessセクションに移動しました。これにより、[ライトニング・ネットワーク](https://lostinbitcoin.jp/glossary/lightning_network/)や[タップルート](https://lostinbitcoin.jp/glossary/taproot/)など、さらなる技術革新が可能となりました。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
