---
title: ECDSA
taxonomy:
    category:
        - glossary
---

以下の英語の用語と説明を日本語にしてください。忠実な翻訳でなくて構いません。AI翻訳にかけて内容を理解した上で、ご自身の言葉で説明してください。

日本語の提案はGitHubでプルリクエストとして受付中。プルリクエストがマージされたら、報酬をライトニング⚡️送金します。
提案手順は[こちら](https://github.com/lostinbitcoin/categories/wiki)の「2. 用語集の用語説明の提案手順」をご参照ください。

## ECDSA
2,100 sats

The Elliptic Curve Digital Signature Algorithm or ECDSA is a cryptographic scheme for producing digital signatures using public and private keys. All Bitcoin keys and signatures are currently generated using ECDSA. An ECDSA signature allows someone to publish a public key and then create a signature of some data with their private key, such that anyone can verify that the signature was created by the owner of this public key. However, no one is capable of deriving the private key from the public key or the signature. Nor can this signature be used to forge a signature for other data. ECDSA signatures are used to sign all Bitcoin transactions thanks to these strong security features. An elliptic curve is a defined mathematical function of the general format y^2 = x^3 + ax + b. For Bitcoin, this curve has the specific equation y^2 = x^3 + 7, as a = 0 and b = 7. Any point on this elliptic curve, called secp256k1, is a valid Bitcoin public key. In order to generate a public key, a user must generate a private key, which is simply a large number. Next, this private key is multiplied by a defined point called the Generator Point, to produce the public key. This multiplication is point multiplication, which behaves differently than normal multiplication. Critically, point division is incalculable, meaning a public key cannot currently be used to derive a private key, giving the ECDSA scheme its security.

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
