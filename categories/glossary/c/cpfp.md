---
title: CPFP
taxonomy:
    category:
        - glossary
---

## Child-Pays-for-Parent (CPFP)
2,100 sats

Child-Pays-for-Parent is a transaction mechanism with a similar purpose as Replace-by-Fee (RBF). While RBF allows the sender to speed up a transaction’s confirmation, Child-Pays-for-Parent allows the recipient to speed up the transaction’s confirmation.

In case a transaction is sent with a low fee and is not being confirmed fast enough for the recipient’s liking, the recipient may create a new transaction spending the bitcoin they received in the previous transaction (even though it is still unconfirmed in the mempool). This second transaction will pay a higher fee and signal to miners that they must mine the first transaction first in order to mine the second transaction. In this way, the recipient will receive their funds faster despite the low fee paid by the sender.

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
