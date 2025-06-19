---
title: 承認
taxonomy:
    category:
        - glossary
---

## Confirmation
2,100 sats

承認とは、[ビットコイン](https://lostinbitcoin.sakuraweb.com/glossary/bitcoin/)トランザクションが[ブロックチェーン](https://lostinbitcoin.sakuraweb.com/glossary/blockchain/)に追加されることを指します。[トランザクション](https://lostinbitcoin.sakuraweb.com/glossary/transaction/)は一旦承認されると、それ以降に生成される[ブロック](https://lostinbitcoin.sakuraweb.com/glossary/block/)からも順次承認されます。承認回数が増えるほど、トランザクションの取り消しや置き換えは困難になります。一般的にトランザクションは6承認をもって最終決済と見なされます。

[ウォレット](https://lostinbitcoin.sakuraweb.com/glossary/wallet/)で生成され、ビットコインネットワークにブロードキャストされたトランザクションは、即時決済されるわけではなく、まず未承認または保留中トランザクションとして[mempool](https://lostinbitcoin.sakuraweb.com/glossary/mempool/)に入ります。マイナーはブロック生成時、収益性が高い、つまり、単位データあたりの送金手数料が高いトランザクションからブロックに取り込みます。トランザクションがブロックに取り込まれると、mempoolから削除されて承認済みと見なされます。

ただし、この時点ではトランザクションはまだ1承認しか得ていません。2～6回承認されるまでは、取り消しや置き換えが可能と考えた方が安全です。1承認しか得ていないトランザクションは、取り込まれたブロックが上書きされて[オーファンブロック](https://lostinbitcoin.sakuraweb.com/glossary/orphan_block/)と化す可能性が否定できません。オーファンブロックに含まれるトランザクションは、mempoolに戻されて再び保留状態になります。保留中の未承認トランザクションを受金完了、決済完了として処理するのは危険です。同じビットコインをインプットとする、より高い手数料を支払う別のトランザクションに置き換えられる可能性があるからです。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
