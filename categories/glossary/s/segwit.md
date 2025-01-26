---
title: SegWit
taxonomy:
    category:
        - glossary
---

## SegWit
2,100 sats

SegWit（セグウィット：Segregated Witness）は、2017年にビットコインで実施された[ソフトフォーク](https://lostinbitcoin.jp/glossary/soft_fork/)のアップグレードで、さまざまな重要な改善をもたらしました。その一例として、トランザクションの[マリアビリティ](https://lostinbitcoin.jp/glossary/malleability/)問題を解決しました。これは1つのトランザクションが複数の有効な[トランザクションID（txid）](https://lostinbitcoin.jp/glossary/txid/)を持つ可能性があった問題で、このアップグレードによってtxidが一意となり、[ライトニング・ネットワーク](https://lostinbitcoin.jp/glossary/lightning_network/)や[タップルート](https://lostinbitcoin.jp/glossary/taproot/)などの新たなイノベーションが可能になりました。

SegWitはまた、1つの[ブロック](https://lostinbitcoin.jp/glossary/block/)により多くの[トランザクション](https://lostinbitcoin.jp/glossary/transaction/)を含めることを可能にし、手数料の負担を軽減するとともに、スケーリング（処理能力向上）に関する部分的なソリューションを提供しました。

SegWitによる特筆すべき変更の一つは、Base58エンコーディングからBech32エンコーディングへの移行です。

技術的にはトランザクション本体に含まれていた[署名](https://lostinbitcoin.jp/glossary/signature/)部分であるScriptSigをトランザクションの別セクションであるWitnessセクションに移動することで、SegWitはマリアビリティを排除しました。このWitnessセクションは依然として[ブロックチェーン](https://lostinbitcoin.jp/glossary/blockchain-2/)上に保存されますが、SegWitを有効化した[ノード](https://lostinbitcoin.jp/glossary/node-2/)だけが利用します。

トランザクションID（txid）に影響を与えないように、Witness部分はトランザクション本体から分離されていますが、ブロックに含まれるWitnessが改ざんされないよう、Witness専用のトランザクションID（wtxid）が計算されます。このwtxidは、各ブロックのコインベーストランザクションの出力に記録される[マークルツリー](https://lostinbitcoin.jp/glossary/merkle_tree/)に含まれます。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
