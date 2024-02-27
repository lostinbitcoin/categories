---
title: シュノア署名
taxonomy:
    category:
        - glossary
---

以下の英語の用語と説明を日本語にしてください。忠実な翻訳でなくて構いません。AI翻訳にかけて内容を理解した上で、ご自身の言葉で説明してください。

日本語の提案はGitHubでプルリクエストとして受付中。プルリクエストがマージされたら、報酬をライトニング⚡️送金します。
提案手順は[こちら](https://github.com/lostinbitcoin/categories/wiki)の「2. 用語集の用語説明の提案手順」をご参照ください。

## Schnorr Signature
2,100 sats

Schnorr is a type of digital signature scheme similar to the ECDSA scheme used by Bitcoin since its inception. The Schnorr scheme presents several advantages over ECDSA, and is thus currently in the process of being implemented in Bitcoin via the Taproot upgrade.

Firstly, the Schnorr scheme is provably secure and non-malleable, two improvements over ECDSA. Secondly, compared to ECDSA signatures, Schnorr signatures take less time to verify. Schnorr signatures and public keys can be aggregated, meaning that multiple parties with unique private keys can sign the same message with much greater efficiency. Thanks to this feature, Schnorr signatures can be verified in batches instead of individually, further speeding up verification.

Key and signature aggregation also enable privacy gains by obscuring the number of signatures present on a transaction. Finally, Schnorr signatures are also smaller than ECDSA signatures, offering savings on fees for those spending Schnorr outputs.

When Bitcoin was invented, the Schnorr scheme was still patent-protected, and thus Satoshi Nakamoto decided to use ECDSA as the signature scheme for Bitcoin. The Schnorr patent has since expired, and Schnorr is currently in the process of being implemented in Bitcoin.

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
