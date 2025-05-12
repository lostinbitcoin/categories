---
title: BIP 32 (階層型決定性ウォレット)
taxonomy:
    category:
        - glossary
---

## BIP 32 (Hierarchical Deterministic Wallets)
2,100 sats

BIP32は階層型決定性(HD)ウォレットの標準規格と拡張鍵を[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)に導入した[ビットコイン改善提案](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bip/)です。

BIP32のおかげで、ビットコイン[ウォレット](http://lostinbitcoin.jp.testrs.jp/staging/glossary/wallet/)は大幅に改善しました。まず、HDウォレットは[拡張秘密鍵](http://lostinbitcoin.jp.testrs.jp/staging/glossary/xprv/)１つを転送するだけで全ての鍵セットを別のウォレットに転送可能なため、ウォレットの相互運用性が飛躍的高まりました。

同様に、1つの[シード](http://lostinbitcoin.jp.testrs.jp/staging/glossary/seed/)でウォレット全体を復元できるので、ウォレットの復元性も向上しました。この改善は[BIP39](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bip39/)で拡張され、シードの保存と記憶が容易になりました。

また、BIP32によって、新規[アドレス](http://lostinbitcoin.jp.testrs.jp/staging/glossary/address/)の生成と保管が可能な閲覧専用ウォレットが作成できるようになりました。閲覧専用ウォレットはビットコインの受け取り、残高の確認、[トランザクション](http://lostinbitcoin.jp.testrs.jp/staging/glossary/transaction/)の生成が[秘密鍵](http://lostinbitcoin.jp.testrs.jp/staging/glossary/private_key/)不要で、秘密鍵を[コールドストレージ](http://lostinbitcoin.jp.testrs.jp/staging/glossary/cold_storage/)に保管したままできるため、安全性が高まりました。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
