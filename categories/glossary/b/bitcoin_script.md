---
title: ビットコインスクリプト
taxonomy:
    category:
        - glossary
---

以下の英語の用語と説明を日本語にしてください。忠実な翻訳でなくて構いません。AI翻訳にかけて内容を理解した上で、ご自身の言葉で説明してください。

日本語の提案はGitHubでプルリクエストとして受付中。プルリクエストがマージされたら、報酬をライトニング⚡️送金します。
提案手順は[こちら](https://github.com/lostinbitcoin/categories/wiki)の「2. 用語集の用語説明の提案手順」をご参照ください。

## Bitcoin Script
2,100 sats

Bitcoin’s scripting language is simply called Script. All Bitcoin scripts are written in Script. It is a simple language that is not Turing complete, meaning it lacks several logical functions, including loops. This is done to ensure that no Bitcoin script can consume inordinate computing power and harm nodes on the network.
Script is used almost exclusively to lock and unlock bitcoin, not to build applications or run programs. Script’s simplicity also gives Bitcoin security and makes it easier for developers to avoid losing money while designing wallets or applications on top of Bitcoin.

All Bitcoin transactions use Script to define how outputs can be spent. In other words, the script of a Bitcoin transaction determines to whom the bitcoin was sent. Bitcoin has a few different scripts, with Pay-to-Public-Key-Hash (P2PKH) being the most popular. P2PKH is a simple script which pays bitcoin to an address.

Other scripts can achieve more complex setups, such as creating multisig addresses. Bitcoin sent to a multisig address requires multiple signatures from multiple private keys to be spent.

Although SegWit script types—P2WPKH and P2WSH—offer savings on transaction fees, adoption of these new script types has been slow. As of April 2021, almost four years after SegWit’s activation, P2PKH scripts are used by over 70% of UTXOs.

![](/_images/glossary-ha_1.png)

Source: [Clark Moody's Dashboard](https://bitcoin.clarkmoody.com/dashboard/)

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
