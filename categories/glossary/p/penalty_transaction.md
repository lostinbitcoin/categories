---
title: ペナルティトランザクション
taxonomy:
    category:
        - glossary
---

以下の英語の用語と説明を日本語にしてください。忠実な翻訳でなくて構いません。AI翻訳にかけて内容を理解した上で、ご自身の言葉で説明してください。

日本語の提案はGitHubでプルリクエストとして受付中。プルリクエストがマージされたら、報酬をライトニング⚡️送金します。
提案手順は[こちら](https://github.com/lostinbitcoin/categories/wiki)の「2. 用語集の用語説明の提案手順」をご参照ください。

## Penalty Transaction
2,100 sats

A penalty transaction allows an one party to a Lightning channel to reclaim funds that were stolen during the dishonest close of a Lightning channel. To send a Lightning channel payment, the sender signs a Bitcoin transaction called a commitment transaction which rebalances the channel. This new transaction is sent to the receiver, but is not broadcast to the Bitcoin blockchain. Future Lightning payments will create additional commitment transactions and render this transaction out of date. However, the original transaction is still a valid Bitcoin transaction, and can thus be broadcast to the blockchain. This would close the Lightning channel and undo all Lightning transactions which occurred after the original. This allows parties to steal or double spend on the Lightning Network.

In order to fix this problem, commitment transactions are set up such that even after an old commitment transaction has been confirmed on the blockchain, if someone can produce a newer, valid commitment transaction from the same channel, this transaction can reclaim the stolen funds and additionally claim all of the funds from the thief’s side of the channel.

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
