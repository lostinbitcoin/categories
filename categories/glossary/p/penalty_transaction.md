---
title: ペナルティトランザクション
taxonomy:
    category:
        - glossary
---

## Penalty Transaction
2,100 sats

ペナルティトランザクションとは、[ライトニング・チャネル](https://lostinbitcoin.sakuraweb.com/glossary/lightning_channel/)の一方の当事者が、不正なチャネルクローズ中に盗まれた資金を取り戻すための仕組みです。ライトニング・チャネルで支払いを行う際、送信者は「コミットメントトランザクション」と呼ばれるビットコイントランザクションに署名し、これによってチャネルの残高を調整します。この新しい[トランザクション](https://lostinbitcoin.sakuraweb.com/glossary/transaction/)は受信者に送信されますが、[ビットコイン](https://lostinbitcoin.sakuraweb.com/glossary/bitcoin/)の[ブロックチェーン](https://lostinbitcoin.sakuraweb.com/glossary/blockchain-2/)にはブロードキャストされません。その後、将来のライトニング決済によって新しいコミットメントトランザクションが生成され、前のトランザクションは古いものと見なされます。しかし、元のトランザクションも依然として有効であるため、ブロックチェーンにブロードキャストされる可能性があります。この場合ライトニング・チャネルは閉じられ、元のトランザクション以降に行われたすべてのライトニング決済が反映されなくなります。この仕組みによって、[ライトニング・ネットワーク](https://lostinbitcoin.sakuraweb.com/glossary/lightning_network/)上での盗用や[二重支払い](https://lostinbitcoin.sakuraweb.com/glossary/double_spend/)のリスクが存在することになります。

この問題を解決するため、コミットメントトランザクションは、たとえ古いコミットメントトランザクションがブロックチェーン上で承認された場合でも、同じチャネルから新しい有効なコミットメントトランザクションを提示できる場合、この新しいトランザクションを使って盗まれた資金を取り戻せるように設計されています。さらに、ペナルティトランザクションは悪意のあるユーザー側のチャネルに存在する全ての資金を没収できる仕組みです。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
