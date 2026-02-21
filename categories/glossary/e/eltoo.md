---
title: Eltoo
taxonomy:
    category:
        - glossary
---

以下の英語の用語と説明を日本語にしてください。忠実な翻訳でなくて構いません。AI翻訳にかけて内容を理解した上で、ご自身の言葉で説明してください。

日本語の提案はGitHubでプルリクエストとして受付中。プルリクエストがマージされたら、報酬をライトニング⚡️送金します。
提案手順は[こちら](https://github.com/lostinbitcoin/categories/wiki)の「2. 用語集の用語説明の提案手順」をご参照ください。


## Eltoo
2,100 sats

Eltoo（「L2」と発音）は、主に[レイヤー](https://lostinbitcoin.sakuraweb.com/glossary/layer/)2ソリューション、特に[ライトニング・ネットワーク](https://lostinbitcoin.sakuraweb.com/glossary/lightning_network/)を改善することを目的とした、[ビットコイン](https://lostinbitcoin.sakuraweb.com/glossary//bitcoin-2/)に対する提案中のアップグレードです。

Eltooは、SIGHASH_NOINPUTと呼ばれる新しいサイハッシュフラグを [プロトコル](https://lostinbitcoin.sakuraweb.com/glossary/protocol/)に導入することで、これらのアップグレードを実装します。この新しいサイハッシュフラグにより、入力の[トランザクションID（TXID）](https://lostinbitcoin.sakuraweb.com/glossary/txid/)を指定することなく、ビットコインの[署名](https://lostinbitcoin.sakuraweb.com/glossary/signature/)を[トランザクション](https://lostinbitcoin.sakuraweb.com/glossary/transaction/)にコミットできるようになります。

txidを指定しないことで、トランザクションにより大きな柔軟性がもたらされます。これは、親トランザクションが[ブロックチェーン](https://lostinbitcoin.sakuraweb.com/glossary/blockchain-2/) に公開される前に、子孫トランザクションへ署名できることを意味します。

たとえば、アリスとボブが[ライトニング・チャネル](https://lostinbitcoin.sakuraweb.com/glossary/lightning_channel/)を開く場合、まずビットコインを[2-of-2](https://lostinbitcoin.sakuraweb.com/glossary/m_of_n/)の[マルチシグ](https://lostinbitcoin.sakuraweb.com/glossary/multisig/)アドレスへ送る資金調達トランザクションに署名します。チャネルが開かれた後、アリスとボブは一連の更新トランザクションを作成し、2-of-2マルチシグアドレス内の資金を使用します。アリスとボブがチャネルを閉じたい場合には、決済トランザクションに署名する必要があります。

Eltooがない場合、この一連の処理における各トランザクションは、直前のトランザクションが作成されてからでなければ署名できません。Eltooを用いると、資金調達トランザクションと同時に決済トランザクションへ署名することが可能になります。これにより[ライトニング・ネットワーク・ペナルティ](https://lostinbitcoin.sakuraweb.com/glossary/lightning_network_penalty/)が不要となり、ライトニングネットワークにおける[二重支払い](https://lostinbitcoin.sakuraweb.com/glossary/double_spend/)保護が大幅に簡素化されます。

重要な事実：Eltooは新しいサイハッシュフラグを導入するため、[コンセンサス](https://lostinbitcoin.sakuraweb.com/glossary/consensus/)プロトコルの変更となり、ソフトフォークが必要になります。


---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
