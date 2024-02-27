---
title: MuSig
taxonomy:
    category:
        - glossary
---

以下の英語の用語と説明を日本語にしてください。忠実な翻訳でなくて構いません。AI翻訳にかけて内容を理解した上で、ご自身の言葉で説明してください。

日本語の提案はGitHubでプルリクエストとして受付中。プルリクエストがマージされたら、報酬をライトニング⚡️送金します。
提案手順は[こちら](https://github.com/lostinbitcoin/categories/wiki)の「2. 用語集の用語説明の提案手順」をご参照ください。

## MuSig
2,100 sats

MuSig is a protocol for creating Taproot multisig public keys and signatures. MuSig makes use of Schnorr signature and public key aggregation, and thus will only be possible with the activation of the Taproot upgrade.

MuSig is special in that a resulting multisig transaction is no longer discernible from a single signature transaction. This is because MuSig combines the individual public keys of each party to create a single public key. When bitcoin is spent from this public key, the spenders are not forced to reveal their individual public keys. Instead, they collectively create a single signature valid for the public key they created earlier. This is not the case for typical multisig transactions, which use P2SH scripts and force the signatures and public keys of each signer to be revealed on the blockchain.

MuSig presents a significant privacy improvement over the current multisig implementation, and not just for MuSig users. MuSig will undermine many heuristics currently used for chain analysis by removing any differentiation between single signature and multi signature transactions.


---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
