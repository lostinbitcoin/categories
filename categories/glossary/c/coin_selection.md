---
title: コインセレクション
taxonomy:
    category:
        - glossary
---

以下の英語の用語と説明を日本語にしてください。忠実な翻訳でなくて構いません。AI翻訳にかけて内容を理解した上で、ご自身の言葉で説明してください。

日本語の提案はGitHubでプルリクエストとして受付中。プルリクエストがマージされたら、報酬をライトニング⚡️送金します。
提案手順は[こちら](https://github.com/lostinbitcoin/categories/wiki)の「2. 用語集の用語説明の提案手順」をご参照ください。

## Coin Selection
2,100 sats

Coin selection is the process of choosing a subset of the UTXOs owned by a wallet in order to create and fund a transaction. When creating a transaction on behalf of a user, a wallet must select specific UTXOs as inputs in the transaction.

For example, if Alice wishes to pay Bob 1 BTC and her wallet contains 5 BTC in various amounts, her wallet must determine which UTXOs to spend. This decision is not trivial, and depends on the priority of the user. Some coin selection methods prioritize spending smaller outputs to avoid dust accumulation while others spend large outputs to pay lower fees. Still others prioritize privacy or avoiding change outputs.

Coin selection is usually dictated by an algorithm built into a wallet, but some wallets allow users to dictate their own coin selection preferences to suit their needs.

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
