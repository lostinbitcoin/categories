---
title: [ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)スクリプト
taxonomy:
    category:
        - glossary
---

## Bitcoin Script
2,100 sats

[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)のスクリプト言語は単にスクリプト（Script）と呼ばれ、[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)は全てスクリプトで書かれています。このスクリプトは非常にシンプルで、ループを含むいくつかの論理機能を欠いているため「チューリング完全」ではありません。つまり、理論上あらゆる計算を実行できる能力を「持たない」設計となっています。ループなど一部の論理機能を敢えて省いている理由は、ビットコインスクリプトが過剰な計算リソースを消費してネットワーク全体に過剰な負荷をかけないようにするためです。

ビットコインスクリプトは主に[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)のロック（送金時の条件設定）およびアンロック（着金後の条件解除）に使用され、アプリケーションやプログラムを構築するために使われることはほとんどありません。このシンプルさは[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)のセキュリティを高め、開発者が[ウォレット](http://lostinbitcoin.jp.testrs.jp/staging/glossary/wallet-2/)や[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)関連アプリを設計する際に、資金を失うリスクを最小限に抑える助けとなります。

[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)のすべての[トランザクション](http://lostinbitcoin.jp.testrs.jp/staging/glossary/transaction/)においてスクリプトは出力条件を決定するために使用され、[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)が誰に送られるかを決定する役割を果たしています。最も一般的なスクリプト形式はPay-to-Public-Key-Hash（P2PKH）であり、これは[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)を[アドレス](http://lostinbitcoin.jp.testrs.jp/staging/glossary/address/)に送るシンプルなスクリプトです。

その他のスクリプトでは、[マルチシグ](http://lostinbitcoin.jp.testrs.jp/staging/glossary/multisig/)アドレスの作成など、より複雑な設定を実現できます。マルチシグアドレスに送られた[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)を使用するには、複数の[秘密鍵](http://lostinbitcoin.jp.testrs.jp/staging/glossary/private_key/)による署名が必要です。

[SegWit](http://lostinbitcoin.jp.testrs.jp/staging/glossary/segwit/)のスクリプトタイプ（P2WPKHおよびP2WSH）は[送金手数料](http://lostinbitcoin.jp.testrs.jp/staging/glossary/transaction_fee/)を削減できる一方で、このスクリプトタイプの採用は遅れています。SegWitが有効化されてから約4年が経過しましたが、2021年4月時点では70%以上の[未使用トランザクションアウトプット(UTXO)](http://lostinbitcoin.jp.testrs.jp/staging/glossary/utxo/)で依然としてP2PKHスクリプトが使用されています。

![](/_images/glossary-ha_1.png)

ソース: [Clark Moody's Dashboard](https://bitcoin.clarkmoody.com/dashboard/)

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
