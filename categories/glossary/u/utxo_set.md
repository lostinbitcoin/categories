---
title: UTXOセット
taxonomy:
    category:
        - glossary
---

以下の英語の用語と説明を日本語にしてください。忠実な翻訳でなくて構いません。AI翻訳にかけて内容を理解した上で、ご自身の言葉で説明してください。

日本語の提案はGitHubでプルリクエストとして受付中。プルリクエストがマージされたら、報酬をライトニング⚡️送金します。
提案手順は[こちら](https://github.com/lostinbitcoin/categories/wiki)の「2. 用語集の用語説明の提案手順」をご参照ください。

## UTXO Set
2,100 sats

The UTXO set is the comprehensive set of all UTXOs existing at a given point in time. The sum of the amounts of each UTXO in this set is the total supply of existing bitcoin at that point of time. Bitcoin is special as a money in that anyone can verify the total supply at any time in a trustless manner. All nodes maintain identical copies of the UTXO set. When a new block is created, the UTXO set is updated as some UTXOs were spent and new ones were created. The UTXO set is also important because it allows all nodes in the Bitcoin network to detect and reject attempted double spends, wherein someone attempts to spend the same bitcoin twice. Nodes must store the entire UTXO at all times in order to determine which bitcoin exist, and thus can be spent, at any given point in time.


---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
