---
title: トランザクションID (TXID)
taxonomy:
    category:
        - glossary
---

## Transaction ID (txid)
2,100 sats

トランザクションID（TXID）とは[ブロックチェーン](https://lostinbitcoin.sakuraweb.com/glossary/blockchain/)上で特定の[トランザクション](https://lostinbitcoin.sakuraweb.com/glossary/transaction/)を識別するための英数字から成る文字列です。この文字列はトランザクション全体に2回[SHA-256](https://lostinbitcoin.sakuraweb.com/glossary/sha_256/)を適用して生成したハッシュで、[ノード](https://lostinbitcoin.sakuraweb.com/glossary/node/)や[ブロックエクスプローラ](https://lostinbitcoin.sakuraweb.com/glossary/block_explorer/)でトランザクションを検索する時に使います。

[Segwit](https://lostinbitcoin.sakuraweb.com/glossary/segwit/)以前のトランザクションでは、[承認](https://lostinbitcoin.sakuraweb.com/glossary/confirmation/)前にインプットの一部や[署名](https://lostinbitcoin.sakuraweb.com/glossary/signature/)を書き換えても、トランザクションとして有効となる改変方法があります。インプットや署名を書き換えるのでTXIDは変化しますが、トランザクション自体は有効なので承認されます。これはトランザクション・[マリアビリティ](https://lostinbitcoin.sakuraweb.com/glossary/malleability/)という特性によるものです。SegWitトランザクションでは、改変可能なインプットや署名をTXID生成の対象外としたため、TXIDが承認前後で変わることはなくなりました。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
