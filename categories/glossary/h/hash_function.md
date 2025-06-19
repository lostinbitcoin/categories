---
title: ハッシュ関数
taxonomy:
    category:
        - glossary
---

## Hash Function
2,100 sats

暗号ハッシュ関数には多くの種類がありますが、すべての暗号ハッシュ関数に共通するいくつかの重要な性質があります。

- すべての暗号ハッシュ関数は入力値を受け取り、ハッシュまたはダイジェストと呼ばれる一定の長さの出力値を生成します。この長さは、使用する関数によって変わります。
- 暗号ハッシュ関数の出力値は**決定論的**であり、与えられた入力値に対して、出力値は常に全く同じになります。
- 暗号ハッシュ関数は**一方向性関数**であり、入力値から出力値は簡単に計算できます。しかし、与えられた出力値から入力値を逆算することはできません。
- 出力値は**ランダム**で**予測不可能**であり、特定の出力値を得るための入力値を見つけ出すことは非常に困難です。また、一連の入力値とその出力値の関係性は予測不可能です。例えば、100文字の入力値を1文字だけ変更した場合、新しい出力値は古い出力値とは全く異なるものになります。

このような特性を持つ暗号ハッシュ関数は、[ビットコイン](https://lostinbitcoin.sakuraweb.com/glossary/bitcoin/)にとって非常に有用です。ハッシュはランダムで制御できないため、ビットコインの[マイニング](https://lostinbitcoin.sakuraweb.com/glossary/mining/)が公正な競争であることを保証します。[公開鍵](https://lostinbitcoin.sakuraweb.com/glossary/public_key/)や[アドレス](https://lostinbitcoin.sakuraweb.com/glossary/address/)を取得するためのスクリプトをハッシュ化することで、優れたセキュリティ、プライバシー、利便性をユーザーに提供します。また、取引と[ブロック](https://lostinbitcoin.sakuraweb.com/glossary/block/)をハッシュ化することで、取引とブロックの両方に普遍的でユニークなIDが作成できます。そして、[Merkle Trees](https://lostinbitcoin.sakuraweb.com/glossary/merkle_tree/)はハッシュを使用して、ブロック内のすべての[トランザクション](https://lostinbitcoin.sakuraweb.com/glossary/transaction/)から信頼性の高い、改ざん不可能なマークルルート値を算出します。これにより、マイニングとブロックの検証が大幅に効率化できます。

ビットコインには、数種類のハッシュ関数が使用されています。[プルーフ・オブ・ウォーク](https://lostinbitcoin.sakuraweb.com/glossary/pow/)の作成にはハッシュ関数[SHA-256](https://lostinbitcoin.sakuraweb.com/glossary/sha_256/)が使用され、[txid](https://lostinbitcoin.sakuraweb.com/glossary/txid/)の生成にはSHA-256が2回適用されます。公開鍵のハッシュやアドレスの生成には、SHA-256とRIPEMD160のハッシュ関数を組み合わせたhash160関数が使用されています。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
