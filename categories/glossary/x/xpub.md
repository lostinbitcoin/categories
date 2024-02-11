---
title: 拡張公開鍵 (Xpub)
taxonomy:
    category:
        - glossary
---

## Extended Public Key (Xpub)
2,100 sats

拡張公開鍵とは、[階層型決定性（HD）ウォレット](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bip32/)が子公開鍵の生成に使う[公開鍵](http://lostinbitcoin.jp.testrs.jp/staging/glossary/public_key/)です。拡張公開鍵は[BIP](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bip/)32が定義するビットコインの標準規格であり、主に公開鍵を生成するために[ウォレット](http://lostinbitcoin.jp.testrs.jp/staging/glossary/wallet/)が背後で使用します。

拡張公開鍵を信頼できる第三者と共有することで利便性は高まりますが、信頼できない事業者や個人には共有すべきではありません。共有した相手は拡張公開鍵から導出した公開鍵を追跡して、あなたの過去の[トランザクション](http://lostinbitcoin.jp.testrs.jp/staging/glossary/transaction/)だけでなく、将来のトランザクションもすべて検閲できるからです。

拡張公開鍵をオンラインで管理し、万が一流出したとしても、ビットコインが盗まれることはありません（プライバシーは損なわれます）。拡張公開鍵から[秘密鍵](http://lostinbitcoin.jp.testrs.jp/staging/glossary/private_key/)を割り出すことは不可能だからです。拡張公開鍵は秘密鍵を[ハードウェアウォレット](http://lostinbitcoin.jp.testrs.jp/staging/glossary/hardware_wallet/)などの[コールドストレージ](http://lostinbitcoin.jp.testrs.jp/staging/glossary/cold_storage/)で管理する人にとって特に便利です。オンラインの拡張公開鍵から新規[アドレス](http://lostinbitcoin.jp.testrs.jp/staging/glossary/address/)を生成することで、秘密鍵をオフラインで保ったまま、コールドウォレットに直接ビットコインを受け取れます。

拡張公開鍵はどれも「xpub」で始まり、その後に長い英数字が続きます。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
