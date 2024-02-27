---
title: ニュートリノ
taxonomy:
    category:
        - glossary
---

以下の英語の用語と説明を日本語にしてください。忠実な翻訳でなくて構いません。AI翻訳にかけて内容を理解した上で、ご自身の言葉で説明してください。

日本語の提案はGitHubでプルリクエストとして受付中。プルリクエストがマージされたら、報酬をライトニング⚡️送金します。
提案手順は[こちら](https://github.com/lostinbitcoin/categories/wiki)の「2. 用語集の用語説明の提案手順」をご参照ください。

## Neutrino
2,100 sats

Neutrino is a proposed light client protocol which offers privacy and efficiency improvements over existing light client designs, notably Simplified Payment Verification (SPV).

A typical light client requests data about transactions and blocks in which it is interested from either a central server or other nodes in the Bitcoin network. Often, when a light client requests such information, they leak their addresses and transactions to the server, sacrificing privacy. Several schemes have been proposed and implemented by different wallets. So far, none have emerged as a standard.

In order to preserve a light client’s privacy, the Neutrino protocol has the server send all transaction outputs in a block to the light client, leaving the light client to decide whether there are any transactions of interest. If there are such transactions, the light client requests the full block to be sent, in order to trustlessly verify that the transaction of interest was included in the block. This scheme preserves privacy better but requires significantly more bandwidth and compute power than the existing SPV scheme.

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
