---
title: 拡張秘密鍵 (Xprv)
taxonomy:
    category:
        - glossary
---

## Extended Private Key (Xprv)
2,100 sats

拡張秘密鍵はxprvとも表記され、[階層型決定性（HD）ウォレット](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bip32/)で子秘密鍵の生成に使われます。BIP32が実装されて以降、バックアップの利便性から、ほぼすべてのビットコイン[ウォレット](http://lostinbitcoin.jp.testrs.jp/staging/glossary/wallet/)がHDフォーマットを採用しています。マスター秘密鍵と呼ばれる拡張秘密鍵の1つだけをバックアップしておけば、ウォレット内のすべての公開鍵と秘密鍵を一括してバックアップ・復元できるのです。

マスター秘密鍵と拡張秘密鍵はよく混同されますが、マスター秘密鍵はHDウォレットの[シード](http://lostinbitcoin.jp.testrs.jp/staging/glossary/seed/)から直接生成される唯一の拡張秘密鍵で、HDツリーのルートに当たります。一方の拡張秘密鍵は子秘密鍵を生成できる秘密鍵を指し、1つのHDウォレットで無数に生成できます。

子秘密鍵が漏洩した場合、失うのはその鍵に関連する資金のみです。しかし、拡張秘密鍵が漏洩すると、それを基に生成されたすべての子秘密鍵に関連する資金が失われます。拡張秘密鍵はすべて'xprv'で始まり、その後に英数字からなる文字列が続きます。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
