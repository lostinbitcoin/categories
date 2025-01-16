---
title: vByte
taxonomy:
    category:
        - glossary
---

## vByte
2,100 sats

A vByte is a unit of measure for the weight of blocks and transactions. The vByte was introduced by the SegWit upgrade. A vByte is equivalent to 4 weight units, and thus, a block is limited to being 1 vMegabyte large, or 4 million weight units. Wallets usually calculate and display transaction fees in terms of sats/vByte, meaning the fee is paid per vByte of data used. Thus, the larger the transaction, the larger the total fee must be to ensure the desired speed of verification. This setup also makes SegWit transactions cheaper than regular transactions, as a byte of Witness data is only equivalent to 1 weight unit (1/4 vByte), while a byte of non-Witness data is 4 weight units (1 vByte).

vByte（vバイト）は、[ブロック](https://lostinbitcoin.jp/glossary/block/)と[トランザクション](https://lostinbitcoin.jp/glossary/transaction/)のデータ容量（重さ）を表す単位です。[SegWit](https://lostinbitcoin.jp/glossary/segwit/)アップグレードで新たに導入されました。1vバイトは4ウェイトユニットに相当するため、1ブロックの大きさは最大で1vメガバイト（400万ウェイトユニット）に制限されます。[送金手数料](https://lostinbitcoin.jp/glossary/transaction_fee/)は通常、ウォレットでsatsまたはvバイトで計算・表示され、使用データ量（vバイト単位）に応じて手数料が支払われる仕組みです。そのためトランザクションのデータ量が多いほど手数料も高くなり、迅速な取引を行うためにはそれに見合った手数料を支払う必要があります。SegWitを利用すると、通常の取引よりも手数料を抑えることができます。SegWitでは1vバイトの検証データ（Witnessデータ）が1ウェイトユニット（1/4 vバイト）として計算されるのに対し、通常取引の1vバイトの非検証データは4ウェイトユニット（1vバイト）として計算されるためです。この仕組みによって、SegWitは効率的かつ低コストな取引を実現します。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
