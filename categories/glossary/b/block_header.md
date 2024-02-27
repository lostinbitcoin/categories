---
title: ブロックヘッダー
taxonomy:
    category:
        - glossary
---

以下の英語の用語と説明を日本語にしてください。忠実な翻訳でなくて構いません。AI翻訳にかけて内容を理解した上で、ご自身の言葉で説明してください。

日本語の提案はGitHubでプルリクエストとして受付中。プルリクエストがマージされたら、報酬をライトニング⚡️送金します。
提案手順は[こちら](https://github.com/lostinbitcoin/categories/wiki)の「2. 用語集の用語説明の提案手順」をご参照ください。

## Block Header
2,100 sats

A block is a collection of transactions. Each block also includes some metadata which provides a summary of the block. This metadata is known as the block header. Included in the block header are several pieces of data:

・Block height. The block height indicates how many blocks have come before this block.<br>
・Block hash. The hash of the block header serves as Proof-of-Work for this block.<br>
・Previous block hash. The hash of the previous block header ensures past blocks cannot be altered.<br>
・Timestamp. The timestamp indicates when the block was published.<br>
・Merkle root. A Merkle root is the hash of all the transactions included in this block.<br>
・Difficulty. The difficulty is encoded and called the “bits”.<br>
・Nonce. A nonce is a random number which helps miners satisfy the Proof-of-Work.

The block header serves as an efficient summary of a block and can be sent across the network and processed more rapidly than a full block. When miners hash their block continuously, searching for a valid hash as Proof-of-Work, they are in fact hashing the block header, not the entire block.

This is done for efficiency purposes, as hashing more data, including the thousands of transactions included in each block, takes more time. If miners were forced to hash the entire block, they would be incentivized to mine empty blocks in order to hash more efficiently. This would lower Bitcoin’s throughput and utility, as miners would lack incentive to process transactions.

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
