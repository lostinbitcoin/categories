---
title: SegWit
taxonomy:
    category:
        - glossary
---

## SegWit
2,100 sats

Segregated Witness (SegWit) is a soft-fork upgrade to Bitcoin which was activated in 2017. SegWit fixed the problem of transaction malleability, wherein a transaction could have several possible txids. This upgrade paved the way for the implementation of the Lightning Network, and will open the door for several future upgrades, including Taproot.

SegWit also allowed more transactions to be included in a single block, which eased fee pressure and provided a partial scaling solution.

One of the most noticeable changes introduced by SegWit was the switch from using Base58 encoding to Bech32 encoding.

SegWit eliminated transaction malleability by moving the ScriptSig—the transaction signature and the malleable part of the transaction—from the main body of the transaction into the Script Witness, which resides in the Witness section. The Witness of each transaction is still stored on the blockchain, but only by nodes whose version includes SegWit.

Because the Witness is not included in the main body of a transaction, it does not affect the txid. However, in order to ensure that the Witness of a transaction cannot be altered after its inclusion in a block, a separate Witness txid (wtxid) is calculated. This wtxid includes the Witness and a Merkle tree of wtxids are recorded in an output of each block’s coinbase transaction.


---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
