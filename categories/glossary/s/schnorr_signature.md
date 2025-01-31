---
title: シュノア署名
taxonomy:
    category:
        - glossary
---

## Schnorr Signature
2,100 sats

シュノア署名は、[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)で初期から使用されている[ECDSA](http://lostinbitcoin.jp.testrs.jp/staging/glossary/ecdsa/)（楕円曲線デジタル署名アルゴリズム）に似たデジタル署名の方式です。シュノア署名にはECDSAと比べて複数のの利点があり、現在は[タップルート](http://lostinbitcoin.jp.testrs.jp/staging/glossary/taproot/)（アップグレード）を通じてビットコインへの実装が進められています。

シュノア署名の利点の一つは安全性が証明されており、非改ざん性を備えている点です。これらはECDSAに対する重要な改良点とされています。シュノア署名はECDSAに比べて検証時間が短く、効率的です。また、シュノア署名では複数の[秘密鍵](http://lostinbitcoin.jp.testrs.jp/staging/glossary/private_key/)を持つ当事者が1つのメッセージに対して効率的に署名を作成できます。この特性により、シュノア署名は複数の署名を一括で検証する「[バッチ](http://lostinbitcoin.jp.testrs.jp/staging/glossary/batching/)検証」が可能となり、検証プロセスがさらに高速化します。

署名と公開鍵の集約機能は、プライバシーの向上にも寄与します。シュノア署名を使用することで取引に含まれる署名数を隠すことができ、[トランザクション](http://lostinbitcoin.jp.testrs.jp/staging/glossary/transaction/)の[匿名性](http://lostinbitcoin.jp.testrs.jp/staging/glossary/anonymity/)が高まります。さらに、シュノア署名はECDSAよりもサイズが小さいため、手数料削減も可能です。

ビットコインの開発当初、シュノア署名は特許で保護されていました。そのため、[サトシ・ナカモト](http://lostinbitcoin.jp.testrs.jp/staging/glossary/satoshi_nakamoto/)はECDSAをビットコインの署名方式として採用しました。しかし、その後シュノア署名の特許が失効し、現在ではビットコインへの実装が進められています。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
