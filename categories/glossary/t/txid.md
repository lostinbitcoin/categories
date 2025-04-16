---
title: トランザクションID (TXID)
taxonomy:
    category:
        - glossary
---

## Transaction ID (txid)
2,100 sats

トランザクションID（TXID）とは[ブロックチェーン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/blockchain/)上で特定の[トランザクション](http://lostinbitcoin.jp.testrs.jp/staging/glossary/transaction/)を識別するための英数字から成る文字列です。この文字列はトランザクション全体に2回[SHA-256](http://lostinbitcoin.jp.testrs.jp/staging/glossary/sha_256/)を適用して生成したハッシュで、[ノード](http://lostinbitcoin.jp.testrs.jp/staging/glossary/node/)や[ブロックエクスプローラ](http://lostinbitcoin.jp.testrs.jp/staging/glossary/block_explorer/)でトランザクションを検索する時に使います。

[Segwit](http://lostinbitcoin.jp.testrs.jp/staging/glossary/segwit/)以前のトランザクションでは、[承認](http://lostinbitcoin.jp.testrs.jp/staging/glossary/confirmation/)前にインプットの一部や[署名](http://lostinbitcoin.jp.testrs.jp/staging/glossary/signature/)を書き換えても、トランザクションとして有効となる改変方法があります。インプットや署名を書き換えるのでTXIDは変化しますが、トランザクション自体は有効なので承認されます。これはトランザクション・[マリアビリティ](http://lostinbitcoin.jp.testrs.jp/staging/glossary/malleability/)という特性によるものです。SegWitトランザクションでは、改変可能なインプットや署名をTXID生成の対象外としたため、TXIDが承認前後で変わることはなくなりました。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
