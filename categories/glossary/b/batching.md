---
title: バッチ
taxonomy:
    category:
        - glossary
---

## Batching
2,100 sats

バッチまたはバッチ処理とは、複数の送金を 1 件の[トランザクション](http://lostinbitcoin.jp.testrs.jp/staging/glossary/transaction/)にまとめることを指します。[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)の[送金手数料](http://lostinbitcoin.jp.testrs.jp/staging/glossary/transaction_fee/)はトランザクションのデータサイズに基づくため、複数の送金を 1 件にまとめてデータ量を削減することで手数料が抑えられます。

例えば、アリスがボブに 0.5 BTC、チャーリーに 0.3 BTC、デビッドに 0.2 BTCを送金する場合、1 BTCのインプットに対して、送金先アドレスとおつりアドレスの ２ つのアウトプットを含むトランザクションを 3 件作成するより、3 つの送金先アドレスをアウトプットとする 1 件のトランザクションを作成する方が手数料を節約できます。

バッチ効果は規模に応じて大きくなります。例えば、取引所は顧客からの 100 件の出庫依頼を処理する際、トランザクションを 100 件作成してもよいですが、100 の送金先アドレスをアウトプットとするトランザクション 1 件作成することも可能です。後者は手数料を大幅に削減できます。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
