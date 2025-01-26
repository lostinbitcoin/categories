---
title: タップルート
taxonomy:
    category:
        - glossary
---

## Taproot
2,100 sats

タップルートは、ビットコインに新機能を導入するために提案されたアップグレードです。このアップグレードはビットコイン改善提案（BIP） 340、341、342で定義されており、[シュノア署名](https://lostinbitcoin.jp/glossary/schnorr_signature/)、タップルート、タップスクリプトという新しい技術を導入するものです。これらを組み合わせることで、ビットコイン取引をより効率的で柔軟かつプライバシー保護に優れた形に進化させます。シュノア署名は、従来のデジタル署名方式である[ECDSA](https://lostinbitcoin.jp/glossary/ecdsa/)と比べて効率が良く、安全性が高く、検証速度が速いという特長があります。さらに、シュノア署名は[MuSig](https://lostinbitcoin.jp/glossary/musig/)と呼ばれる新しいマルチシグネチャ方式を可能にします。これにより、複数人で署名する[マルチシグ](https://lostinbitcoin.jp/glossary/multisig/)取引のプライバシーが大幅に向上し、取引手数料の削減も期待できます。タップルートは、シュノア[公開鍵](https://lostinbitcoin.jp/glossary/public_key/)への送金やその公開鍵からの支払いだけでなく、複数のスクリプトへの送金を一度に行うことも可能にします。この機能を実現するために、Pay-to-Taproot（P2TR）と呼ばれる新しいScriptPubKeyの形式が定義されます。これらのアドレスは、SegWit v1形式とBech32エンコーディングを採用します。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
