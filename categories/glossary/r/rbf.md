---
title: RBF (Replace-By-Fee)
taxonomy:
    category:
        - glossary
---

## Replace-By-Fee (RBF)
2,100 sats

In Bitcoin, RBF stands for Replace-by-Fee. A Bitcoin transaction can be designated as RBF in order to allow the sender to replace this transaction with another similar transaction which pays a higher fee. This mechanism exists to allow users to respond if the network becomes congested and fees rise unexpectedly. If a user sends a transaction with a low fee, and finds that it is taking too long to confirm, the user can raise the fee they pay to confirm their transaction faster. RBF only works while the transaction is in the mempool. As soon as a transaction enters a block, it cannot be replaced by fee. Additionally, when a transaction is first sent, it must specify that it is available to be replaced by fee. This is achieved by setting the nSequence, a small part of each transaction, to any value below 0xfffffffe. The nSequence of a transaction is intended to allow a transaction to be updated after it has been broadcast. Also see [BIP 125 (RBF)](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bip125/)


---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
