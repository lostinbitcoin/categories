---
title: CPFP
taxonomy:
    category:
        - glossary
---

## Child-Pays-for-Parent (CPFP)
2,100 sats

CPFPは、[トランザクション](https://lostinbitcoin.sakuraweb.com/glossary/transaction/)の確認速度を速める手法のことを指します。[RBF（Replace-by-Fee）](https://lostinbitcoin.sakuraweb.com/glossary/rbf/)と似た目的を持ちますが、RBFが送信者によってトランザクションの確認速度を向上させるのに対し、CPFPでは受信者がトランザクションの確認速度を向上させることができます。

もし送信者が低い手数料でトランザクションを送信し、そのトランザクションが十分な速さで[ブロック](https://lostinbitcoin.sakuraweb.com/glossary/block/)に取り込まれない場合、受信者は、未確認の状態でそのトランザクションの[ビットコイン](https://lostinbitcoin.sakuraweb.com/glossary/bitcoin/)を使用する新しいトランザクションを作成できます。(元のトランザクションがまだ[メンプール](https://lostinbitcoin.sakuraweb.com/glossary/mempool/)にある状態でも可能です。)この2番目のトランザクション（子トランザクション）で高い手数料を設定し、マイナーに対して「この子トランザクションを[マイニング](https://lostinbitcoin.sakuraweb.com/glossary/mining/)するには、まず最初のトランザクション（親トランザクション）もマイニングしなければならない。」と示すことになります。この仕組みにより、送信者が低い手数料を設定していても、受信者がトランザクションの確認速度を速めることができます。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
