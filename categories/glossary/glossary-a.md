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

### 索引 <a id="a"></a>あ

|  用語  |  英語表記  |  説明  |  報酬  |
| ---- | ---- | ---- |---- |
|<a id="address"></a>アドレス|  Address |  An address is used to receive bitcoin and is represented as a string of letters and numbers. Public keys and addresses are often conflated. An address is usually a hash of a public key, and at present, addresses, not public keys are used to directly receive bitcoin. On a technical level, an address can represent more than just the hash of a public key.A Bitcoin wallet allows users to generate as many addresses as they require. Wallets also allow users to send bitcoin to a provided address. When bitcoin is sent to an address, only the owner of the private key(s) which derived that address is capable of spending the bitcoin.Warning: avoid address reuse to protect your privacy. *It is considered a best practice never to reuse addresses. Every time you wish to receive bitcoin, you should use your wallet to generate a new address.* On a technical level, an address can represent several different scripts. Addresses are encoded and prefixed in order to convey their script type. Legacy addresses use Base58, and when a legacy address is the hash of a public key, a so-called P2PKH address, it begins with a ‘1’. Less frequently, a legacy address is a hash of a script, in which case it will begin with a ‘3’. Currently, all SegWit addresses are encoded in Bech32 and begin with the prefix ‘bc1’.When a user inputs an address into their wallet in order to send bitcoin to that address, the wallet examines the address type and constructs the appropriate script. This script, called the scriptPubKey, is appended to the amount being sent to the address. These two pieces of data—the amount and the scriptPubKey—form an output. | 2,100 sats  |
|<a id="ibd"></a>イニシャル・ブロック・ダウンロード (IBD) |Initial Block Download (IBD) | Initial Block Download (IBD) is the process of building the full Bitcoin blockchain from scratch. When a new node is set up and joins the network, it connects to other nodes and asks them for blocks. The new node processes these blocks and builds the blockchain until it has caught up and is in sync with the network. Although blocks are being requested from individual nodes, the IBD process is trustless because a node can cross-check the data from different nodes and because of the nature of the blockchain’s Proof-of-Work chain. This process can take a few days or a few weeks depending on internet bandwidth and computer specifications. When beginning IBD, a node first gathers all of the block headers from other nodes and then requests each full block. This is done for increased efficiency and to allow users to begin using their node sooner. While building the blockchain block by block, a Bitcoin node also builds the UTXO set—the comprehensive list of all valid bitcoin. This set is updated with each block as the transactions in that block destroy and create UTXOs.|2,100 sats |
|<a id="wallet"></a>ウォレット |Wallet| A wallet is a piece of software which generates and stores public and private keys, allowing users to send, receive, and store bitcoin. Wallets can come in the form of mobile apps, desktop apps, or hardware devices. Wallet is a general term for any of these implementations, and wallets differ greatly on security and privacy. Wallets are most useful for abstracting the complexities of Bitcoin and cryptography away from the user, so that they can transact and store their bitcoin in a simple manner. Wallets will show users their balances, their transaction history, and their addresses, which users can publish in order to receive transactions. Selecting a wallet with quality security and privacy practices is important, as is backing up the wallet in case you lose or break your device.|2,100 sats |
|<a id="off_chain"></a>オフチェーン |Off-Chain| Off-chain is a term used to describe any data that is not registered on the Bitcoin blockchain. Off-chain data can be Bitcoin transactions that were not sent to the blockchain, data on the Lightning Network, or data on other blockchains, such as a sidechain.|2,100 sats |
|<a id="on_chain"></a>オンチェーン |On-Chain | AOn-chain is a term used to describe any data that is registered on the Bitcoin blockchain, in contrast with off-chain data, which is not stored on the blockchain. On-chain data are always Bitcoin transactions, while off-chain data can be an unconfirmed Bitcoin transaction or any other type of data..|2,100 sats |
---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
