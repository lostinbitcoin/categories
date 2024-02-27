---
title: ダスト攻撃
taxonomy:
    category:
        - glossary
---

以下の英語の用語と説明を日本語にしてください。忠実な翻訳でなくて構いません。AI翻訳にかけて内容を理解した上で、ご自身の言葉で説明してください。

日本語の提案はGitHubでプルリクエストとして受付中。プルリクエストがマージされたら、報酬をライトニング⚡️送金します。
提案手順は[こちら](https://github.com/lostinbitcoin/categories/wiki)の「2. 用語集の用語説明の提案手順」をご参照ください。

## Dust Attack
2,100 sats

Occasionally, attackers will send tiny fractions of bitcoin, around 500 sats, to random wallets. If the owner of the wallet does not notice, they may inadvertently include this piece of dust in their next transaction, leaking information about which bitcoin they own to the attacker. A dust attack is like placing a tracking device on a victim, allowing the attacker to view where the victim travels, or in this case, which bitcoin the victim owns. High quality wallets do their best to disallow users from including dust in their transactions in order to protect them from such attacks. If you notice tiny amounts of unsolicited bitcoin being sent to your wallet, you should not spend them as part of a transaction with other pieces of bitcoin. A dust attack only works if the victim spends the dust along with other UTXOs they own.

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
