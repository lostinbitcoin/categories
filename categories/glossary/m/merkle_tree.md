---
title: マークルツリー
taxonomy:
    category:
        - glossary
---

## Merkle Tree
2,100 sats

マークルツリーとは、[ビットコイン](https://lostinbitcoin.sakuraweb.com/glossary/bitcoin-2/)において有用となる特有の性質を持つデータ構造です。マークルツリーは、特定の[ブロック](https://lostinbitcoin.sakuraweb.com/glossary/block/)内に含まれるすべての[トランザクション](https://lostinbitcoin.sakuraweb.com/glossary/transaction/)を保存するために使用されます。この仕組みの利点は、ある[ノード](https://lostinbitcoin.sakuraweb.com/glossary/node-2/)が、特定のトランザクションが特定のブロックに含まれていたことを、別のノードに対して容易に証明できる点にあります。これは、[ブロックチェーン](https://lostinbitcoin.sakuraweb.com/glossary/blockchain-2/)全体を保存せず、特定のトランザクションやブロックのみに関心を持つ[SPV](https://lostinbitcoin.sakuraweb.com/glossary/spv/)ノードや[軽量クライアント](https://lostinbitcoin.sakuraweb.com/glossary/light_client/)にとって有用です。
たとえば、アリスが[ウォレット](https://lostinbitcoin.sakuraweb.com/glossary/wallet-2/)を使用していて自身のトランザクションの[承認](https://lostinbitcoin.sakuraweb.com/glossary/confirmation/)を待っているが、ノードを運用していない場合、[ビットコインノード](https://lostinbitcoin.sakuraweb.com/glossary/bitcoin_node/)を運用するボブに対してマークル証明を要求することができます。この証明により、ボブがすべてのトランザクションやブロック全体をアリスに共有する必要なく、アリスは関心のあるトランザクションが有効なブロックに含まれていたことを確認できます。

技術的な観点から見ると、マークルツリーは複数の層を持っています。最初の層は、ブロック内にあるすべての[トランザクションID（TXID）](https://lostinbitcoin.sakuraweb.com/glossary/txid/)の一覧です。2番目の層を生成するために、これらのtxidはペアごとに連結され、[SHA-256](https://lostinbitcoin.sakuraweb.com/glossary/sha_256/)を用いてハッシュ化されます。その結果、2番目の層の長さは最初の層の半分になります。この処理は、最後の層にちょうど 1つのハッシュが含まれるまで続けられます。この最終的なハッシュをマークルルートと呼びます。[ハッシュ関数](https://lostinbitcoin.sakuraweb.com/glossary/hash_function/)の性質により、1つのトランザクションIDが変更されると、その変更はツリー全体に伝播し、ルートハッシュは完全に変化します。

![](/_images/glossary-ma_1.png)

マークルツリーの利点は、マークルツリー全体を開示することなく、特定のトランザクションIDがマークルツリーに含まれていることを証明できる点にあります。たとえば、8件のトランザクションを含むマークルツリーでは、あるtxidがそのツリーに含まれていることを証明するために、3つのハッシュを提示するだけで十分です。これは、ブロックチェーン全体を保存しておらず、特定のトランザクションが承認されていることの証明を他のノードに問い合わせる必要がある軽量クライアントにとって、高い効率性を提供します。

![](/_images/glossary-ma_2.png)

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
