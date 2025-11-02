---
title: RBF (Replace-By-Fee)
taxonomy:
    category:
        - glossary
---

## Replace-By-Fee (RBF)
2,100 sats

ビットコインにおいて、RBFは「Replace-by-Fee（手数料による置き換え）」の略です。ビットコインのトランザクションはRBFとして指定することができ、その場合、送信者はより高い手数料を支払う同様のトランザクションで当該トランザクションを置き換えられます。この仕組みは、ネットワークが混雑して手数料が予想外に上昇したときでも、ユーザーが対応できるようにするために存在します。もしユーザーが低い手数料でトランザクションを送信し、確定までに時間がかかりすぎると感じた場合、手数料を引き上げてトランザクションの承認を早めることができます。RBFが機能するのは、そのトランザクションが[メンプール](https://lostinbitcoin.sakuraweb.com/glossary/mempool/)に存在している間だけです。いったん[トランザクション](https://lostinbitcoin.sakuraweb.com/transaction/)が[ブロック](https://lostinbitcoin.sakuraweb.com/glossary/block/)に取り込まれると、手数料による置き換えはできません。RBFを使うには、最初に送る時点で「置き換えできるよ」という合図を入れておく必要があります。具体的には、各入力（input）に付いている小さな数値フィールド「nSequence」のうち、少なくとも1つを 0xfffffffe 未満の値に設定して送ります。これで「このトランザクションは、あとからより高い手数料のトランザクションに置き換えてOK」という意思表示になります。nSequenceはもともと、ブロードキャスト後にトランザクションを更新できるようにするための仕組みの一部です。[BIP 125 (RBF)](https://lostinbitcoin.sakuraweb.com/glossary/bip125/)も参照してください。


---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
