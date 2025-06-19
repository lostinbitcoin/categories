---
title: SegWit
taxonomy:
    category:
        - glossary
---

## SegWit
2,100 sats

SegWit（セグウィット：Segregated Witness）は、2017年に[ビットコイン](https://lostinbitcoin.sakuraweb.com/glossary/bitcoin/)で実施された[ソフトフォーク](https://lostinbitcoin.sakuraweb.com/glossary/soft_fork/)のアップグレードで、さまざまな重要な改善をもたらしました。その一例として、トランザクションの[マリアビリティ](https://lostinbitcoin.sakuraweb.com/glossary/malleability/)問題を解決しました。これは1つのトランザクションが複数の有効な[トランザクションID（txid）](https://lostinbitcoin.sakuraweb.com/glossary/txid/)を持つ可能性があった問題で、このアップグレードによってtxidが一意となり、[ライトニング・ネットワーク](https://lostinbitcoin.sakuraweb.com/glossary/lightning_network/)や[タップルート](https://lostinbitcoin.sakuraweb.com/glossary/taproot/)などの新たなイノベーションが可能になりました。

SegWitはまた、1つの[ブロック](https://lostinbitcoin.sakuraweb.com/glossary/block/)により多くの[トランザクション](https://lostinbitcoin.sakuraweb.com/glossary/transaction/)を含めることを可能にし、手数料の負担を軽減するとともに、スケーリング（処理能力向上）に関する部分的なソリューションを提供しました。

SegWitによる特筆すべき変更の一つは、Base58エンコーディングからBech32エンコーディングへの移行です。

技術的にはトランザクション本体に含まれていた[署名](https://lostinbitcoin.sakuraweb.com/glossary/signature/)部分であるScriptSigをトランザクションの別セクションであるWitnessセクションに移動することで、SegWitはマリアビリティを排除しています。このWitnessセクションは依然として[ブロックチェーン](https://lostinbitcoin.sakuraweb.com/glossary/blockchain-2/)上に保存されますが、SegWitを有効化した[ノード](https://lostinbitcoin.sakuraweb.com/glossary/node-2/)だけが利用します。

トランザクションID（txid）に影響を与えないように、Witness部分はトランザクション本体から分離されていますが、ブロックに含まれるWitnessが改ざんされないよう、Witnessを含むトランザクションID（wtxid）が計算されます。このwtxidを葉ノードとする[マークルツリー](https://lostinbitcoin.sakuraweb.com/glossary/merkle_tree/)を構成し、そのルートハッシュが各ブロックのコインベーストランザクションに記録されます。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
