---
title: RBF (Replace-By-Fee)
taxonomy:
    category:
        - glossary
---

以下の英語の用語と説明を日本語にしてください。忠実な翻訳でなくて構いません。AI翻訳にかけて内容を理解した上で、ご自身の言葉で説明してください。

日本語の提案はGitHubでプルリクエストとして受付中。プルリクエストがマージされたら、報酬をライトニング⚡️送金します。
提案手順は[こちら](https://github.com/lostinbitcoin/categories/wiki)の「2. 用語集の用語説明の提案手順」をご参照ください。

## Replace-By-Fee (RBF)
2,100 sats

Bitcoinにおいて、RBFは「Replace-by-Fee（手数料による差し替え）」の略です。
ビットコインのトランザクションはRBFとして指定することができ、その場合、送信者はより高い手数料を支払う同様のトランザクションで当該トランザクションを置き換えられます。
この仕組みは、ネットワークが混雑して手数料が予想外に上昇したときでも、ユーザーが対応できるようにするために存在します。もしユーザーが低い手数料でトランザクションを送信し、確定までに時間がかかりすぎると感じた場合、手数料を引き上げてトランザクションの確定を早めることができます。

RBFが機能するのは、そのトランザクションが[メンプール](https://lostinbitcoin.jp/glossary/mempool/)に存在している間だけです。
いったん[トランザクション](https://lostinbitcoin.jp/glossary/transaction/)が[ブロック](https://lostinbitcoin.jp/glossary/block/)に取り込まれると、手数料による差し替えはできません。

RBFを使うには、最初に送る時点で「差し替えできるよ」という合図を入れておく必要があります。
具体的には、各入力（input）に付いている小さな数値フィールド「nSequence」のうち、少なくとも1つを 0xfffffffe 未満の値に設定して送ります。これで「この取引は、あとからより高い手数料の取引に差し替えてOK」という意思表示になります。nSequence はもともと、ブロードキャスト後に取引を更新できるようにするための仕組みの一部です。[BIP 125 (RBF)](https://lostinbitcoin.sakuraweb.com/glossary/bip125/)も参照してください。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
