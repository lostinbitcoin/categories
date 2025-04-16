---
title: トランザクション
taxonomy:
    category:
        - glossary
---

## Transaction
2,100 sats

トランザクションは[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)の移動の記録です。全てのトランザクションは[ブロックチェーン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/blockchain/)の[ブロック](http://lostinbitcoin.jp.testrs.jp/staging/glossary/block/)の中に記録されます。ほとんどのユーザはビットコイントランザクションを送ったり、受け取ったりするのに[ウォレット](http://lostinbitcoin.jp.testrs.jp/staging/glossary/wallet/)を使います。ウォレットがバックグラウンドで技術的な作業を行うので、ユーザは[アドレス](http://lostinbitcoin.jp.testrs.jp/staging/glossary/address/)と金額を簡単に指定できます。

準備が整うとトランザクションはビットコインネットワーク上の[ノード](http://lostinbitcoin.jp.testrs.jp/staging/glossary/node/)にブロードキャストされます。マイナーがトランザクションをブロックに追加するまでの間、ノードはトランザクションを[mempool](http://lostinbitcoin.jp.testrs.jp/staging/glossary/mempool/)に保持します。mempoolは[承認](http://lostinbitcoin.jp.testrs.jp/staging/glossary/confirmation/)が保留されているトランザクションのプールです。承認されると、トランザクションはブロックに追加されます。トランザクションが確定したとみなすときの安全な方法は、少なくとも6ブロック経つまで待つことです。

トランザクションは、3つのパートで構成されます。インプット、アウトプット、[署名](http://lostinbitcoin.jp.testrs.jp/staging/glossary/signature/)です。インプットは支払者が使うと決めた[UTXO](http://lostinbitcoin.jp.testrs.jp/staging/glossary/utxo/)と呼ばれるビットコインの一部です。アウトプットは指定されたアドレスに指定された金額のビットコインを送り、新しいUTXOを作ります。ひとつのトランザクションは複数のインプットと複数のアウトプットを持つことができます。最後に、トランザクションを有効にするために、支払者はトランザクションに署名しなければなりません。これにより、支払いに使うインプットが自分のものであることを証明します。この署名は支払い者の[秘密鍵](http://lostinbitcoin.jp.testrs.jp/staging/glossary/private_key/)を使って作られます。

トランザクションの例を見てみましょう。アリスが1BTCのUTXOを持っていて、ボブに0.4BTC払いたいとします。彼女はインプットとして1BTCのUTXOを使います。アリスは2つのアウトプットを作ります。1つ目はボブへ送る0.4BTC、2つ目は彼女自身への0.59BTCのおつりとなるアウトプットです。この例では、0.01BTCが[送金手数料](http://lostinbitcoin.jp.testrs.jp/staging/glossary/transaction_fee/)として支払われます。送金手数料はアウトプットではありません。インプットの合計（1BTC）からアウトプットの合計（0.4＋0.59＝0.99）引いたものであり、これはマイナーのものになります。

最後に、アリスはトランザクションをブロードキャストする前に、インプットのUTXOを制御できる秘密鍵でトランザクションに署名します。このトランザクションがブロックチェーンに追加されると、1BTCのUTXOは削除されて、新しく0.4BTCと0.59BTCのUTXOが生成されます。0.4BTCのUTXOはボブが、0.59BTCのUTXOはアリスが所有します。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
