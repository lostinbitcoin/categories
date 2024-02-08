---
title: マークルツリー
taxonomy:
    category:
        - glossary
---

## Merkle Tree
2,100 sats

A Merkle tree is a data structure with unique properties which make it useful for Bitcoin. Merkle trees are used to store all transactions in a given block. The advantage of this system is that one node can easily prove to another that a given transaction was contained in a specific block. This is useful for SPV nodes and light clients, who do not store the entire blockchain and are only interested in certain transactions or blocks.
For example, if Alice runs a wallet and is waiting for her transaction to confirm, but she does not run a node, she can request a Merkle proof from Bob, who runs a full node. This proof will convince Alice that the transaction she is interested in was included in a valid block, without Bob needing to share all of the transactions or the entire block with Alice.

From a technical point of view, a Merkle tree has layers. The first layer is the list of all transaction IDs (txids) in a block. To produce the second layer, these txids are concatenated and hashed in pairs using SHA-256. Thus, the second layer will be half as long as the first layer. This process is continued until the last layer contains exactly one hash. This is called the Merkle root. Given the properties of a hash, if a single transaction id is changed, that change will trickle up the tree and change the root hash entirely.

![](/_images/glossary-ma_1.png)

The advantage of a Merkle tree is that the presence of any given transaction id in a Merkle tree can be proven without revealing the entire Merkle tree. For example, in a Merkle tree with eight transactions, only three hashes must be provided to prove that one of the txids were included in that tree. This provides great efficiency for light clients, which do not store the entire blockchain, and therefore must query other nodes for proof that certain transactions are confirmed.

![](/_images/glossary-ma_2.png)

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
