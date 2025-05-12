---
title: ライトニング・ネットワーク・ペナルティ
taxonomy:
    category:
        - glossary
---

## Lightning Network Penalty
2,100 sats

ライトニング・ネットワーク・ペナルティは、[ライトニング・ネットワーク（LN）](http://lostinbitcoin.jp.testrs.jp/staging/glossary/lightning_network/)内での不正行為、特に[二重支払い](http://lostinbitcoin.jp.testrs.jp/staging/glossary/double_spend/)を試みる行為を抑止する仕組みです。このペナルティは、過去の無効なチャネルの状態を公開して資金を盗もうとした者から、[ライトニング・チャネル](http://lostinbitcoin.jp.testrs.jp/staging/glossary/lightning_channel/)の全額を没収することで機能します。

ライトニング・ネットワークでは、完全に[署名](http://lostinbitcoin.jp.testrs.jp/staging/glossary/signature/)された[トランザクション](http://lostinbitcoin.jp.testrs.jp/staging/glossary/transaction/)を用いて当事者間で[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)を送受信します。これらのトランザクションは通常、ビットコインの[ブロックチェーン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/blockchain-2/)には公開・追加されません。しかし有効なトランザクションであるため、いつでもブロックチェーンに記録可能です。ブロックチェーンに記録した時点でライトニング・チャネルは閉じられ、その後に行われたライトニング・トランザクションは無効となります。

この仕組みを悪用すると、ライトニング・ネットワークで二重支払いが可能になります。例えば、アリスとボブがそれぞれ0.25BTCを持つライトニング・チャネルを開設したとします。この時点で、両者の残高（0.25BTCずつ）を反映するコミットメント・トランザクションが存在します。その後アリスがボブに0.05BTCを送金すると、アリスの残高は0.20BTC、ボブの残高は0.30BTCとなり、新しいコミットメント・トランザクションがこの変更を記録します。しかし、アリスが意図的に古いコミットメント・トランザクションをブロックチェーンに記録すると、両者の残高は再び0.25BTCずつと見なされ、アリスが送金した0.05BTCが無効化されることになってしまいます。これによりアリスはボブに送金した資金を実質的に取り戻すことになり、不正な利益を得ることができます。

これを防ぐため、ライトニングプロトコルではボブが一定期間内に新しいコミットメント・トランザクションを公開することで、不正に送信された0.05BTCだけでなくチャネル内の全額（0.5BTC）をボブが没収できるように設計されています。このペナルティによって、アリスによる二重支払いの試みが罰せられる仕組みとなっています。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
