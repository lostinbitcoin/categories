---
title: ライトニング・ネットワーク・ペナルティ
taxonomy:
    category:
        - glossary
---

以下の英語の用語と説明を日本語にしてください。忠実な翻訳でなくて構いません。AI翻訳にかけて内容を理解した上で、ご自身の言葉で説明してください。

日本語の提案はGitHubでプルリクエストとして受付中。プルリクエストがマージされたら、報酬をライトニング⚡️送金します。
提案手順は[こちら](https://github.com/lostinbitcoin/categories/wiki)の「2. 用語集の用語説明の提案手順」をご参照ください。

## Lightning Network Penalty
2,100 sats

The Lightning Network Penalty is a mechanism for discouraging attempts to double spend bitcoin using the Lightning Network (LN). Currently the LN Penalty confiscates the entire balance of a Lightning channel from an actor who attempts to publish an invalid state in order to steal funds.

The Lightning Network uses fully signed Bitcoin transactions to transfer bitcoin between parties. These transactions are not normally broadcast and added to the Bitcoin blockchain. However, since they are valid transactions, any of them can be broadcast to the blockchain at any time. This would close the Lightning channel and invalidate any Lightning transactions that occurred after that time.

This mechanism can be exploited to allow double spends over Lightning. For example, Alice and Bob have an open Lightning channel, in which they each control 0.25 BTC. Both parties currently hold a commitment transaction which allots each of them 0.25 BTC. Alice then sends Bob 0.05 BTC over Lightning, leaving her with 0.2 BTC while Bob has 0.3 BTC. A new commitment transaction reflects this new balance. However, Alice can now take the old commitment transaction and publish it to the blockchain. Each party would receive 0.25 BTC, which would effectively reverse the 0.05 BTC transaction Alice sent to Bob.

In order to prevent this, the Lightning protocol enables Bob to publish the newer commitment transaction within a certain time period and take not just the 0.05 BTC he is owed, but the full 0.5 BTC from the channel. Bob would take Alice’s entire stake in the channel as a punishment for Alice’s attempted double spend.

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
