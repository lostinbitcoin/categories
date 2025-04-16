---
title: 送金手数料
taxonomy:
    category:
        - glossary
---

## Transaction Fee
2,100 sats

[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)の送金を指示する[トランザクション](http://lostinbitcoin.jp.testrs.jp/staging/glossary/transaction/)を、[マイニング](http://lostinbitcoin.jp.testrs.jp/staging/glossary/mining/)を介して[ブロックチェーン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/blockchain/)に取り込んでもらうためには、送金手数料を支払う必要があります。送金手数料は[ブロック報酬](http://lostinbitcoin.jp.testrs.jp/staging/glossary/block_subsidy/)と並び、マイナーにマイニングを促すインセンティブを形成しています。トランザクションが支払う手数料が高いほど、マイナーが[ブロック](http://lostinbitcoin.jp.testrs.jp/staging/glossary/block/)に含めるインセンティブが大きくなるため、迅速に処理、承認されます。

マイナーは各ブロックに最大 4MB※ のデータしか格納できないため、送金手数料の合計ではなく、手数料とバイトの比率（sats/vByte、satoshi建て手数料/仮想バイト）に基づいてトランザクションを評価します。したがって、ほとんどの[ウォレット](http://lostinbitcoin.jp.testrs.jp/staging/glossary/wallet/)では送金手数料をsats/vByteで表示されます。

送金手数料は大きく変動します。迅速な[承認](http://lostinbitcoin.jp.testrs.jp/staging/glossary/confirmation/)を得るために高い手数料を支払うトランザクションもあれば、承認に数時間〜数日要するのを覚悟で低い手数料を支払うトランザクションもあります。

将来的にはビットコインネットワーク上での取引需要が高まるにつれて送金手数料が上昇すると予想されています。手数料を節約する方法としては、[UTXO](http://lostinbitcoin.jp.testrs.jp/staging/glossary/utxo/)の統合、複数トランザクションの一括処理、[SegWit](http://lostinbitcoin.jp.testrs.jp/staging/glossary/segwit/) など最新トランザクションタイプの使用などがあります。

※原則 1MB とされているものの、SegWit 導入により最大 4MB まで格納可能となっています。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
