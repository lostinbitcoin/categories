---
title: vByte
taxonomy:
    category:
        - glossary
---

## vByte
2,100 sats

vByte（vバイト）は、[ブロック](http://lostinbitcoin.jp.testrs.jp/staging/glossary/block/)と[トランザクション](http://lostinbitcoin.jp.testrs.jp/staging/glossary/transaction/)のデータ容量（重さ）を表す単位です。[SegWit](http://lostinbitcoin.jp.testrs.jp/staging/glossary/segwit/)アップグレードで新たに導入されました。1vバイトは4ウェイトユニットに相当するため、1ブロックの大きさは最大で1vメガバイト（400万ウェイトユニット）に制限されます。[送金手数料](http://lostinbitcoin.jp.testrs.jp/staging/glossary/transaction_fee/)は通常、[ウォレット](http://lostinbitcoin.jp.testrs.jp/staging/glossary/wallet/)では、sats/vByte（サトシ/vバイト）の単位で手数料を計算・表示し、使用データ量（vバイト単位）に応じて手数料が支払われる仕組みです。そのためトランザクションのデータ量が多いほど手数料も高くなり、迅速な取引を行うためにはそれに見合った手数料を支払う必要があります。SegWitを利用すると、通常のトランザクションよりも手数料を抑えることができます。SegWitではWitnessデータの1バイトが1ウェイトユニット（1/4 vバイト）で計算されるのに対し、通常トランザクションの1vバイトの非検証データは4ウェイトユニット（1vバイト）として計算されるためです。この仕組みによって、SegWitは効率的かつ低コストなトランザクションを実現します。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
