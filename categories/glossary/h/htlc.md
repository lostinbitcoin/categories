---
title: HTLC (ハッシュタイムロックコントラクト)
taxonomy:
    category:
        - glossary
---

以下の英語の用語と説明を日本語にしてください。忠実な翻訳でなくて構いません。AI翻訳にかけて内容を理解した上で、ご自身の言葉で説明してください。

日本語の提案はGitHubでプルリクエストとして受付中。プルリクエストがマージされたら、報酬をライトニング⚡️送金します。
提案手順は[こちら](https://github.com/lostinbitcoin/categories/wiki)の「2. 用語集の用語説明の提案手順」をご参照ください。

## Hashed Time Locked Contract (HTLC)
2,100 sats

タイムロック付きコントラクト（Time Locked Contract）は、「ある時刻やブロック高になるまで、そのコインを使えない」という条件（＝タイムロック）を含むビットコイントランザクションのことです。このトランザクションにハッシュの条件「正しいハッシュの答え（プリイメージ）を提示できれば受け取れる」を組み合わせたものが、HTLC（Hashed Time Locked Contract）です。HTLCは主に[ライトニング・ネットワーク](https://lostinbitcoin.sakuraweb.com/lightning_network/)で使われ、支払いを複数の[ノード](https://lostinbitcoin.sakuraweb.com/bitcoin_node/)を経由して届けるための仕組みを支えています。これにより、送る人と受け取る人のあいだに直接[チャネル](https://lostinbitcoin.sakuraweb.com/lightning_channel/)がなくても、間のチャネルを利用して、相手を信用に頼らず（trustless）安全に送金できます。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.