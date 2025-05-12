---
title: ビザンチン障害耐性
taxonomy:
    category:
        - glossary
---

## Byzantine Fault Tolerance (BFT)
2,100 sats

ビザンチン障害耐性（BFT）とは、不正や誤情報を識別して拒否できる分散型かつパーミッションレスなシステムの特徴です。ビザンチン障害耐性を有するシステムは、[ビザンチン将軍問題](http://lostinbitcoin.jp.testrs.jp/staging/glossary/byzantine_generals_problem/)を克服するとともに、[シビル攻撃](http://lostinbitcoin.jp.testrs.jp/staging/glossary/sybil_attack/)に対しても堅牢です。

誰でも自由に参加して情報を発信できる分散型パーミッションレスシステムにはビザンチン障害耐性が不可欠です。ビザンチン障害耐性がないネットワークは、参加者が発信する不正な情報を検知、排除できないため、ネットワークの信頼性が担保できません。分散型かつパーミッションレスな[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)も、誰でも自由に[ノード](http://lostinbitcoin.jp.testrs.jp/staging/glossary/node/)を運用してネットワークに参加でき、[ブロック](http://lostinbitcoin.jp.testrs.jp/staging/glossary/block/)や[トランザクション](http://lostinbitcoin.jp.testrs.jp/staging/glossary/transaction/)をブロードキャストできます。ノードは同一のビットコインをインプットとする2件のトランザクションをブロードキャストして、[二重支払い](http://lostinbitcoin.jp.testrs.jp/staging/glossary/double_spend/)を試みるかもしれません。各ノードが他のノードから受信したデータの有効性を独自に判断できれば、こうした不正は防げます。

ビットコインネットワークに参加する各ノードは、すべてのトランザクションとブロックを独自かつ客観的に検証できます。つまり、ビットコインにはビザンチン障害耐性があります。あるノードが無効なブロックやトランザクションをブロードキャストしても、他のノードは個別にそれらの有効性を検証し、[ブロックチェーン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/blockchain/)への登録を拒否します。ビザンチン障害耐性のおかげで、無効なブロックやトランザクションが弾かれるため、ビットコインブロックチェーンに記録されたデータは常に有効性が担保されています。この明確なデータの有効性が、ビットコインを事実に基づく客観的な規則に基づくネットワークたらしめています。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
