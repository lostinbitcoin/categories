---
title: 未使用トランザクションアウトプット (UTXO)
taxonomy:
    category:
        - glossary
---

## UTXO
2,100 sats

未使用トランザクションアウトプット(UTXO)とは一定額の[ビットコイン](https://lostinbitcoin.sakuraweb.com/glossary/bitcoin/)の固まりです。

ビットコインでは口座や口座残高という考え方をしません。各個人が[ブロックチェーン](https://lostinbitcoin.sakuraweb.com/glossary/blockchain/)にちりぢりに記録されているUTXOを保有・管理します。UTXOはビットコイン[トランザクション](https://lostinbitcoin.sakuraweb.com/glossary/transaction/)にてインプット・アウトプットで使用される単位です。

UTXOはトランザクションで使用されると破棄され、1つまたは複数の新しいUTXOが作成されます。すべての[ノード](https://lostinbitcoin.sakuraweb.com/glossary/node/)はUTXOセットと呼ばれるブロックチェーンに存在する全てのUTXO情報を持っており、[承認](https://lostinbitcoin.sakuraweb.com/glossary/confirmation/)済みトランザクションがUTXOを生成・破棄するたびに更新されます。この仕組みによって各ノードはトランザクションが使おうとしているビットコインが有効かどうかを個別に検証することができます。

UTXOは現金に類似しており、UTXO使用時にチェンジ(邦訳：おつり)アウトプットが必要となる事が多いです。例えばアリスはボブに1BTCのUTXOから0.4BTCを支払いたい場合、アリスはインプットとして1BTC全てを使わなければなりません。0.4BTCはボブ、0.59BTCは自分(おつり)、残りの0.01BTCで[送金手数料](https://lostinbitcoin.sakuraweb.com/glossary/transaction_fee/)を支払ったものとします。この取引でUTXOが1つ消費され、新たに2つ作成されます。支払った送金手数料はアウトプットにならないことに注意してください。送金手数料はインプットの1BTCからアウトプットの合計0.99BTCの差額になります。マイナーはトランザクションから送金手数料を計算し、マイナー自身の報酬となるように[コインベース・トランザクション](https://lostinbitcoin.sakuraweb.com/glossary/coinbase_transaction/)のアウトプットに含めます。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
