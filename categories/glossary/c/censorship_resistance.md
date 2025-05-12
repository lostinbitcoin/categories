---
title: 検閲耐性
taxonomy:
    category:
        - glossary
---

## Censorship Resistance
2,100 sats

<div><button class="zap-button" data-npub="npub1u3rz86hzjejkh54mg04u20sxe62ps3nhtqy987n6yqv6sx52uhjsnkn4se" data-relays="wss://relay.damus.io,wss://relay.snort.social,wss://nostr.wine,wss://relay.nostr.band">Zap Me ⚡</button><a href="https://twitter.com/fuuuumin314">@fuuuumin314</a></div>

[ビットコイン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/bitcoin/)の送金を取り消したり、特定の[ウォレット](http://lostinbitcoin.jp.testrs.jp/staging/glossary/wallet/)や[アドレス](http://lostinbitcoin.jp.testrs.jp/staging/glossary/address/)を凍結することは誰にもできません。この意味で、ビットコインには検閲耐性があります。[トランザクション](http://lostinbitcoin.jp.testrs.jp/staging/glossary/transaction/)のブロードキャストや[ブロック](http://lostinbitcoin.jp.testrs.jp/staging/glossary/block/)への取り込みは[ノード](http://lostinbitcoin.jp.testrs.jp/staging/glossary/node/)とマイナーに一任されているため、第三者が検閲することは実質的に不可能です。

ビットコインネットワークにブロードキャストされたトランザクションは、ノードからノードに次々と伝播されます。ノードは受信したトランザクションを[メンプール](http://lostinbitcoin.jp.testrs.jp/staging/glossary/mempool/)（mempool、メモリープール）と呼ばれる未承認トランザクションのデータベースに格納します。マイナーは[ブロックチェーン](http://lostinbitcoin.jp.testrs.jp/staging/glossary/blockchain/)に追加するブロックに含めるトランザクションをメンプールから選びます。マイナーがブロックの[マイニング](http://lostinbitcoin.jp.testrs.jp/staging/glossary/mining/)に成功すると、ブロックに含まれるトランザクションはメンプールから削除され、[承認](http://lostinbitcoin.jp.testrs.jp/staging/glossary/confirmation/)されます。

この一連のプロセスには第三者による介入機会はほとんどありません。送金者はビットコインネットワーク上のノードに何らかの方法で接続さえできれば、トランザクションをブロードキャストでき、あとは承認を待つのみです。政府などによるトランザクションの検閲リスクを軽減するため、ビットコイン開発者はインターネット以外にもメッシュネットワーク、衛星、アマチュア無線を介したトランザクションのブロードキャストを可能にしました。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
