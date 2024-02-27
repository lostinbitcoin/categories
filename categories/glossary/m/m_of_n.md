---
title: M-of-N
taxonomy:
    category:
        - glossary
---

以下の英語の用語と説明を日本語にしてください。忠実な翻訳でなくて構いません。AI翻訳にかけて内容を理解した上で、ご自身の言葉で説明してください。

日本語の提案はGitHubでプルリクエストとして受付中。プルリクエストがマージされたら、報酬をライトニング⚡️送金します。
提案手順は[こちら](https://github.com/lostinbitcoin/categories/wiki)の「2. 用語集の用語説明の提案手順」をご参照ください。

## M-of-N
2,100 sats

The term m-of-n describes the precise conditions of a multisig setup, with m being the number of signatures required, and n being the number of authorized keys from which the signatures can come. A Multiple Signature (multisig) address is a Bitcoin address which requires the signatures of multiple private keys in order to be spent. While most bitcoin is controlled in a single signature setup, some Bitcoin users store their bitcoin in a multisig setup to avoid a single point of failure. If one of their keys is compromised, they do not lose their funds.

Let’s walk through an example: Alice, Bob, and Charlie want to start a company and hold joint custody of some bitcoin. To ensure that one of them cannot steal the collective funds, Alice, Bob, and Charlie share one public key each. They also decide that they will run their company based on majority rule. Thus, any two signatures are sufficient to spend their shared bitcoin. This requirement of two signatures (m) coming from any of the three (n) public keys is translated into a script, which is hashed to yield the address to which all three partners will send their contributions to the company fund. This set up would be described as a 2-of-3 multisig.


---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
