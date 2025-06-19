---
title: 検閲耐性
taxonomy:
    category:
        - glossary
---

## Censorship Resistance
2,100 sats

<div><button class="zap-button" data-npub="npub1u3rz86hzjejkh54mg04u20sxe62ps3nhtqy987n6yqv6sx52uhjsnkn4se" data-relays="wss://relay.damus.io,wss://relay.snort.social,wss://nostr.wine,wss://relay.nostr.band">Zap Me ⚡</button><a href="https://twitter.com/fuuuumin314">@fuuuumin314</a></div>

[ビットコイン](https://lostinbitcoin.sakuraweb.com/glossary/bitcoin/)の送金を取り消したり、特定の[ウォレット](https://lostinbitcoin.sakuraweb.com/glossary/wallet/)や[アドレス](https://lostinbitcoin.sakuraweb.com/glossary/address/)を凍結することは誰にもできません。この意味で、ビットコインには検閲耐性があります。[トランザクション](https://lostinbitcoin.sakuraweb.com/glossary/transaction/)のブロードキャストや[ブロック](https://lostinbitcoin.sakuraweb.com/glossary/block/)への取り込みは[ノード](https://lostinbitcoin.sakuraweb.com/glossary/node/)とマイナーに一任されているため、第三者が検閲することは実質的に不可能です。

ビットコインネットワークにブロードキャストされたトランザクションは、ノードからノードに次々と伝播されます。ノードは受信したトランザクションを[メンプール](https://lostinbitcoin.sakuraweb.com/glossary/mempool/)（mempool、メモリープール）と呼ばれる未承認トランザクションのデータベースに格納します。マイナーは[ブロックチェーン](https://lostinbitcoin.sakuraweb.com/glossary/blockchain/)に追加するブロックに含めるトランザクションをメンプールから選びます。マイナーがブロックの[マイニング](https://lostinbitcoin.sakuraweb.com/glossary/mining/)に成功すると、ブロックに含まれるトランザクションはメンプールから削除され、[承認](https://lostinbitcoin.sakuraweb.com/glossary/confirmation/)されます。

この一連のプロセスには第三者による介入機会はほとんどありません。送金者はビットコインネットワーク上のノードに何らかの方法で接続さえできれば、トランザクションをブロードキャストでき、あとは承認を待つのみです。政府などによるトランザクションの検閲リスクを軽減するため、ビットコイン開発者はインターネット以外にもメッシュネットワーク、衛星、アマチュア無線を介したトランザクションのブロードキャストを可能にしました。

---
コンテンツの著作権は [River Financial](https://river.com/) に帰属します。二次利用の可否は権利者にご確認ください。 / All rights reserved to River Financial.
