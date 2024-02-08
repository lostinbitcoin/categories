---
title: Eltoo
taxonomy:
    category:
        - glossary
---

## Eltoo
2,100 sats

Eltoo—pronounced as “L2”—is a proposed upgrade to Bitcoin whose main goal is to improve layer two solutions, most importantly, the Lightning Network.

Eltoo would implement these upgrades by introducing a new sighash flag called SIGHASH_NOINPUT to the Bitcoin protocol. The new sighash flag would allow a Bitcoin signature to commit to a transaction without specifying the txid of the input.

Leaving the txid unspecified enables greater flexibility for transactions. It means descendant transactions can be signed before their ancestors are published to the blockchain.

For example, if Alice and Bob open a Lightning channel, they first sign a funding transaction, which sends bitcoin to a 2-of-2 multisig address. Once the channel is open, Alice and Bob make a series of update transactions, which spend the funds in the 2-of-2 multisig address. When Alice and Bob wish to close the channel, they must sign a settlement transaction to do so.

Without eltoo, each transaction in this process can only be signed once the previous one has been created. With eltoo, the settlement transaction can be signed at the same time as the funding transaction. This eliminates the need for the Lightning Network penalty, significantly simplifying the Lightning Network’s double spend protection.

Key Fact: Because eltoo would introduce a new sighash flag, it is a change to the consensus protocol, and would require a soft fork.

Because eltoo would introduce a new sighash flag, it is a change to the consensus protocol, and would require a soft fork.

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
