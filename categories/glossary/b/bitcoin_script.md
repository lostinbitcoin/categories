---
title: ビットコインスクリプト
taxonomy:
    category:
        - glossary
---

## Bitcoin Script
2,100 sats

ビットコインのスクリプト言語は単にスクリプト（Script）と呼ばれ、ビットコインは全てスクリプトで書かれています。このスクリプトは非常にシンプルで、ループを含むいくつかの論理機能を欠いているため「チューリング完全」ではありません。つまり、理論上あらゆる計算を実行できる能力を「持たない」設計となっています。ループなど一部の論理機能を敢えて省いている理由は、ビットコインスクリプトが過剰な計算リソースを消費してネットワーク全体に過剰な負荷をかけないようにするためです。

ビットコインスクリプトは主にビットコインのロック（送金時の条件設定）およびアンロック（着金後の条件解除）に使用され、アプリケーションやプログラムを構築するために使われることはほとんどありません。このシンプルさはビットコインのセキュリティを高め、開発者が[ウォレット](https://lostinbitcoin.jp/glossary/wallet-2/)やビットコイン関連アプリを設計する際に、資金を失うリスクを最小限に抑える助けとなります。

ビットコインのすべての[トランザクション](https://lostinbitcoin.jp/glossary/transaction/)においてスクリプトは出力条件を決定するために使用され、ビットコインが誰に送られるかを決定する役割を果たしています。最も一般的なスクリプト形式はPay-to-Public-Key-Hash（P2PKH）であり、これはビットコインを[アドレス](https://lostinbitcoin.jp/glossary/address/)に送るシンプルなスクリプトです。

その他のスクリプトでは、[マルチシグ](https://lostinbitcoin.jp/glossary/multisig/)アドレスの作成など、より複雑な設定を実現できます。マルチシグアドレスに送られたビットコインを使用するには、複数の[秘密鍵](https://lostinbitcoin.jp/glossary/private_key/)による署名が必要です。

[SegWit](https://lostinbitcoin.jp/glossary/segwit/)のスクリプトタイプ（P2WPKHおよびP2WSH）は取引手数料を削減できる一方で、このスクリプトタイプの採用は遅れています。SegWitが有効化されてから約4年が経過しましたが、2021年4月時点では70%以上の[未使用トランザクションアウトプット(UTXO)](https://lostinbitcoin.jp/glossary/utxo/)で依然としてP2PKHスクリプトが使用されています。

![](/_images/glossary-ha_1.png)

ソース: [Clark Moody's Dashboard](https://bitcoin.clarkmoody.com/dashboard/)

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
