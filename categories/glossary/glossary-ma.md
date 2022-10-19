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

### 索引 ま

|  用語  |  英語表記  |  説明  |  報酬  |
| ---- | ---- | ---- |---- |
|<a id="マリアビリティ"></a>マリアビリティ|  Malleability | Transaction malleability is the ability of a transaction to have multiple valid IDs (txids). Malleability occurs when a part of a transaction can change after the transaction has been signed without invalidating the signature. Since a txid is a hash of the transaction, any change to the transaction will result in a change of the txid. However, changes that alter the txid and invalidate the signature are not a concern; only changes which alter the txid and do not invalidate the signature raise malleability concerns. Malleability is a problem for developers and users who want to reference a previous transaction in a spending transaction before the previous transaction has been confirmed on the blockchain. This problem arises because, in order to spend an output created by a previous transaction, the spending transaction must reference the txid of the previous transaction. If this txid can change, the reference will fail, and the spending transaction will be rendered invalid. A transaction can be malleated in two ways. First, after being signed, additional data can be added to a ScriptSig. Secondly, the signature itself, which is contained within the ScriptSig, can be changed. These options are both possible because a signature cannot sign itself.Eliminating transaction malleability was achieved by the SegWit upgrade, enabling more innovation on top of Bitcoin, including the Lightning Network and Taproot. SegWit eliminated transaction malleability by moving the ScriptSig—the transaction signature and the malleable part of the transaction—from the main body of the transaction into a separate Witness section.|  1,000 sats  |
| | |
| | |

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.