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

### 索引 <a id="ra"></a>ら

|  用語  |  英語表記  |  説明  |  報酬  |
| ---- | ---- | ---- |---- |
|<a id="lightning_invoice"></a>ライトニング・インボイス| Lightning Invoice | A Lightning invoice is similar to a normal invoice in that it serves as a request for payment. A Lightning invoice includes the amount to be paid, the destination of the payment, metadata, and a message. Invoices are the Lightning equivalent of an address in that both are sent from the payee to the payer to facilitate a payment. Lightning invoices are usually represented as QR codes due to their length.|  2,100 sats  |
|<a id="lightning_implementations"></a>ライトニング実装| Lightning Implementations | ライトニング実装とはライトニングノードを稼働させ、ライトニングネットワークと接続することが可能なソフトウェアプログラムです。 <br>ライトニング実装には様々なプログラミング言語で書かれた複数の異なる実装が存在します。<br>最も一般的なライトニング実装は、LND、c-lightning、Electrum Lightning、Eclairなどです。<br>各実装は微妙に異なる機能や設計を提供していますが、すべての実装はBasis of Lightning Technology (BOLT) 仕様で定義された規格に準拠しています。<br>この仕様ではあるライトニング実装が他のすべての実装と相互運用できるように必要な機能を定義しています。 |  2,100 sats  |
|<a id="lightning_channel"></a>ライトニング・チャネル|Lightning Channel|A Lightning channel is a connection between two parties, and the Lightning Network is composed of thousands of channels. Lightning transactions are sent back and forth over channels and are used to recalibrate the bitcoin balances of each party in this channel. All bitcoin in a channel belongs to one of the two parties. Lightning channels are called bidirectional payment channels because both parties can send and receive bitcoin across the channel. In order to open a Lightning channel, two parties, say Alice and Bob, cooperatively construct a 2-of-2 multisig address. Any bitcoin sent to this address requires two signatures, one from each party, in order to be spent. Imagine Alice and Bob open a channel and deposit 1 BTC each. If Alice now wishes to pay Bob 0.5 BTC, she signs a transaction spending from the multisig address. This transaction has two outputs: Bob will receive 1.5 BTC and Alice will receive 0.5 BTC. Since spending from the multisig address requires two signatures, this is not yet a valid transaction, and Alice cannot broadcast it to the Bitcoin network. Instead, she sends the partially-signed transaction, called a commitment transaction, to Bob, who keeps it but does not broadcast it. Alice has paid Bob 0.5 BTC, but Bob has not settled this payment to the Bitcoin blockchain. This is why Lightning transactions are so cheap: they do not require miners to confirm each transaction in a block. A Lightning channel can be closed at any point by publishing the latest unbroadcast commitment transaction. This transaction will send the bitcoin from multisig address to each party in the correct amount, representing the net flow of bitcoin across all of the Lightning transactions that occured on this channel. |  2,100 sats  |
|<a id="lightning_network"></a>ライトニング・ネットワーク| Lightning Network|The Lightning Network (LN) is a protocol designed to allow instant and cheap Bitcoin transactions. The Lightning Network is still experimental, but it shows promise for Bitcoin’s ability to scale. This protocol is built around bidirectional payment channels, which allow two parties to send money back and forth to one another. In addition, multiple channels can be strung together to route payments between parties who do not have a direct connection. In order to open one of these bidirectional payment channels, two users send bitcoin to a joint-custody address by submitting an on-chain Bitcoin transaction. The bitcoin in this joint-custody address can be instantaneously rebalanced between the two parties for free without a Bitcoin transaction. For example, if Alice and Bob both contribute 0.5 BTC to a joint-custody address, the Lightning Network will show their balances as 0.5 BTC each. If Alice then wishes to send Bob 0.1 BTC, she updates the state of the joint-custody address. Bob now has 0.6 BTC while Alice has 0.4 BTC. This transaction is not sent to the Bitcoin blockchain yet, and the pair can continue to transact many more times, updating their respective balances as they go. Only when they wish to close the channel is one final transaction sent to the Bitcoin blockchain. This transaction represents the net change in the two users' balances. |  2,100 sats  |
|<a id="layer"></a>レイヤー| Layer | Bitcoin’s blockchain offers final settlement for bitcoin at the cost of relatively low throughput. The Bitcoin network averages between 4-7 transactions per second. This is obviously insufficient for hosting all of the world’s financial transactions, as Bitcoin intends to do. While larger settlements can still be settled to the blockchain to achieve maximal security, smaller transactions in need of lower security can be executed “off-chain” by another service or protocol, called a layer. Layered solutions can trade lower security for higher throughput and cheaper fees. Bitcoin developers prefer that innovation and scaling takes place on layers on top of Bitcoin in order to separate the security risks that come with software innovation from affecting Bitcoin’s blockchain. These layers have analog examples in the legacy financial system: credit cards, Venmo, and PayPal are all layered on top of a core banking system of wire transfers and the ACH system. Before the gold standard was abandoned, physical cash was a layer on top of the base money of gold.|  2,100 sats  |

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
