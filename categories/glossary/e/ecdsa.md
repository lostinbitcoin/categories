---
title: ECDSA
taxonomy:
    category:
        - glossary
---

## ECDSA
2,100 sats

ECDSA（楕円曲線デジタル署名アルゴリズム）は、[公開鍵](http://lostinbitcoin.jp.testrs.jp/staging/glossary/public_key/)と[秘密鍵](http://lostinbitcoin.jp.testrs.jp/staging/glossary/private_key/)を使用してデジタル署名を生成する暗号化方式の一つです。すべての[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)の鍵と署名はECDSAを使用して生成されています（※注：[Taproot](http://lostinbitcoin.jp.testrs.jp/staging/glossary/taproot/)アップグレード後は[シュノア署名](http://lostinbitcoin.jp.testrs.jp/staging/glossary/schnorr_signature/)が正式に[ビットコインプロトコル](http://lostinbitcoin.jp.testrs.jp/staging/glossary/protocol/)に統合）。ECDSAは、ある人物が公開鍵を公開し、その秘密鍵でデータに[署名](http://lostinbitcoin.jp.testrs.jp/staging/glossary/signature/)することで、そのデータが公開鍵の所有者によって署名されたことを誰もが検証できる仕組みです。公開鍵や署名から秘密鍵を導き出すことは不可能であり、ある署名を使用して他のデータの署名として偽造することもできません。

ビットコインのすべての[トランザクション](http://lostinbitcoin.jp.testrs.jp/staging/glossary/transaction/)は、この強力なセキュリティ機能を用いて署名されています。楕円曲線とは、y^2 = x^3 + ax + bの形式で表される数学の関数です。ビットコインの場合、特定の曲線であるy^2 = x^3 + 7（a = 0, b = 7）を使用します。この楕円曲線は「secp256k1」と呼ばれ、この曲線上の点は、すべて有効なビットコインの公開鍵として機能します。

公開鍵を生成するには、ユーザーが大きな数値を秘密鍵として生成する必要があります。この秘密鍵に「ジェネレータポイント」と呼ばれる定義済みの点を「点乗算」して公開鍵を計算します。点乗算は通常の掛け算とは異なり、公開鍵から秘密鍵を逆算すること（点除算）は不可能です。この仕組みがECDSAのセキュリティの基盤となっています。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
