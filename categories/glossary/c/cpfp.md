---
title: CPFP
taxonomy:
    category:
        - glossary
---

以下の英語の用語と説明を日本語にしてください。忠実な翻訳でなくて構いません。AI翻訳にかけて内容を理解した上で、ご自身の言葉で説明してください。

日本語の提案はGitHubでプルリクエストとして受付中。プルリクエストがマージされたら、報酬をライトニング⚡️送金します。
提案手順は[こちら](https://github.com/lostinbitcoin/categories/wiki)の「2. 用語集の用語説明の提案手順」をご参照ください。

## Child-Pays-for-Parent (CPFP)
2,100 sats

Child-Pays-for-Parent is a transaction mechanism with a similar purpose as Replace-by-Fee (RBF). While RBF allows the sender to speed up a transaction’s confirmation, Child-Pays-for-Parent allows the recipient to speed up the transaction’s confirmation.

In case a transaction is sent with a low fee and is not being confirmed fast enough for the recipient’s liking, the recipient may create a new transaction spending the bitcoin they received in the previous transaction (even though it is still unconfirmed in the mempool). This second transaction will pay a higher fee and signal to miners that they must mine the first transaction first in order to mine the second transaction. In this way, the recipient will receive their funds faster despite the low fee paid by the sender.

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
