---
title: 難易度
taxonomy:
    category:
        - glossary
---

## Difficulty
2,100 sats

難易度とは、[ブロック](https://lostinbitcoin.sakuraweb.com/glossary/block/)を[マイニング](https://lostinbitcoin.sakuraweb.com/glossary/mining/)する際の困難さを示す指標です。ブロックをマイニングするためには、マイナーは公開しようとするブロックの有効なハッシュという[プルーフオブワーク](https://lostinbitcoin.sakuraweb.com/glossary/pow/)を示す必要があります。ハッシュは基本的に大きな数値であり、有効なハッシュとされるためには、あらかじめ定められた目標値よりも小さい値でなければなりません。この目標値がマイニングの難易度を決定し、[ビットコイン](https://lostinbitcoin.sakuraweb.com/glossary/bitcoin-2/)のルールセットによって設定されます。

難易度は動的に変化し、2016ブロック（約2週間）ごとに調整されます。これはビットコインのブロック生成が平均して約10分ごとに行われるようにするためです。もしネットワークに参加するマイナーが増加しブロック生成速度が速くなれば、難易度は上昇します。逆にマイナーが減少しブロック生成が10分より遅くなれば、難易度は低下します。したがって、難易度はネットワーク全体の[ハッシュレート](https://lostinbitcoin.sakuraweb.com/glossary/hash_rate/)の変動に直接対応しています。

技術的にはより正確には、ビットコインネットワークは難易度ではなく目標値を設定しています。すべての有効なプルーフオブワークはこの目標値未満でなければならず、その点で難易度は単に目標値の逆数であると言えます。目標値が高く設定されると、マイナーがその値未満のハッシュを見つけやすくなるため、難易度は低下します。同様に目標値が低く設定されると、難易度は上昇します。この目標値は各[ブロックヘッダー](https://lostinbitcoin.sakuraweb.com/glossary/block_header/)にエンコードされ、「bits」と呼ばれます。これにより、各[ノード](https://lostinbitcoin.sakuraweb.com/glossary/node-2/)は提供されたプルーフオブワークが目標値未満であるかどうかを直接検証することができます。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
