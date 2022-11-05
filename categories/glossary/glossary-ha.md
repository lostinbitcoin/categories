---
title: 用語集
taxonomy:
    category:
        - glossary
---

### 日本一充実したビットコイン用語集を作りたい！

[River Financial の Bitcoin Glossary](https://river.com/learn/terms/) をベースに、日本語のビットコイン用語集を構築中です。用語集作りに参加して、**ビットコイン**を稼ぎませんか？

以下の英語の用語説明を日本語にしてください。忠実な翻訳でなくて構いません。AI翻訳にかけて内容を理解した上で、ご自身の言葉で説明してください。

日本語の提案はGitHubでプルリクエストとして受付中。プルリクエストがマージされたら、報酬をライトニング⚡️送金します。<br>
提案手順は[こちら](https://github.com/lostinbitcoin/categories/wiki)の「2. 用語集の用語説明の提案手順」をご参照ください。

--
### ビットコイン用語集

### 索引 は

|  用語  |  英語表記  |  説明  |  報酬  |
| ---- | ---- | ---- |---- |
|<a id="hash_function"></a>ハッシュ関数| Hash Function|There are many instances of cryptographic hash functions, but all cryptographic hash functions share a few key properties. All cryptographic hash functions take an input, called a preimage, and produce an output, called a hash or digest, of a fixed length. This length varies based on the precise function used. The output of a cryptographic hash function is deterministic. For a given input, the output will always be exactly the same. A cryptographic hash function is a one-way function. An output can easily be calculated from an input. However, there is no known way of determining the input from a given output. The output is random and unpredictable. There is no known method for targeting a specific output and calculating the proper input. Nor can a relationship be drawn between a series of inputs and their outputs. For example, if an input of 100 characters is changed by a single character, the new output bears no resemblance to the old output. These properties make cryptographic hash functions very useful for Bitcoin. Hashing is random and uncontrollable, ensuring Bitcoin mining is a fair competition. Hashing a public key or a script to obtain an address provides superior security, privacy, and convenience for users. Hashing transactions and blocks provides a simple way of creating universally unique IDs for both transactions and blocks. Finally, Merkle Trees use hashing to create reliable, immutable summaries of all transactions in a block, making mining and block verification significantly more efficient. Bitcoin only uses a few hash functions for its various aspects. The hash function SHA-256 is used for creating Proofs-of-Work, and SHA-256 is applied twice to generate txids. In order to generate public key hashes or addresses, the hash160 function is used. This is a combination of the SHA-256 and RIPEMD160 hash functions.|2,100 sats  |
|<a id="hash_rate"></a>ハッシュレート| Hash Rate |Hash rate is a measure of how many hashes miners cumulatively produce per second on the Bitcoin network. A single hash is an attempt to create a Proof-of-Work for a block, and billions of these attempts are made per second by miners around the world. The hash rate indicates how much money, energy, and computing power is being dedicated to processing transactions and securing the network. Hash rate is also an indication of how much a 51% attack on the network would cost. Since a 51% attack requires a malicious miner to control at least 51% of hash rate, the higher the hash rate, the more prohibitively expensive it is for any miner to launch such an attack. Bitcoin’s hash rate has been growing rapidly over the past decade as Bitcoin’s price appreciation incentivizes more miners to join the network. Hash rate is influenced by several factors, including Bitcoin’s price, energy prices and available quantities, local weather, and regulatory environments.|2,100 sats  |
|<a id="batching"></a>バッチ|Batching|Batching involves consolidating multiple payments into a single transaction with many outputs. Because Bitcoin fees are paid based on how much data the transaction uses, combining multiple transactions into a single transaction can lower data overhead and thus save on fees. For example, if Alice wants to pay Bob 0.5 BTC, Charlie 0.3 BTC, and David 0.2 BTC, she can create a transaction with a 1 BTC input and 3 outputs instead of creating 3 transactions with 2 outputs each—one for the payee and one for change output. The advantages of batching increases with scale. For example, an exchange wishing to serve 100 client withdrawal requests can either submit 100 transactions, or a single transaction with 100 different outputs. The latter option will offer significant fee savings.|2,100 sats  |
|<a id="hardware_wallet"></a>ハードウェアウォレット| Hardware Wallet|A hardware wallet is a digital device whose sole purpose is to generate and store public and private keys and sign transactions. Hardware wallets allow users to send and receive Bitcoin in a secure fashion. Hardware wallets are a form of cold storage, meaning that they allow a user to keep their private keys safely disconnected from the internet. Most hardware wallets implement BIP 32 and BIP 39 standards, meaning they use Hierarchical Deterministic wallets and mnemonic phrases. Like all wallets, different hardware wallets vary in terms of security, privacy, and reliability.|2,100 sats  |
|<a id="hard_cap"></a>ハードキャップ|Hard Cap|Bitcoin total supply will never exceed 21 million bitcoin or 2.1 quadrillion satoshis. The hard cap is what guarantees Bitcoin’s absolute scarcity and protects Bitcoin from the fate of many fiat currencies in the past and present—hyperinflation.|2,100 sats  |
|<a id="hard_fork"></a>ハードフォーク|Hard Fork|A fork generally is a change to a project’s source code. Bitcoin is an open-sourced project, meaning that anyone can access, download, or alter the source code without permission. A hard fork specifically is a consensus change that is not backwards compatible. Backwards incompatibility occurs when a previously invalid behavior is made valid. In order to maintain consensus across a hard fork, all nodes are required to upgrade. Otherwise, old nodes will reject transactions or blocks as invalid under the old rules, while upgraded nodes will accept them as valid. For this reason, hard forks are avoided at all costs in Bitcoin.|2,100 sats  |
|<a id="halving"></a>半減期|  Halving | The halving is an event which reduces the issuance rate of bitcoin by half every four years. Bitcoin’s issuance schedule is precisely defined by an algorithm in Bitcoin’s code. This algorithm allows a certain amount of new bitcoin to be minted in each block, as compensation for the miner of the block.This new bitcoin is called the block subsidy, and at Bitcoin’s inception, it was 50 BTC per block. However, the subsidy is cut in half in an event called the halving, which takes place every 210,000 blocks—roughly every four years. This process will continue until the subsidy reaches zero, by which time over 7 million blocks will have been mined across 34 halvings. |2,100 sats  |


---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
