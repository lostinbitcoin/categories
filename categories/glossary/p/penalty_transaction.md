---
title: ペナルティトランザクション
taxonomy:
    category:
        - glossary
---

## Penalty Transaction
2,100 sats

ペナルティトランザクションとは、[ライトニング・チャネル](http://lostinbitcoin.jp.testrs.jp/staging/glossary/lightning_channel/)の一方の当事者が、不正なチャネルクローズ中に盗まれた資金を取り戻すための仕組みです。ライトニング・チャネルで支払いを行う際、送信者は「コミットメントトランザクション」と呼ばれるビットコイントランザクションに署名し、これによってチャネルの残高を調整します。この新しい[トランザクション](http://lostinbitcoin.jp.testrs.jp/staging/glossary/transaction/)は受信者に送信されますが、[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)の[ブロックチェーン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/blockchain-2/)には記録されません。その後、将来のライトニング決済によって新しいコミットメントトランザクションが生成され、前のトランザクションは古いものと見なされます。しかし、元のトランザクションも依然として有効であるため、ブロックチェーンに記録される可能性があります。この場合ライトニング・チャネルは閉じられ、元のトランザクション以降に行われたすべてのライトニング決済が無効化されます。この仕組みによって、[ライトニング・ネットワーク](http://lostinbitcoin.jp.testrs.jp/staging/glossary/lightning_network/)上での盗用や[二重支払い](http://lostinbitcoin.jp.testrs.jp/staging/glossary/double_spend/)のリスクが存在することになります。

この問題を解決するため、コミットメントトランザクションは、たとえ古いコミットメントトランザクションがブロックチェーン上で承認された場合でも、同じチャネルから新しい有効なコミットメントトランザクションを提示できる場合、この新しいトランザクションを使って盗まれた資金を取り戻せるように設計されています。さらに、ペナルティトランザクションは悪意のあるユーザー側のチャネルに存在する全ての資金を没収できる仕組みです。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
