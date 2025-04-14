---
title: ブロック
taxonomy:
    category:
        - glossary
---

## Block
2,100 sats

ブロックとは、[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)ネットワーク上で行われた取引をまとめたものです。ブロックは時系列的に結びつけられ、[ブロックチェーン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/blockchain/)を形成します。ほとんどのブロックは、約2700の取引が含まれ、サイズは最大4MBです。ブロックがブロックチェーンに追加される条件として、そのブロックのハッシュがビットコインの[プルーフオブワーク](http://lostinbitcoin.jp.testrs.jp/staging/glossary/pow/)を満たすことと、直前のブロックハッシュを含むことがあります。直前のブロックハッシュを含むことで、後続するブロックを無効化せずにあるブロックを改ざんできないことが保証されます。この特徴は、決定論的で任意な[ハッシュ関数](http://lostinbitcoin.jp.testrs.jp/staging/glossary/hash_function/)のお陰です。この過程でビットコインの[不変性](http://lostinbitcoin.jp.testrs.jp/staging/glossary/immutability/)が生まれます。例えば、もしブロック数400が改ざんされたら、ブロック数400のハッシュが変わってそのブロックのプルーフオブワークが無効になります。加えて、ブロック数401の「前ハッシュ」パラメータはブロック数400のハッシュと一致しなくなり、ブロック数401も無効になります。この変化が波及し、ブロック数401以降のブロックが切り離されます。この特徴は、ブロックがブロックチェーンに追加された時点から、そのブロックと含まれている取引を改ざんできないことを保証します。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
